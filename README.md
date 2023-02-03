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
    // 命令冷却时间(秒) (#默认如下)
    'cd': 0

    // 冷却模式 (#默认如下)
    // wait -> 等待图片撤回后计时(#默认), <其他> -> 发送后立即开始计时
    'cdmod': 'wait'

    // 处于cd时发送的内容 ('{time}'会自动替换为剩余时间秒数) (#默认如下)
    'cdstring': '太...太快啦! 等我{time}秒行不行?AwQ'

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
- [x] 在等待撤回等待期间会阻塞主线程导致消息无法发送

## 新增功能
* V0.1.1 增加了cd(冷却时间)功能~ | 2023-02-03 21:03:02
