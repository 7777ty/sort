# 数组排序
**问：** 给出正整数数组 array = [2,1,5,3,8,4,9,5]
请写出一个函数 sort，使得 sort(array) 得到从小到大排好序的数组 [1,2,3,4,5,5,8,9]
新的数组可以是在 array 自身上改的，也可以是完全新开辟的内存。
不得使用 JS 内置的 sort API

**答：**
```javascript
let sort = (numbers) => {
    let i, j, max
    for (j = 0; j < numbers.length; j++) {
        for (i = 0; i < numbers.length - 1; i++) {
            if (numbers[i] > numbers[i + 1]) {
                max = numbers[i]
                numbers[i] = numbers[i + 1]
                numbers[i + 1] = max
            }
        }
    }
}
```