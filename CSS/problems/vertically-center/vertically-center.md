### 1. Absolute Positioning and margin auto
```
  .container {
    position: relative;
  }

  .element {
    position: absolute;
    top: 0; bottom: 0; left: 0; right: 0;
    margin: auto;
    height: 20px;
  }
```

### 2. Classic Top 50% translate - 50%
```
  .container {
    position: relative;
  }

  .element {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
  }
```

### 3. Margin auto on a flex-item
```
  .container {
    display: flex;
  }

  .element {
    margin: auto;
  }
```

### 4. 