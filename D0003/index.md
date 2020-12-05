# D0003

## 在页面上隐藏元素的方法有哪些？

### 占位:
* visibility: hidden;
* margin-left: -100%;
* opacity: 0;
* transform: scale(0);

### 不占位:
* display: none;
* width: 0; height: 0; overflow: hidden;

### 仅对块内文本元素:

* text-indent: -9999px;
* font-size: 0;


