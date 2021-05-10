## utils-validation-type
数据类型验证

### 运行环境

- PHP >= 7.4

### 安装

```
composer require 7csn/utils-validation-type
```

### 应用说明

* 方法
    ```php
    use chaser\utils\validation\Type;
    use InvalidArgumentException;
    
    // 判断数值类型是否无效
    Type::invalid($value, int $type, array &$declarations = []): bool;
    
    // 验证数值类型（未通过抛出异常）
    Type::validate(string $name, $value, int $type): void;
    
    // 类型异常
    Type::exception(string $name, string $declaration): InvalidArgumentException;
    ```
* 类型（$type），可用“|”结合使用
    * Type::NULL    
    * Type::INT
    * Type::FLOAT
    * Type::STRING
    * Type::ARRAY
    * Type::OBJECT
    * Type::CALLABLE
    * Type::RESOURCE
