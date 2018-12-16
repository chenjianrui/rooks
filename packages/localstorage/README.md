# @rooks/use-localstorage

### Installation

```
npm install --save @rooks/use-localstorage
```

### Usage

```react
function Demo() {
  const { value, set, remove } = useLocalStorage("my-value", 0);
  return (
    <p>
      Value is {value}{" "}
      <button onClick={() => set(value !== null ? parseFloat(value) + 1 : 0)}>
        Increment
      </button>
      <button onClick={remove}>Remove </button>
    </p>
  );
}

render(<Demo/>)
```

# Local Storage hook for React