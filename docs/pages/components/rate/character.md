### 字符

你可以使用其他 icon、数字、中文或是其他自定义的图案

<!--start-code-->

```js
const App = () => {
  const [value, setValue] = React.useState(2.5);
  const onChnage = value => {
    setValue(value);
  };
  return (
    <div>
      <div>
        <Rate
          allowHalf
          value={value}
          character={<Icon icon="heart" size="2x" />}
          color="red"
          onChange={onChnage}
        />
      </div>
      <div>
        <Rate allowHalf value={value} character="鼎" color="blue" onChange={onChnage} />
      </div>

      <div>
        <Rate allowHalf value={value} character="A" onChange={onChnage} />
      </div>
    </div>
  );
};

ReactDOM.render(<App />);
```

<!--end-code-->
