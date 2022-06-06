## js coding
- [161](https://github.com/Advanced-Frontend/Daily-Interview-Question/issues/431)
  ```js
  const data = {
    a: 2,
    b: 3,
    c: 4,
    d: 5
  }

  Object.prototype.myMap = function (cb,thisObj){
    const result = {}
    const obj = this

    for(let key in obj){
      if(obj.hasOwnProperty(key)){
        result[key] = cb.call(this,obj[key],key,thisObj || obj)
      }
    }
    return result
  }
  console.log(data.myMap((val,key)=>{
    return val + 2
  }))
  ```