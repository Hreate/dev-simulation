crontab

1.  \* ：表示匹配该域的任意值。假如在 Minutes 域使用 \* ，即表示每分钟都会触发事件。
2.  / ：表示起始时间开始触发，然后每隔固定时间触发一次。例如在 Minutes 域使用 5/20 ，则意味着5分钟触发一次，而25，45等分别触发一次。
3.  , ：表示列出枚举值。例如：在 Minutes 域使用 5,20 ，则意味着在5和20分钟触发一次。
4.  \- ：表示范围。例如在 Minutes 域使用 5-20，表示从5分钟到20分钟每分钟触发一次。
5.  ? ：只能在 DayofMonth 和 DayofWeek 两个域中使用。它也匹配域的任意值，但实际不会。因为 DayofMonth 和 DayofWeek 会相互影响。例如想在每月的20日触发调查，不管20日到底是星期几，则只能使用如下写法：13 13 15 20 * ? ，其中最后一位只能用 ? ，而不能使用 * ，如果使用 * 表示不管星期几都会触发，实际上并不是这样。

