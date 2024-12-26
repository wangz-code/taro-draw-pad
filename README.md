<div align='center'>
    <h1>taro-draw-pad</h1>
</div>

<p align="center">
  <a href="https://www.npmjs.com/package/taro-draw-pad"><img src="https://img.shields.io/npm/v/taro-draw-pad.svg?sanitize=true" alt="Version"></a>
  <a href="https://www.npmjs.com/package/vue"><img src="https://img.shields.io/npm/l/vue.svg?sanitize=true" alt="License"></a>
  
</p>
taro-react的手写签名库&绘图板

只支持 taro3 小程序，h5 没有做兼容处理，只支持 Canvas type="2d"

### 安装

```
npm install taro-draw-pad
```

### 使用

```
import {SignaturePad} from "taro-draw-pad";

...
//组件默认是100%高宽

<Signature
    className="signature-canvas"
    ref={signatureRef}
/>
```

### Api

| name        | type     | Description                                                       |
| ----------- | -------- | ----------------------------------------------------------------- |
| isEmpty     | boolean  | 判断是否签名是空白的                                              |
| fromDataURL | function | 还原签名数据 `dataUrl`: 图片的 base64 数据 `options` `callback`法 |
| toDataURL   | function | 获取签名数据 toDataURL(type, encoderOptions) 默认为 png 图片，    |
| clear       | function | 清空签名数据                                                      |
| save        | function | 将签名数据转换为 png 图片并且保存到系统相册                       |
| padCurr     | function | canvas对象                       |

toDataURL:https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLCanvasElement/toDataURL

### 截图

![draw.png](https://raw.githubusercontent.com/WangSunio/img/main/images/draw.png)
