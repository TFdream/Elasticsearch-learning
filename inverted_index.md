# 倒排索引
见其名知其意，有倒排索引，对应肯定，有正向索引。

正向索引（forward index），反向索引（inverted index）更熟悉的名字是倒排索引。

在**搜索引擎**中每个文件都对应一个文件ID，文件内容被表示为一系列关键词的集合（实际上在搜索引擎索引库中，关键词也已经转换为关键词ID）。例如“文档1”经过分词，提取了20个关键词，每个关键词都会记录它在文档中的出现次数和出现位置。

