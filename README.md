# Uside React Snippets

This extension provides useful React snippets for JavaScript React developers.

## Features

Snippets are organized by prefix group:
Current set includes **36 snippet prefixes**.

---

### `hook_` — React Hooks

| Prefix | Output | Description |
|---|---|---|
| `hook_usestate` | `const [state, setState] = useState(null)` | React useState hook |
| `hook_useeffect` | `useEffect(() => { ... }, [deps])` | React useEffect hook |
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
| `ex_userposts_searchfilter_memo` | Component user posts filter (memo) | Search + filter users/posts tối ưu với `useMemo` |
| `ex_userposts_test` | RTL test suite template | Mẫu test với Jest + React Testing Library |
| `ex_restaurant` | Component restaurant search/filter | Search + filter nhà hàng với `useMemo` + `useCallback` + `useRef` |
| `ex_restaurant_components` | Optimized restaurant app | Tách component + tối ưu render bằng `memo` + hooks |

---

### `rcc_` — Render Optimization Demos

| Prefix | Output | Description |
|---|---|---|
| `rcc_usecallback_demo` | Component `useCallback` + `memo` | Demo chống re-render dư thừa bằng `useCallback` |

---

### `user_` — User Posts Templates

| Prefix | Output | Description |
|---|---|---|
| `user_posts_filter_search` | Component user posts search/filter | Search + filter user posts bằng `useEffect` |

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
ex_userposts_searchfilter_memo → User posts search + filter tối ưu bằng useMemo
ex_userposts_test         → Template test UserPosts với Jest + RTL
ex_restaurant             → Restaurant search/filter với useMemo + useCallback + useRef
ex_restaurant_components  → Optimized restaurant app (memo + hooks)

rcc_usecallback_demo      → Demo useCallback + memo tối ưu render
user_posts_filter_search  → User posts filter + search với useEffect
```

---

# Jest & React Testing Library Setup Guide

Hướng dẫn hoàn chỉnh cài đặt và sử dụng Jest + React Testing Library để test React components.

---

## 📋 Table of Contents
1. [Cài đặt Dependencies](#cài-đặt-dependencies)
2. [Cấu hình Files](#cấu-hình-files)
3. [Package.json Scripts](#packagejson-scripts)
4. [Cấu trúc Folder](#cấu-trúc-folder)
5. [Viết Test Đầu Tiên](#viết-test-đầu-tiên)
6. [Testing Patterns](#testing-patterns)
7. [Chạy Tests](#chạy-tests)

---

## 📦 Cài đặt Dependencies

### Step 1: Cài Jest & Testing Library

```bash
npm install --save-dev \
	jest \
	@testing-library/react \
	@testing-library/jest-dom \
	@testing-library/user-event \
	babel-jest \
	@babel/preset-env \
	@babel/preset-react \
	jest-environment-jsdom \
	identity-obj-proxy
```

**Giải thích:**
- `jest` - Testing framework chính
- `@testing-library/react` - Utilities để test React components
- `@testing-library/jest-dom` - Custom matchers cho DOM
- `@testing-library/user-event` - Simulate user interactions
- `babel-jest` - Transform JSX/ES6 cho Jest
- `@babel/preset-env` & `@babel/preset-react` - Babel configs
- `jest-environment-jsdom` - DOM environment for tests

---

## ⚙️ Cấu hình Files

### 1. **jest.config.js** - Jest Configuration

```javascript
export default {
	testEnvironment: 'jsdom',
	roots: ['<rootDir>/src'],
	testMatch: ['**/?(*.)+(spec|test).{js,jsx}'],
	moduleFileExtensions: ['js', 'jsx', 'json'],
	transform: {
		'^.+\\.(js|jsx)$': 'babel-jest',
	},
	setupFilesAfterEnv: ['<rootDir>/jest.setup.js'],
	moduleNameMapper: {
		'\\.(css|less|scss|sass)$': 'identity-obj-proxy',
	},
};
```

**Giải thích:**
- `testEnvironment: 'jsdom'` - Sử dụng DOM giống như browser
- `roots: ['<rootDir>/src']` - Chỉ test files trong src/
- `testMatch` - Pattern để tìm test files (*.test.js, *.spec.js)
- `transform` - Transform JSX & ES6 sang JS
- `setupFilesAfterEnv` - Chạy setup file trước mỗi test
- `moduleNameMapper` - Mock CSS imports

---

### 2. **jest.setup.js** - Setup File

```javascript
import '@testing-library/jest-dom';

// Mock global fetch
global.fetch = jest.fn();

// Mock window.matchMedia
Object.defineProperty(window, 'matchMedia', {
	writable: true,
	value: jest.fn().mockImplementation(query => ({
		matches: false,
		media: query,
		onchange: null,
		addListener: jest.fn(),
		removeListener: jest.fn(),
		addEventListener: jest.fn(),
		removeEventListener: jest.fn(),
		dispatchEvent: jest.fn(),
	})),
});

// Clear mocks sau mỗi test
afterEach(() => {
	jest.clearAllMocks();
});
```

**Chứa:**
- Import jest-dom matchers
- Global mocks (fetch, matchMedia)
- Cleanup sau mỗi test

---

### 3. **babel.config.js** - Babel Configuration

```javascript
export default {
	presets: [
		['@babel/preset-env', { targets: { node: 'current' } }],
		['@babel/preset-react', { runtime: 'automatic' }],
	],
};
```

**Cho phép:**
- Transform JSX sang React calls
- Support modern JavaScript

---

## 📝 Package.json Scripts

Thêm vào `package.json`:

```json
{
	"scripts": {
		"dev": "vite",
		"build": "vite build",
		"lint": "eslint .",
		"preview": "vite preview",
		"test": "jest",
		"test:watch": "jest --watch",
		"test:coverage": "jest --coverage"
	}
}
```

**Scripts:**
- `npm test` - Chạy tất cả tests một lần
- `npm run test:watch` - Watch mode (tự động chạy lại)
- `npm run test:coverage` - Coverage report

---

## 📂 Cấu trúc Folder

```text
project/
├── src/
│   ├── components/
│   │   ├── UserCard.jsx
│   │   ├── UserCard.test.jsx        ← Test file
│   │   ├── UserList.jsx
│   │   └── UserList.test.jsx        ← Test file
│   └── hooks/
│       ├── useFetchUsers.js
│       └── useFetchUsers.test.js    ← Test file
├── babel.config.js
├── jest.config.js
├── jest.setup.js
└── package.json
```

**Convention:**
- Test files cùng folder với component
- Đặt tên: `ComponentName.test.jsx`

---

## 🧪 Viết Test Đầu Tiên

### Ví dụ 1: Component Đơn Giản

**Component:** `UserCard.jsx`
```jsx
function UserCard({ user }) {
	return (
		<div>
			<h3>{user.name}</h3>
			<p>{user.email}</p>
		</div>
	);
}
export default UserCard;
```

**Test:** `UserCard.test.jsx`
```jsx
import { render, screen } from '@testing-library/react';
import UserCard from './UserCard';

describe('UserCard', () => {
	test('renders user name and email', () => {
		const mockUser = { name: 'John Doe', email: 'john@test.com' };

		render(<UserCard user={mockUser} />);

		expect(screen.getByText('John Doe')).toBeInTheDocument();
		expect(screen.getByText('john@test.com')).toBeInTheDocument();
	});
});
```

---

### Ví dụ 2: Component với Fetch

**Component:** `UserList.jsx`
```jsx
import { useEffect, useState } from 'react';

function UserList() {
	const [users, setUsers] = useState([]);
	const [loading, setLoading] = useState(true);

	useEffect(() => {
		fetch('/api/users')
			.then(res => res.json())
			.then(data => {
				setUsers(data);
				setLoading(false);
			});
	}, []);

	if (loading) return <div>Loading...</div>;
	return <div>{users.map(u => <p key={u.id}>{u.name}</p>)}</div>;
}
export default UserList;
```

```jsx
import { render, screen, waitFor } from "@testing-library/react";
import App from "./App";

const mockRes = [
  {
    id: 1,
    name: "Pizza House",
    cuisine: "Italian",
    rating: 4.5,
    priceRange: "$$",
    status: "open",
    image: ""
  },
  {
    id: 2,
    name: "Sushi World",
    cuisine: "Japanese",
    rating: 4.8,
    priceRange: "$$$",
    status: "closed",
    image: ""
  },
];

describe("Products", () => {
  beforeEach(() => {
    global.fetch = jest.fn(); // ✅ quan trọng
  });

  test("renders loading then products", async () => {
    global.fetch.mockResolvedValueOnce({
      ok: true, // ✅ quan trọng
      json: async () => mockRes,
    });

    render(<App />);

    expect(screen.getByText("Loading restaurants...")).toBeInTheDocument();

    await waitFor(() => {
      expect(screen.getByText("Pizza House")).toBeInTheDocument();
      expect(screen.getByText("Sushi World")).toBeInTheDocument();
    });
  });
});
```

**Test:** `UserList.test.jsx`
```jsx
import { render, screen, waitFor } from '@testing-library/react';
import UserList from './UserList';

const mockUsers = [
	{ id: 1, name: 'Alice' },
	{ id: 2, name: 'Bob' },
];

describe('UserList', () => {
	beforeEach(() => {
		global.fetch.mockClear();
	});

	test('renders loading then users', async () => {
		global.fetch.mockResolvedValueOnce({
			json: async () => mockUsers,
		});

		render(<UserList />);

		expect(screen.getByText('Loading...')).toBeInTheDocument();

		await waitFor(() => {
			expect(screen.getByText('Alice')).toBeInTheDocument();
			expect(screen.getByText('Bob')).toBeInTheDocument();
		});
	});
});
```

---

### Ví dụ 3: Component với Custom Hook

**Hook:** `useFetchUsers.js`
```jsx
import { useEffect, useState } from 'react';

function useFetchUsers() {
	const [users, setUsers] = useState([]);
	const [loading, setLoading] = useState(true);

	useEffect(() => {
		fetch('/api/users')
			.then(res => res.json())
			.then(data => setUsers(data))
			.finally(() => setLoading(false));
	}, []);

	return { users, loading };
}
export default useFetchUsers;
```

**Component:** `UserList.jsx`
```jsx
import useFetchUsers from '../hooks/useFetchUsers';

function UserList() {
	const { users, loading } = useFetchUsers();

	if (loading) return <div>Loading...</div>;
	return <div>{users.map(u => <p key={u.id}>{u.name}</p>)}</div>;
}
export default UserList;
```

**Test:** `UserList.test.jsx` - **QUAN TRỌNG: Mock Hook**
```jsx
import { render, screen } from '@testing-library/react';
import UserList from './UserList';
import useFetchUsers from '../hooks/useFetchUsers';

// ← BẮTBUỘC mock hook
jest.mock('../hooks/useFetchUsers');

const mockUsers = [
	{ id: 1, name: 'Alice' },
	{ id: 2, name: 'Bob' },
];

describe('UserList', () => {
	test('renders users from hook', () => {
		// Mock hook return value
		useFetchUsers.mockReturnValue({
			users: mockUsers,
			loading: false,
		});

		render(<UserList />);

		expect(screen.getByText('Alice')).toBeInTheDocument();
		expect(screen.getByText('Bob')).toBeInTheDocument();
	});

	test('renders loading state', () => {
		useFetchUsers.mockReturnValue({
			users: [],
			loading: true,
		});

		render(<UserList />);
		expect(screen.getByText('Loading...')).toBeInTheDocument();
	});
});
```

---

## 🎯 Testing Patterns

### Mocking Fetch

```javascript
// Success
global.fetch.mockResolvedValueOnce({
	ok: true,
	json: async () => ({ data: 'value' }),
});

// Error
global.fetch.mockResolvedValueOnce({
	ok: false,
	statusText: 'Not Found',
});

// Network Error
global.fetch.mockRejectedValueOnce(new Error('Network error'));
```

### Mocking Custom Hooks

```javascript
// BẮTBUỘC ở đầu file test
jest.mock('../hooks/useMyHook');

// Trong test
useMyHook.mockReturnValue({
	data: mockData,
	loading: false,
});

// Reset mock
useMyHook.mockClear();
```

### Mocking Functions

```javascript
const mockCallback = jest.fn();

// Render with mock
render(<Component onAction={mockCallback} />);

// Verify it was called
expect(mockCallback).toHaveBeenCalled();
expect(mockCallback).toHaveBeenCalledWith('arg1', 'arg2');
expect(mockCallback).toHaveBeenCalledTimes(1);
```

### Query Strategies (Order of Preference)

```javascript
import { render, screen } from '@testing-library/react';

// 1. getByRole (Preferred - Accessibility)
screen.getByRole('button', { name: /submit/i })

// 2. getByLabelText (Forms)
screen.getByLabelText('Email')

// 3. getByPlaceholderText
screen.getByPlaceholderText('Enter email')

// 4. getByText
screen.getByText('Exact text')

// 5. getByTestId (Last Resort)
screen.getByTestId('custom-id')

// Query variants:
// getBy* - Throws if not found, prefer for elements that must exist
// queryBy* - Returns null if not found, prefer for asserting absence
// findBy* - Async, waits for element, prefer for async operations
```

### Async Testing

```javascript
import { waitFor, screen } from '@testing-library/react';

// Wait for element to appear
await waitFor(() => {
	expect(screen.getByText('Loaded')).toBeInTheDocument();
});

// Wait for specific condition
await waitFor(() => {
	expect(mockFetch).toHaveBeenCalled();
}, { timeout: 3000 });

// Using findBy (implicit wait)
const element = await screen.findByText('Async Result');
```

---

## ▶️ Chạy Tests

### Chạy Tất Cả Tests
```bash
npm test
```

### Chạy File Cụ Thể
```bash
npm test -- UserCard.test.jsx
```

### Watch Mode (Recommended Development)
```bash
npm run test:watch
```

### Coverage Report
```bash
npm run test:coverage
```

### Debug Mode
```bash
npm test -- --verbose
```

---

## ✅ Checklist Setup

- [ ] Cài đặt tất cả dependencies
- [ ] Tạo `jest.config.js`
- [ ] Tạo `jest.setup.js`
- [ ] Tạo `babel.config.js`
- [ ] Update `package.json` scripts
- [ ] Tạo first test file
- [ ] Chạy `npm test` thành công

---

## 🚨 Common Issues & Solutions

### Issue 1: "Cannot find module"
**Solution:** Kiểm tra import path, chắc chắn file tồn tại

### Issue 2: "jest is not defined"
**Solution:** Kiểm tra jest.setup.js setup đúng trong jest.config.js

### Issue 3: "fetch is not defined"
**Solution:** Thêm vào jest.setup.js:
```javascript
global.fetch = jest.fn();
```

### Issue 4: "Module not mocked"
**Solution:** Thêm jest.mock() ở đầu test file:
```javascript
jest.mock('../hooks/useMyHook');
```

### Issue 5: Test timeout
**Solution:** Tăng timeout:
```javascript
jest.setTimeout(10000);
```

---

## 📚 Useful Jest Matchers

```javascript
expect(value).toBe(5);                              // Strict equality
expect(value).toEqual({ a: 1 });                    // Deep equality
expect(value).toBeNull();
expect(value).toBeUndefined();
expect(value).toBeTruthy();
expect(value).toBeFalsy();
expect(array).toHaveLength(3);
expect(string).toMatch(/pattern/);
expect(fn).toHaveBeenCalled();
expect(fn).toHaveBeenCalledWith(arg);
expect(element).toBeInTheDocument();                // From jest-dom
expect(element).toHaveClass('className');           // From jest-dom
expect(input).toHaveValue('text');                 // From jest-dom
expect(element).toBeVisible();                      // From jest-dom
expect(element).toBeDisabled();                     // From jest-dom
```

---

## 📖 Tài liệu Tham Khảo

- [Jest Documentation](https://jestjs.io/docs/getting-started)
- [React Testing Library](https://testing-library.com/react)
- [Jest DOM Matchers](https://github.com/testing-library/jest-dom)
- [React Documentation - Testing](https://react.dev/learn/react-testing)

---

**Setup hoàn tất! Giờ bạn sẵn sàng test components. 🚀**