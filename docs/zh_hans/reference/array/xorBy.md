# xorBy

使用自定义映射函数计算两个数组之间的对称差异。

对称差异是指在任一数组中存在，但不在它们的交集中的元素集合，根据映射函数返回的值确定。

## 签名

```typescript
function xorBy<T, U>(arr1: T[], arr2: T[], mapper: (item: T) => U): T[];
```

### 参数

- `arr1` (`T[]`): 第一个数组。
- `arr2` (`T[]`): 第二个数组。
- `mapper` (`(item: T) => U`): 将数组元素映射为比较值的函数。

### 返回值

(`T[]`): 包含在 `arr1` 或 `arr2` 中存在但不同时存在于两者中的元素的数组，基于映射函数返回的值。

## 示例

```typescript
// 返回 [{ id: 1 }, { id: 3 }]
xorBy([{ id: 1 }, { id: 2 }], [{ id: 2 }, { id: 3 }], x => x.id);
```