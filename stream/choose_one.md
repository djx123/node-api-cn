
可读流 API 的演化贯穿了多个 Node.js 版本，提供了多种方法来消费流数据。通常开发者应该选择其中 *一种* 来消费数据，而 *不应该* 在单个流使用多种方法来消费数据。

对于大多数用户，建议使用 `readable.pipe()` 方法来消费流数据，因为它是最简单的一种实现。开发者如果要精细地控制数据传递和产生的过程，可以使用 [`EventEmitter`][] 和 `readable.pause()`/`readable.resume()` 提供的 API 。

