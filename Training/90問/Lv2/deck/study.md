# 学んだこと
- vectorでdequeを再現するのは良くない
- C++のvectorとdequeは、実装が異なるため、同じように扱ってもメモリ使用量が異なることがあります。vectorは要素が連続した領域に格納されるため、要素の挿入や削除が発生した場合、元の要素をコピーして、新たな領域に要素を再配置する必要があります。そのため、vectorの要素数が増えるほど、要素を挿入や削除するたびにメモリの再配置が発生し、その分メモリ消費量が増えます。

一方、dequeは、要素が分割された領域に格納されます。要素の挿入や削除が発生した場合、必要に応じて新しい領域を割り当て、元の領域のデータを転送することで対処します。dequeは、先頭と末尾の要素の挿入や削除が高速であるという利点がありますが、要素が分割された領域に格納されるため、vectorよりもメモリ使用量が多くなることがあります。

したがって、vectorでdequeを再現しようとすると、vectorが本来持っていない特性を実現するために、余分なメモリ消費が発生する可能性があります。一方、dequeは元々その特性を持っているため、余分なメモリ消費が発生せずに要素の挿入や削除が行えます。(引用：chatgpt)
