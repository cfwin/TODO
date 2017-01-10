# TODO

### 分类后排出不要的功能
----



### 删除过期的功能 
----
```
通过对API的查询进行验证 
防止API访问频繁，添加导入时间功能
```



### 用关键字删除功能 
----
```php
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
```
### 删除接口建立

```php
批量删除
for ($i = 303; $i < 310; $i++) {  
    $params ['body'][] = array(  
        'delete' => array(  
            '_index' => 'er',  
            '_type' => 'state',  
            '_id' => $i  
        )  
    );  
}  
$response = $client -> bulk($params);
```

```
单一删除
$params = [
    'index' => 'my_index',
    'type' => 'my_type',
    'id' => 'my_id'
];

// Delete doc at /my_index/my_type/my_id
$response = $client->delete($params);
```

### 删除重复的功能
----
```
导入的时候题目设置指纹进行验证
```

