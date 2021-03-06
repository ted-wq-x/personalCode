## Hibernate Validator 常用注解


|注解|	作用|
|---|---|
|@Valid	|被注释的元素是一个对象，需要检查此对象的所有字段值|
|@Null	|被注释的元素必须为 null|
|@NotNull	|被注释的元素必须不为 null|
|@AssertTrue	|被注释的元素必须为 true|
|@AssertFalse	|被注释的元素必须为 false|
|@Min(value)	|被注释的元素必须是一个数字，其值必须大于等于指定的最小值|
|@Max(value)	|被注释的元素必须是一个数字，其值必须小于等于指定的最大值|
|@DecimalMin(value)|	被注释的元素必须是一个数字，其值必须大于等于指定的最小值|
|@DecimalMax(value)	|被注释的元素必须是一个数字，其值必须小于等于指定的最大值|
|@Size(max, min)	|被注释的元素的大小必须在指定的范围内|
|@Digits (integer, fraction)	|被注释的元素必须是一个数字，其值必须在可接受的范围内|
|@Past	|被注释的元素必须是一个过去的日期|
|@Future	|被注释的元素必须是一个将来的日期|
|@Pattern(value)	|被注释的元素必须符合指定的正则表达式|

hibernate补充的注解中，最后3个不常用，可忽略。
主要区分下@NotNull,@NotEmpty,@NotBlank 3个注解的区别：

@NotNull：任何对象的value不能为null
@NotEmpty：集合对象的元素不为0，即集合不为空，也可以用于字符串不为null
@NotBlank：只能用于字符串不为null，并且字符串trim()以后length要大于0

## Hibernate Validator 附加的 constraint

|注解|	作用|
|---|---|
|@Email	|被注释的元素必须是电子邮箱地址|
|@Length(min=, max=)	|被注释的字符串的大小必须在指定的范围内|
|@NotEmpty	|被注释的字符串的必须非空|
|@Range(min=, max=)	|被注释的元素必须在合适的范围内|
|@NotBlank	|被注释的字符串的必须非空|
|@URL(protocol=,host=, port=, regexp=, flags=)|	被注释的字符串必须是一个有效的url|
|@CreditCardNumber|	被注释的字符串必须通过Luhn校验算法，银行卡，信用卡等号码一般都用Luhn计算合法性|
|@ScriptAssert(lang=, script=, alias=)	|要有Java Scripting API 即JSR 223 ("Scripting for the JavaTM Platform")的实现|
|@SafeHtml(whitelistType=, additionalTags=)	|classpath中要有jsoup包|
