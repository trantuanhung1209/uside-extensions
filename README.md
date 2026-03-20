# Uside React Snippets

This extension provides useful React snippets for JavaScript React developers.

## Features

Snippets are organized by prefix group:
Current set includes **34 snippet prefixes**.

---

### `hook_` — React Hooks

| Prefix | Output | Description |
|---|---|---|
| `hook_usestate` | `const [state, setState] = useState(null)` | React useState hook |
| `hook_useeffect` | `useEffect(() => { ... }, [deps])` | React useEffect hook |
| `hook_useref` | `const refName = useRef(null)` | React useRef hook |
| `hook_useref_focus` | `useRef + useEffect` tự động focus input | useRef để focus DOM element khi mount |
| `hook_useRef_ex` | Component demo đầy đủ với `useRef` | Full example: useRef + focus button có giải thích |
| `hook_usememo` | `const memoValue = useMemo(() => ..., [deps])` | React useMemo hook |
| `hook_useMemo_filter` | Component demo `useMemo` lọc danh sách | useMemo tối ưu filter tránh tính lại không cần thiết |
| `hook_usecallback` | `const fn = useCallback(() => ..., [deps])` | React useCallback hook |
| `hook_usereducer` | `const [state, dispatch] = useReducer(reducer, initialState)` | useReducer with switch |
| `hook_useEffect_debounce` | Component debounce search với `useEffect` | Trì hoãn search 500ms dùng setTimeout + cleanup |
| `hook_custom` | `export const useHookName = () => { ... }` | Custom hook template |
| `hook_useCounter` | Custom hook `useCounter(initial)` | Hook counter có `inc/dec/reset` |
| `hook_fetch_users` | Custom hook `useFetchUsers()` | Hook fetch users có loading + error + refetch |

---

### `router_` — React Router App Setup

| Prefix | Output | Description |
|---|---|---|
| `router_layout` | `createBrowserRouter([...])` + `RouterProvider` | Full React Router v6 layout with nested routes |

---

### `route_` — Route Page Components

| Prefix | Output | Description |
|---|---|---|
| `route_dashboard` | `<Dashboard>` with `<Link>` nav + `<Outlet />` | Dashboard layout dùng React Router Outlet |

---

### `task_` — Components & Utilities

| Prefix | Output | Description |
|---|---|---|
| `task_rfc` | `const ComponentName = () => { ... }` | React functional component |
| `task_reactmemo` | `export default memo(ComponentName)` | Bọc component với React.memo |
| `task_fetchapi` | `const fetchData = async () => { ... }` | Fetch API với async/await và try/catch |
| `task_searchfilter` | `data.filter(item => item.name.includes(keyword))` | Lọc danh sách theo từ khóa |
| `task_pagination` | `currentItems = data.slice(startIndex, ...)` | Tính toán phân trang |
| `task_formhandle` | `const [form, setForm] = useState({...})` | Xử lý form với handleChange |

---

### `ex_` — Exercise Templates (Full component)

| Prefix | Output | Description |
|---|---|---|
| `ex_todo_reducer` | Component todo CRUD | Todo list dùng `useReducer` (ADD / TOGGLE / DELETE) |
| `ex_theme` | Component theme toggle | Theme Manager dùng `Context API` (light/dark mode) |
| `ex_cart` | Component shopping cart | Shopping cart dùng `Context + useReducer` + localStorage |
| `ex_fetch_users` | Component fetch users | Fetch danh sách users từ API có loading / error state |
| `ex_search_filter` | Component search & filter | Lọc danh sách users theo từ khóa dùng `useState` |
| `ex_counter_state` | Component counter state object | Counter dùng `useState` với object `{ count, step }` |
| `ex_counter_reducer` | Component counter reducer | Counter dùng `useReducer` với action `inc/dec/reset/setStep` |
| `ex_memo_demo` | Component React.memo demo | Minh họa tránh re-render không cần thiết với `React.memo` |
| `ex_todo_performance` | Component todo + perf | Todo CRUD với `memo` + `useCallback` tối ưu re-render (local state) |
| `ex_todo_performance_api` | Component todo + perf + API | Todo CRUD với `memo` + `useCallback` + gọi MockAPI thực tế |
| `ex_usememo_search` | Component useMemo + fetch users | Tìm kiếm users với `useMemo` và custom hook |
| `ex_stopwatch` | Component đồng hồ bấm giờ | Stopwatch dùng `useState` + `useRef` + `useEffect` có ghi lap |

---

### `rcc_` — Render Optimization Demos

| Prefix | Output | Description |
|---|---|---|
| `rcc_usecallback_demo` | Component `useCallback` + `memo` | Demo chống re-render dư thừa bằng `useCallback` |

---

## Usage

Gõ prefix vào file `.jsx` / `.tsx` và nhấn **Tab** để tạo code:

```
hook_usestate              → const [state, setState] = useState(null)
hook_useeffect             → useEffect với cleanup và dependency
hook_useref_focus          → useRef tự động focus input khi mount
hook_useRef_ex             → full component demo useRef + focus
hook_useMemo_filter        → useMemo lọc danh sách tối ưu
hook_useEffect_debounce    → debounce search 500ms với useEffect
hook_usereducer            → skeleton reducer + dispatch
hook_custom                → custom hook template
hook_useCounter            → custom hook counter (inc/dec/reset)
hook_fetch_users           → custom hook fetch users + loading/error

router_layout         → createBrowserRouter full setup
route_dashboard       → Dashboard với Link + Outlet

task_rfc              → React Functional Component
task_fetchapi         → async fetch với try/catch
task_formhandle       → form state + handleChange
task_pagination       → logic tính currentItems

ex_todo_reducer           → Bài tập Todo với useReducer
ex_theme                  → Bài tập Theme với Context API
ex_cart                   → Bài tập Shopping Cart (Context + Reducer)
ex_fetch_users            → Bài tập Fetch API có loading/error
ex_search_filter          → Bài tập Search & Filter danh sách
ex_counter_state          → Bài tập Counter bằng useState object
ex_counter_reducer        → Bài tập Counter bằng useReducer
ex_memo_demo              → Bài tập React.memo tránh re-render dư
ex_todo_performance       → Bài tập Todo tối ưu hiệu năng (local)
ex_todo_performance_api   → Bài tập Todo tối ưu + CRUD thực với MockAPI
ex_usememo_search         → Bài tập Search users với useMemo
ex_stopwatch              → Bài tập Đồng hồ bấm giờ (useRef interval)

rcc_usecallback_demo      → Demo useCallback + memo tối ưu render
```