# for-in使用

## 一、用途
-----
用来遍历对象，获取每个属性的键值，同时也可以用来遍历数组，获取数组的键值

```
for(var k in window) {
	console.log(k);
}
```

## 二、注意事项
尽量不用使用`for-in`来遍历数组，除了会遍历数组的键值外，还会遍历其它附加的属性
```javascript
var foo = [1,2];
foo.z = 4;
for(var k in foo) {
	console.log(k);
}
//输出 0 1 z
```
