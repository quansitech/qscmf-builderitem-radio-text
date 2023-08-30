# qscmf-builderitem-radio-text

radio-text builder组件

#### 效果截图
##### form_type
![image](https://github.com/quansitech/qscmf-builderitem-radio-text/assets/18739970/e22b4b1d-3079-45d1-9c82-2657814c32dd)

##### column_type
![image](https://github.com/quansitech/qscmf-builderitem-radio-text/assets/18739970/548df282-a751-40a2-a39e-60cb461bb124)

#### 安装

```php
composer require quansitech/qscmf-builderitem-radio-text
```

#### 如何使用

+ FormType

  ```php
  // title: 选项标题
  // key: 选现对应的键值
  // need_text 是否需要填写额外的文本项
  $option = [
    [
        'title' => '网站开发',
        'key' => 1,
    ],
    [
        'title' => '公众号运维',
        'key' => 2,
    ],
    [
        'title' => '其他',
        'key' => 3,
        'need_text' => true,
    ]
  ];
  ->addFormItem("main_business", "radio_text", "主营业务", "", $option)
  
  //注意：组件会自动构造好json格式的数据提交，直接存入对应的数据库字段即可
  ```

+ ColumnType

  ```php
    $option = [
        [
            'title' => '网站开发',
            'key' => 1,
        ],
        [
            'title' => '公众号运维',
            'key' => 2,
        ],
        [
            'title' => '其他',
            'key' => 3,
            'need_text' => true,
        ]
    ];
  ->addTableColumn("main_business", "主营业务", "radio_text", $option)
  ```
