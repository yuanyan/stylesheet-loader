# stylesheet-loader
A webpack loader that imports a css file and converts it to be used as an inline style

## Usage
```css
/* foo.css */
.container {
  color: red;
  background-color: blue;
}
```

```js
import styles from 'stylesheet!css!./foo.css';
// import styles from 'stylesheet!css!less!./foo.less';
function Foo() {
  return <div style={styles.container} />;
}
export default Foo;
```

## Limitations
Because the css is inlined, pseudo classes (`:hover`, `:active`, ...) can't be supported.  
