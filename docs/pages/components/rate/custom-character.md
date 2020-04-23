### 自定义渲染

当有多级评价时，你可以自定义每级展现的 character，不过这需要你自己实现

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
    <div>
      <Rate defaultValue={1} renderCharacter={renderCharacter} />
    </div>
    <div>
      <Rate defaultValue={2} renderCharacter={renderCharacter} />
    </div>
    <div>
      <Rate defaultValue={3} renderCharacter={renderCharacter} />
    </div>
    <div>
      <Rate defaultValue={4} renderCharacter={renderCharacter} />
    </div>
    <div>
      <Rate defaultValue={5} renderCharacter={renderCharacter} />
    </div>

    <hr />

    <Rate max={10} defaultValue={2} />
  </div>
);

ReactDOM.render(instance);
```

<!--end-code-->