# @rooks/use-interval

### Installation

```
npm install --save @rooks/use-interval
```

### Usage

```react
function reducer(state, action) {
  switch (action.type) {
    case "increment":
      return { count: state.count + 1 };
    default:
      return state;
  }
}

function Demo() {
  const [value, dispatcher] = useReducer(reducer, { count: 0 });

  function increment() {
    dispatcher({
      type: "increment"
    });
  }

  const { start, stop } = useInterval(() => {
    increment();
  }, 1000);

  return (
    <>
      <p>value is {value.count}</p>
      <button onClick={start}>Start</button>
      <button onClick={stop}>Stop</button>
    </>
  );
}
render(<Demo/>)
```

### Arguments

| Argument         | Type     | Description                                              | Default value |
| ---------------- | -------- | -------------------------------------------------------- | ------------- |
| callback         | function | Function be invoked after each interval duration         | undefined     |
| intervalDuration | number   | Duration in milliseconds after which callback is invoked | undefined     |
| startImmediate   | boolean  | Should the timer start immediately or no                 | false         |



# A react hook for using setInterval