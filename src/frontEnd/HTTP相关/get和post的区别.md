## GET 和 POST 的区别
GET 和 POST 本质的区别，是语意的区别，GET 是读，POST 是取。

1、GET是幂等的，POST 不是幂等的。

    幂等：一个操作无论多做少次，结果不变，GET 是读操作，无论做多少次，都不会改变结果，
         POST 是写操作，每次操作的结果都不一样。

2、参数不同

    通常情况下，GET 的参数放在 URL 里面，POST 参数放在 body 里面。
    因为地址栏会直接曝露 URL ，所以 GET 没有 POST 安全。
    浏览器对 URL 会有长度限制，比较小，POST Body 的限制比较大，可以传输更多的数据。
