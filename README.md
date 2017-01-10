# TODO

分类后排出不要的功能

删除过期的功能 //通过对API的查询进行验证 添加时间

# 用关键字删除功能 
----

$params = [
    'index' => 'sanctions_lists',
    'type' => $listName,
    'body' => [
        'query' => [
            'match_all' => []
        ]
    ]
];
return $this->deleteByQuery($params);
-----

删除重复的功能
