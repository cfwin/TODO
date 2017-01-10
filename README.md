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
$params = array(
    "body" => array(
        "query" => array(
            "filtered" => array(
                "query" => array(
                    "match_phrase" => array(
                        "content"  => "XXXXXX"
                    ),
                ),
            ),
        ),
    ),
);

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
去掉空格
去掉全角空格
然后变成指纹
然后在指纹库中验证
```

### python api test
```
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello World!'

@app.route('/user/<username>')
def show_user_profile(username):
    # show the user profile for that user
    return 'User %s' % username

@app.route('/post/<int:post_id>')
def show_post(post_id):
    # show the post with the given id, the id is an integer
    return 'Post %d' % post_id

if __name__ == '__main__':
    app.run()
```
