# Plain React Redux

-   reducers - manages state and returns the updated state
-   actions - have 2 properties, a unique identifier and payload with data
-   dispatch - used to send actions to update the data

**Note:** The reducers functions shouldn't be asynchronous

**Note:** The reducers functions shouldn't mutate the original state

## How to select a state from the store

```js
import { useSelector } from 'react-redux';

const counter = useSelector((state) => state.counter);
```

## How to dispatch an action

```js
import { useDispatch } from 'react-redux';

const dispatch = useDispatch();

const increment = () => {
    dispatch({ type: 'ADD', payload: 10 });
};
```

## Example of a reducer function

```js
const reducerFn = (state = { counter: 0 }, action) => {
    if (action.type === 'ADD') {
        return { counter: state.counter + action.payload };
    }
};
```

# React Redux Toolkit

## Example of creating a slice

```js
import { configureStore, createSlice } from '@reduxjs/toolkit';

const counterSlice = createSlice({
    name: 'counter',
    initialState: { counter: 0},
    reducers: {
        increment(state, action) {
            state.counter += 1;
        }
        increment(state, action) {
            state.counter -= 1;
        }
        addBy(state, action) {
            state.counter += action.payload;
        }
    }
});

export const actions = counterSlice.actions;

const store = configureStore({
    reducer: counterSlice.reducer
});

export default store;
```
