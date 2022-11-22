---
id: entry-statistics
title: "Entry Statistics"
---

ZIO Cache also tracks statistics associated with each entry, such as when the entry was last accessed. You can access the statistics for a specified entry using the `entryStats` operator on `Cache`.

```scala mdoc
import zio._

import java.time.Instant

trait EntryStats {
  def loaded: Instant
}

trait Cache[-Key, +Error, +Value] {
  def entryStats: UIO[EntryStats]
}
```

More entry statistics will be added over time.
