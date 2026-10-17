# React Native + TypeScript Snippets for VS Code

Bộ snippet giúp viết nhanh **React Native + TypeScript (TSX)** trong VS Code, hướng đến các bài thực hành Expo/Snack: giao diện, Hooks, gọi API, FlatList, tìm kiếm/lọc, giỏ hàng và Movie Watchlist.

> **Lưu ý:** Đây là bộ **mẫu code được chèn vào editor**, không phải thư viện React Native, không tự chạy ứng dụng và không thay thế việc cài các dependency trong dự án.

## 1. Yêu cầu

- **VS Code** (phiên bản hiện hành).
- Để **sử dụng snippets:** không cần Node.js, Expo hay Android Studio.
- Để **đóng gói `.vsix`:** cần Node.js + npm và công cụ `@vscode/vsce`.
- Để **chạy đoạn code React Native:** cần một dự án React Native/Expo với dependency tương ứng.

## 2. Cài extension từ file `.vsix`

### Cách 1: Cài qua giao diện VS Code

1. Mở **VS Code**.
2. Nhấn `Cmd + Shift + P` (macOS) hoặc `Ctrl + Shift + P` (Windows/Linux).
3. Gõ **Extensions: Install from VSIX...**.
4. Chọn file `.vsix` đã được build.
5. Mở file `App.tsx`, nhập `rnflatlist` và nhấn `Tab`/`Enter` để kiểm tra.

### Cách 2: Cài qua terminal

```bash
code --install-extension ./ten-extension-1.0.0.vsix
```

> Thay tên file bằng **đúng tên file `.vsix` thực tế**. Nếu lệnh `code` chưa hoạt động trên macOS: mở Command Palette → **Shell Command: Install 'code' command in PATH** (nếu tùy chọn này có sẵn) rồi mở lại terminal.

Cài lại sau khi cập nhật:

```bash
code --install-extension ./ten-extension-1.0.1.vsix --force
```

## 3. Sử dụng snippet trong VS Code

1. Mở một file `.tsx` (khuyến nghị), ví dụ `App.tsx`.
2. Gõ prefix, chẳng hạn `rnfetch` hoặc `rnflatlist`.
3. Chọn gợi ý snippet rồi nhấn `Tab` hoặc `Enter`.
4. Thay các placeholder và biến cho đúng yêu cầu đề bài; nhấn `Tab` để chuyển giữa các điểm cần điền.
5. Nếu không thấy gợi ý, thử `Ctrl + Space` (Trigger Suggest).

Ví dụ:

```text
rnflatlist + Tab  →  sinh khung FlatList
rnsearch + Tab    →  sinh logic tìm kiếm
rncartadd + Tab   →  sinh logic thêm vào giỏ
```

**Phân biệt:** `rnapp`, `rnmoviefull`, `rnmoviecardfull` là mẫu file/khối lớn; không bung chúng vào giữa một component đã có. Các mẫu như `rninput`, `rnfilter` cần đặt đúng vị trí và phải có các import/state cần thiết.

### Dùng với Expo Snack

Website [snack.expo.dev](https://snack.expo.dev/) **không tự cài extension VS Code**. Hãy bung snippet trong VS Code, chỉnh sửa xong rồi copy code sang `App.tsx` hoặc các file tương ứng trên Snack.

`Alert.alert()` chủ yếu hoạt động trên iOS/Android; hành vi trên Snack Web có thể khác. File Jest test có thể được viết trên Snack nhưng Snack không phải môi trường chạy Jest.

## 4. Danh mục prefix hiện có

File `react-native.code-snippets` được kiểm tra chứa **56 snippet**. Danh mục dưới đây phản ánh đúng file đó.

### Khởi tạo và Hooks

| Prefix | Mục đích |
|---|---|
| `rnimport` | Import React Native thường dùng |
| `rnapp` | Khung App cơ bản |
| `rnsafe` | SafeAreaProvider / SafeAreaView |
| `hook_usestate` | State có TypeScript |
| `rnstatearray` | State cho mảng dữ liệu |
| `hook_useeffect` | useEffect khi mount |
| `hook_usememo` | useMemo |
| `hook_usecallback` | useCallback |
| `rnref` | useRef cho TextInput |
| `rnreducer` | useReducer |
| `rncontext` | Context API |
| `rnnavtypes` | Type cho navigation |

### Giao diện React Native

| Prefix | Mục đích |
|---|---|
| `rnview` | View + Text |
| `rnrow` | Bố cục hàng ngang |
| `rncenter` | Căn giữa |
| `rninput` | TextInput |
| `rnbutton` | Pressable |
| `rnswitch` | Switch |
| `rnimage` | Image từ URL |
| `rnflatlist` | FlatList có type |
| `rngrid` | Chuyển List/Grid |
| `rnempty` | ListEmptyComponent |
| `rnstyles` | StyleSheet |
| `rncard` | Card component có memo |

### API, danh sách, sự kiện

| Prefix | Mục đích |
|---|---|
| `rnfetch` | GET API + loading/error |
| `rnfetchfn` | Hàm fetch cơ bản |
| `rnloadingui` | UI loading/error/retry |
| `rnrefresh` | Pull to refresh |
| `rnalert` | Alert xem chi tiết |
| `rnconfirm` | Alert xác nhận xóa |
| `rnadd` | Thêm item vào state |
| `rndelete` | Xóa item khỏi state |
| `rntoggle` | Đổi trạng thái item |
| `rnsearch` | Tìm kiếm |
| `rnfilter` | Lọc boolean |
| `rnsearchfilter` | Kết hợp search + filter |
| `rnpagination` | Phân trang local |
| `rnform` | State form |
| `rntype` | TypeScript item type |
| `rncallbackdetail` | useCallback xem chi tiết |
| `rncallbackdelete` | useCallback xóa |
| `rnpost` | HTTP POST |
| `rnapidelete` | HTTP DELETE |
| `rnpatch` | HTTP PATCH |

### Giỏ hàng và bài Movie

| Prefix | Mục đích |
|---|---|
| `rncarttype` | Kiểu Product, CartItem |
| `rncartstate` | State giỏ hàng |
| `rncartadd` | Thêm/trùng thì tăng số lượng |
| `rncartinc` | Tăng số lượng |
| `rncartdec` | Giảm số lượng |
| `rncartremove` | Xóa khỏi giỏ |
| `rncarttotal` | Tổng số lượng/tổng tiền |
| `rncartrow` | Một dòng giỏ hàng |
| `rncartapp` | Mẫu màn hình giỏ hàng |
| `rnmovie` | Khung bài Movie Watchlist |
| `rnmoviefull` | App.tsx Movie + API + Search + Cart |
| `rnmoviecardfull` | MovieCard.tsx tương ứng |

### Jest test (mẫu bổ sung riêng)

Prefix `rntestcard` đã được cung cấp dưới dạng JSON trong cuộc trò chuyện, nhưng **chưa có trong file 56 snippets hiện tại**. Muốn dùng trong bản phát hành, cần dán snippet đó vào file nguồn của extension trước khi build. Mẫu này kiểm thử render, `layout="row"/"tile"`, `isShowing` và `fireEvent.press` theo **component MovieCard của đề test**, không khớp tự động với MovieCard cũ dùng `gridMode` và `onDetail`.

## 5. Cấu trúc dự án extension để build `.vsix`

Nếu hiện bạn mới có **một file** `react-native.code-snippets` (User Snippets), thì **chưa thể** dùng `vsce package` trực tiếp. Hãy tạo cấu trúc extension như sau:

```text
react-native-snippets-extension/
├── package.json
├── README.md
├── snippets/
│   └── react-native.code-snippets
└── .vscodeignore        # tùy chọn
```

Chép file snippet hiện tại vào `snippets/react-native.code-snippets` và tạo `package.json` mẫu:

```json
{
  "name": "react-native-exam-snippets",
  "displayName": "React Native Exam Snippets",
  "description": "React Native and TypeScript snippets for Expo practice",
  "version": "1.0.0",
  "publisher": "your-publisher-id",
  "engines": {
    "vscode": "^1.85.0"
  },
  "categories": ["Snippets"],
  "contributes": {
    "snippets": [
      {
        "language": "typescriptreact",
        "path": "./snippets/react-native.code-snippets"
      },
      {
        "language": "javascriptreact",
        "path": "./snippets/react-native.code-snippets"
      }
    ]
  }
}
```

**Giải thích:** `typescriptreact` áp dụng cho `.tsx`, `javascriptreact` cho `.jsx`. Các đoạn có `type`, generic TypeScript và annotation chỉ có thể dùng đúng trong `.tsx` nếu chưa điều chỉnh. `your-publisher-id` là ví dụ: thay bằng publisher ID của bạn nếu dự định công bố extension; không dùng nhầm ID của người khác.

Nếu extension của bạn **đã có `package.json`**, hãy giữ các trường đang dùng và đảm bảo `contributes.snippets` trỏ đến **đường dẫn file thực tế**, không thay toàn bộ package tùy tiện.

## 6. Build extension thành `.vsix`

Mở terminal **tại thư mục gốc có `package.json`**:

```bash
npm install -g @vscode/vsce
vsce package
```

Hoặc không cần cài global:

```bash
npx @vscode/vsce package
```

Khi thành công, thư mục sẽ xuất hiện một file tương tự:

```text
react-native-exam-snippets-1.0.0.vsix
```

> Đây là **ví dụ**; tên thật lấy từ `name` + `version` trong `package.json`. Nếu công cụ hỏi về publisher, license, README, repository hay cảnh báo khi đóng gói, hãy đọc cảnh báo và bổ sung metadata hoặc xử lý theo đúng dự án, không tự tắt kiểm tra bảo mật để build cho qua.

### Kiểm tra nội dung gói

```bash
vsce ls
```

Kiểm tra `snippets/react-native.code-snippets`, `package.json`, `README.md` có được đưa vào gói. Sau đó cài file `.vsix` vào VS Code và thử prefix.

### Đóng gói phiên bản mới

1. Sửa file JSON snippet.
2. Đảm bảo JSON hợp lệ.
3. Tăng `version` trong `package.json`, ví dụ từ `1.0.0` thành `1.0.1`.
4. Chạy lại `vsce package`.
5. Cài `.vsix` mới và test.

Không cần chạy `expo build` hay `eas build`: đó là lệnh build **ứng dụng mobile**, không phải đóng gói VS Code extension.

## 7. Kiểm tra JSON snippet trước khi build

Chạy ở thư mục extension:

```bash
node -e "const fs=require('fs'); const p='snippets/react-native.code-snippets'; const data=JSON.parse(fs.readFileSync(p,'utf8')); console.log('Valid JSON:',Object.keys(data).length,'snippets');"
```

Nếu file có comment kiểu JSONC, lệnh `JSON.parse` không hỗ trợ comment; hãy dùng cấu trúc JSON thuần hoặc kiểm tra trong VS Code trước khi đóng gói.

**Thêm snippet mới**: đặt một object cùng cấp với các snippet hiện có, thêm dấu phẩy giữa các object và đảm bảo không trùng key. Prefix có thể khác key, nhưng nên ngắn và dễ nhớ.

## 8. Cách kiểm tra extension sau khi cài

- Mở file `App.tsx` → gõ `rnflatlist`, `rnfetch` hoặc `rnsearch` → gợi ý phải xuất hiện.
- Gõ `rnmoviefull` trong file `.tsx` rỗng → sinh khung `App.tsx`.
- Tạo `components/MovieCard.tsx` → gõ `rnmoviecardfull` → sinh component.
- Kiểm tra đường dẫn import giữa hai file.
- Nếu đã tự thêm `rntestcard`, gõ prefix trong `__tests__/MovieCard.test.tsx` để kiểm tra.
- Mở lại file `.tsx`, dùng `Ctrl + Space` nếu IntelliSense chưa tự bật.

## 9. Sửa lỗi thường gặp

| Hiện tượng | Cách xử lý |
|---|---|
| `vsce: command not found` | Dùng `npx @vscode/vsce package` hoặc cài `@vscode/vsce` global |
| Không có `package.json` | Bạn đang ở sai thư mục hoặc mới chỉ có User Snippets; tạo extension như mục 5 |
| `Missing publisher` / cảnh báo metadata | Bổ sung trường `publisher` và các metadata theo thông báo; không tự nhận publisher người khác |
| Extension cài được nhưng không thấy snippets | Kiểm tra `contributes.snippets.path`, loại file `.tsx` và thử `Ctrl + Space` |
| Prefix không xuất hiện trong VSIX mới | Xác nhận đã thêm vào **file được đóng gói**, tăng version và cài lại VSIX |
| Gõ `React.memo` báo `React doesn't exist` | `import React from 'react'` hoặc dùng `import { memo } from 'react'` rồi gọi `memo(...)` |
| Code web báo lỗi với React Native | Không dùng `div`, `input`, `button`, `document`, `localStorage` như trong ReactDOM |
| `Alert.alert()` không mở trên Snack Web | Thử trên iOS/Android; môi trường Web không hỗ trợ như native |
| Fetch API lỗi | Kiểm tra URL, quyền truy cập mạng, trạng thái `res.ok`, cấu trúc JSON trả về |
| `FlatList` đổi cột lỗi | Dùng `key={gridMode ? 'grid' : 'list'}` cùng `numColumns` |
| `rntestcard` không chạy trong Snack | Jest chạy trong môi trường test đã cấu hình, không chạy trực tiếp trong Snack |

## 10. Lưu ý khi dùng cho bài thi

- Đọc kỹ đề, đặc biệt **tên field**, **props**, **API URL** và **định dạng dữ liệu**.
- Snippet là khung tham khảo; không đảm bảo khớp mọi đề. Ví dụ `MovieCard` có thể dùng `layout`, `genre`, `isShowing`, `onSelect`, khác với phiên bản `gridMode`/`onDetail`/`onAddToCart`.
- `rnmoviefull` dùng giỏ hàng local với **giá giả định 100.000đ/phim**, không phải flow thanh toán thật.
- Thêm/xóa movie trong ví dụ là **state local**; pull-to-refresh sẽ tải lại API.
- File test Jest phải tương ứng với component thực tế và cấu hình test khi có môi trường chạy.
- **Chỉ sử dụng snippets/extension trong giờ thi nếu được giảng viên cho phép**.

## 11. Quy trình ngắn gọn

```text
Sửa snippets JSON
    ↓
Kiểm tra JSON và prefix
    ↓
Tăng package.json version
    ↓
npx @vscode/vsce package
    ↓
Cài .vsix vào VS Code
    ↓
Mở .tsx → gõ prefix → Tab
    ↓
Kiểm tra code sinh ra, sửa theo đề
```

---

**Phân biệt hai việc:** `vsce package` → build **VS Code extension (.vsix)**; `eas build` → build **ứng dụng Expo (.apk/.aab/.ipa)**. Đây là hai quy trình độc lập.


## Custom Hook fetch data (mới)

Bộ snippet hiện có **58 mẫu** (thêm 2 mẫu):

| Prefix | Nơi dùng | Chức năng |
| --- | --- | --- |
| `rnusefetch` | `hooks/useFetch.ts` | Tạo generic hook `useFetch<T>(url)` trả về `data`, `loading`, `error`, `refetch`; có AbortController hủy request khi unmount |
| `rnusefetchuse` | `App.tsx` | Mẫu gọi `useFetch<Movie[]>(API_URL)` và hiển thị FlatList, loading, retry |

**Cách dùng:** Tạo thư mục `hooks`, tạo file `useFetch.ts`, gõ `rnusefetch` rồi Tab. Trong `App.tsx`, gõ `rnusefetchuse` ở file thử nghiệm và thay `API_URL`, `Movie` theo đề. Không dán nguyên App mẫu vào App đang có vì sẽ trùng `export default`.

**Lưu ý:** Hook trả về dữ liệu từ API. Nếu bài tập cần thêm/xóa/sửa local, hãy dùng state riêng hoặc mở rộng hook; không gán trực tiếp vào biến `data`. `refetch` sẽ lấy lại dữ liệu từ server.
