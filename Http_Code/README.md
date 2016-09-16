###HTTP状态吗
* 100 请求者应继续进行请求。服务器返回此代码以表示，服务器已收到某项请求的第一部分，正等待接收剩余部分。

* 101 请求者已要求服务器切换协议，服务器已确认并准备切换。

* 200 服务器已成功处理相应请求。通常，这表示服务器提供了请求的网页。如果您的 robots.txt 文件显示为此状态，则表示 Googlebot 已成功检索到该文件。

* 201 请求成功且服务器创建了新的资源。

* 202 服务器已接受相应请求，但尚未对其进行处理。

* 203 服务器已成功处理相应请求，但返回了可能来自另一来源的信息。

* 204 服务器已成功处理相应请求，但未返回任何内容。

* 205 服务器已成功处理相应请求，但未返回任何内容。与 204 响应不同，此响应要求请求者重置文档视图（例如清除表单内容以输入新内容）

* 206 服务器成功处理了部分 GET 请求。

* 300 服务器可以根据请求来执行多项操作，例如：按照请求者（用户代理）的要求来选择某项操作或者展示列表以便请求者选择其中某项操作。

* 301 请求的网页已被永久迁移至新位置。服务器返回此响应（作为对 GET 或 HEAD 请求的响应）时，会自动将请求者转到新位置。您应使用此代码通知 Googlebot 某个网页或网站已被永久迁移至新位置。

* 302 服务器目前正从不同位置的网页响应请求，但请求者应继续使用原有位置来进行以后的请求。此代码与响应 GET 和 HEAD 请求的 301 代码类似，会自动将请求者转到不同的位置。但由于 Googlebot 会继续抓取原有位置并将其编入索引，因此您不应使用此代码来通知 Googlebot 某个页面或网站已被迁移。

* 303 当请求者应对不同的位置进行单独的 GET 请求以检索响应时，服务器会返回此代码。对于除 HEAD 请求之外的所有请求，服务器会自动转到其他位置。

* 304 请求的网页自上次请求后再也没有修改过。当服务器返回此响应时，不会返回相关网页的内容。
如果网页自请求者上次请求后再也没有更改过，您应当将服务器配置为返回此响应（称为 If Modified-Since HTTP 标头）。服务器可以告诉 Googlebot 自从上次抓取后网页没有变更，进而节省带宽和开销。

* 305 请求者只能使用代理访问请求的网页。如果服务器返回此响应，那么服务器还会指明请求者应当使用的代理。

* 307 服务器目前正从不同位置的网页响应请求，但请求者应继续使用原有位置来进行以后的请求。此代码与响应 GET 和 HEAD 请求的 301 代码类似，会自动将请求者转到不同的位置。但由于 Googlebot 会继续抓取原有位置并将其编入索引，因此您不应使用此代码来通知 Googlebot 某个页面或网站已被迁移。

* 400 服务器不理解请求的语法。

* 401 请求要求进行身份验证。登录后，服务器可能会返回对页面的此响应。

* 403 服务器正在拒绝相应请求。如果 Googlebot 在尝试抓取网站的有效网页时收到此状态代码（您可在 Google Search Console 中运行状况下的抓取错误页上进行查看），则可能是因为您的服务器或主机正在阻止 Googlebot 进行访问。

* 404 服务器找不到请求的网页。例如，如果相应请求是针对服务器上不存在的网页进行的，那么服务器通常会返回此代码。如果您的网站上没有 robots.txt 文件，而您在 Google Search Console 中的已拦截的网址页上看到此状态，那么这就是正确的状态。但是，如果您有 robots.txt 文件而又看到此状态，则说明您的 robots.txt 文件可能命名错误或位于错误的位置（该文件应当位于顶级域名上，且应当名为 robots.txt）。如果您在 Googlebot 尝试抓取的网址上看到此状态，那么这表示 Googlebot 追踪的可能是另一网页中的无效链接（旧链接或输入有误的链接）。

* 405 禁用请求中所指定的方法。

* 406 无法使用请求的内容特性来响应请求的网页。

* 407 此状态代码与 401（未授权）类似，但却指定了请求者应当使用代理进行授权。如果服务器返回此响应，那么，服务器还会指明请求者应当使用的代理。

* 408 服务器等待请求超时。

* 409 服务器在完成请求时遇到冲突。服务器必须在响应中包含该冲突的相关信息。服务器在响应与前一个请求相冲突的 PUT 请求时可能会返回此代码，同时会提供两个请求的差异列表。

* 410 如果请求的资源已被永久移除，那么，服务器会返回此响应。该代码与 404（未找到）代码类似，但在资源以前有但现在已经不复存在的情况下，有时会替代 404 代码出现。如果资源已被永久删除，那么，您应当使用 301 代码指定该资源的新位置。

* 411 服务器不会接受包含无效内容长度标头字段的请求。

* 412 服务器未满足请求者在请求中设置的其中一个前提条件。
 
* 413 服务器无法处理请求，因为请求实体过大，已超出服务器的处理能力。
 
* 414 请求的 URI（通常为网址）过长，服务器无法进行处理。
 
* 415 请求的格式不受请求页面的支持。 
 
* 416 如果相应请求是针对网页的无效范围进行的，那么服务器会返回此状态代码。 
 
* 417 服务器未满足“期望”请求标头字段的要求。 
 
* 500 服务器遇到错误，无法完成请求。

* 501 服务器不具备完成相应请求的功能。例如，当服务器无法识别请求方法时，可能便会返回此代码。

* 502 服务器作为网关或代理，从上游服务器收到了无效的响应。

* 503 目前无法使用服务器（由于超载或进行停机维护）。通常，这只是一种暂时的状态。

* 504 服务器作为网关或代理，未及时从上游服务器接收请求。

* 505 服务器不支持相应请求中所用的 HTTP 协议版本。