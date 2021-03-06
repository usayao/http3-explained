# HTTP/3优先度

HTTP/3中有一种帧是优先度（`PRIORITY`）。与HTTP/2中的类似，它用于设定一个流的优先度和依赖关系。

该帧可以设定一个流依赖于另一个流，也可以设定特定流的“权重”。

服务器应该只在一个流所依赖的所有流都被关闭，或者都无法取得进展时为该流分配资源。

一个流的权重是介于1到256之间的值，有着相同父系流的流**应该**按照权重的比例分配资源。
