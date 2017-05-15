##一个简单的轮播图
> 含有 js 和 jQuery版本


###JavaScript 疑虑:
```javascript
container.onmouseover = stopPlay;   // 拷贝 该函数；
container.onmouseover = stopPlay(); // 错误， 加括号为调用该函数，
```                 
                    
按 index 位移，对于有动画的图片，不是很好的解决方案, 违反 S.O.L.I.D五大原则之单一职责SRP, 过度依赖index。 

应该使用 传位移解决
```javascript
function animate(offset) {  // 错误的设计
    oldIndex = index;
    list.style.left = offset * index + "px";
}
```
