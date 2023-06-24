## React 有哪些 hooks
##### useState()：状态钩子
useState()用于为函数组件引入状态（state）；
##### useContext(): 共享状态钩子
如果需要在组件之间共享状态，可以使用useContext()。
##### useEffect()：副作用钩子。
useEffect()用来引入具有副作用的操作，
##### useReducer()：action 钩子
useReducers()钩子用来引入 Reducer 功能。





## 为什么使用 hooks
 Hooks 可以从组件中提取状态逻辑，使这些逻辑可以单独的测试和复用。
 相比较类组件，结构和逻辑更清晰。