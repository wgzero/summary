# 小技巧

## 1.数组、对象

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <script>
    // 计算数组中大于5的数字
    const arr = [1,3,5,7,10]
    const res = arr.filter(item => item > 5)
    console.log("res", res) // 7, 10
    // 大于五且等于10的数字
    const r1 = arr.filter(item => item > 5).find(item => item == 7)
    console.log("r1---", r1) // 7
    const obj = {
      name: "summer"
    }
    // 展开对象加入新的值
    let resObj = { ...obj, age: 10}
    console.log("resObj", resObj) // {name: "summer", age: 10}
    // async + await
    const add = (x, y) => x + y
    async function show(){
      const met = await add(2, 3)
      console.log("met", met) // 5
    }
    show()
    let obj2 = { 
       sex: "男"
    }
    let obj3 = {
      name: "zero"
    } 
    let obj1 = Object.assign(obj2, obj3)
    console.log("obj1", obj1) // {sex: "男", name: "zero"}
    // 解构赋值-点到为止
    let arrObj = {
      list: {
        id: 1,
        address: "shenzhen"
      }
    }
    let { list } = arrObj
    console.log("list", list)  // {id: 1, address: "shenzhen"}
      // &&都为真取第二个，第一个为假的，那就取第一个值
    const yn = 11&&22
    const yn1 = 0&&22
    console.log("yn", yn, yn1) // 22 0
    // ||都为真取第一个，第一个为假的，那就取第二个值
    const ny = 11||22
    const ny1 = 0 || 22
    const ny2 = 0 || false
    console.log("ny", ny, ny1, ny2) // 11 22 false
    // 三目运算
    const result = 5 > 3 ? 5 : 3;
    console.log("result", result) // 5
  </script>
</body>
</html>
```

## 2.一个空对象和一个有数据的对象遍历赋值

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <script>
    // 有数据对象
    let obj = {
      name: "summer",
      age: 18,
      school: "一中"
    }
    // 无数据对象
    let emptyObj = {
      name: "",
      age: "",
      school: ""
    }
    // 长度统计
    let num = 0
    // 有对象数据赋值给无对象数据
    for(let key in obj){
      num++
      for(let emptyKey in emptyObj){
        emptyObj[key] = obj[key]
      }
    }
    console.log("xxxxx", emptyObj, num) // {name: "summer", age: 18, school: "一中"} 3
  </script>
</body>
</html>
```

