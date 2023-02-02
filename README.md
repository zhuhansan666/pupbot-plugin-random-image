## 二次元图片随机发送 | pupbot-plugin-random-image

## 安装
```
/plugin add random-image
```

## 启用
```
/plugin on random-image
```

## 指令(默认)
* `来张图` -> 来一张图

## 配置文件详解

```
{
    // 可使用人群(不区分大小写)
    // admins -> 所有管理员(#默认), mainadmin -> 主管理员, <其他> -> 所有人
    'use-permisson': 'admins',
    
    // 撤回时间 (-1~120秒) -1 -> 不撤回 (#默认90秒) 
    // *时间可能比实际略短, 因为获取图片需要时间
    'recall-time': 90,

    // api 数组, api 应当直接跳转图片直链 (#默认如下)
    'random-api': [  
        'http://www.dmoe.cc/random.php',
        'http://img.xjh.me/random_img.php?return=302'
    ],
    
    // 触发词 (#默认如下)
    'command': [  
        '来张图'
    ]
}
```

## 问题 / 不合理设定 (√代表已修复)
* 暂无
