### Custom character

When there are multiple levels of rating, you can customize the character displayed at each level, but you need to implement this yourself

<!--start-code-->

```js
const renderCharacter = (value, index) => {
  // unselected character
  if (value <= index) {
    return <Icon icon="frown-o" size="2x" />;
  }
  if (value < 3) {
    return <Icon icon="frown-o" size="2x" style={{ color: '#ED5043' }} />;
  }
  if (value < 4) {
    return <Icon icon="meh-o" size="2x" style={{ color: '#F4CA1D' }} />;
  }
  return <Icon icon="smile-o" size="2x" style={{ color: '#F4CA1D' }} />;
};

const instance = (
  <div>
    <Rate defaultValue={2.5} renderCharacter={renderCharacter} />
    <hr />
    <Rate max={10} defaultValue={2} />
  </div>
);

ReactDOM.render(instance);
```

<!--end-code-->
