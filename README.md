# React Native + TypeScript Snippets cho VS Code

File: `react-native.code-snippets` (45 snippets). Được biên soạn từ bộ 57 ReactJS snippets do bạn cung cấp, chọn các mẫu hữu ích cho buổi thực hành React Native và viết lại cho `App.tsx` trên Expo Snack.

## Cài đặt

1. VS Code → **Code → Settings → Configure User Snippets** (macOS; trên Windows/Linux dùng File → Preferences → Configure User Snippets).
2. Chọn **New Global Snippets file...**, đặt tên `react-native`, hoặc tạo file `react-native.code-snippets` trong `.vscode/` của project.
3. Dán toàn bộ nội dung file được cung cấp vào, lưu. Nếu tạo file Global Snippets, bạn cũng có thể mở file qua **Configure User Snippets** và dán đè.
4. Mở file `.tsx` rồi gõ prefix như `rnflatlist`, chọn gợi ý và bấm Tab/Enter. Nhấn Tab để di chuyển qua các điểm cần điền. Nếu gợi ý không hiện, thử `Ctrl+Space`.
5. Muốn dùng trên Snack: snippets tự bung trong VS Code, sau đó **copy code đã bung** vào Snack; website Snack không tự đọc VS Code snippets.

## Prefix đáng nhớ

- `rnapp` App.tsx cơ bản; `rnsafe` SafeArea; `rnstyles` StyleSheet; `rnimport` các import thông dụng.
- `hook_usestate`, `hook_useeffect`, `hook_usememo`, `hook_usecallback`, `rnstatearray`.
- `rninput`, `rnbutton`, `rnswitch`, `rnimage`, `rnflatlist`, `rngrid`, `rnempty`.
- `rnfetch` GET + loading/error; `rnrefresh` pull refresh; `rnloadingui` Retry; `rnmovie` starter Movie Watchlist.
- `rnsearch`, `rnfilter`, `rnsearchfilter`, `rncard`, `rnconfirm`, `rnalert`.
- `rnpost`, `rnapidelete`, `rnpatch` là các mẫu cập nhật server; `rnadd`, `rndelete`, `rntoggle` chỉ đổi state tại máy.
- `rnref`, `rnreducer`, `rncontext`, `rnnavtypes` cho các chủ đề bổ sung.

## Lưu ý

- Các snippet ngắn là **mảnh code**, phải đặt đúng bên trong `App()` hay JSX và bổ sung import/type tương ứng. Các snippet đầy đủ (`rnapp`, `rnmovie`) là các ví dụ file độc lập, không dán chồng lên App đã có.
- `Alert.alert()` hướng đến native iOS/Android; Snack Web không bảo đảm hỗ trợ.
- `rnmovie` là **khung GET + FlatList**, không thay thế việc tự làm đủ các câu của đề Movie Watchlist.
- Khi dùng `rnfetch`, nếu đề bài cho sẵn `API_URL` và `fetchMovies()` bắt buộc giữ nguyên, đừng thay/xóa hai phần đó; chỉ dùng phần state/loading/retry phù hợp.
- `rnpost`, `rnapidelete`, `rnpatch` yêu cầu URL đúng và backend hỗ trợ phương thức HTTP tương ứng.
- Bộ snippet không phụ thuộc React DOM (`div`, `button`, `input`, `window`, `localStorage`) hoặc React Router.
- Snippets giúp tra và gõ nhanh khi luyện tập; hãy kiểm tra quy định phòng thi trước khi dùng extension/tài liệu số trong giờ thi.


## Bổ sung: Giỏ hàng React Native

Các prefix mới: `rncarttype`, `rncartstate`, `rncartadd`, `rncartinc`, `rncartdec`, `rncartremove`, `rncarttotal`, `rncartrow`, `rncartapp`.

- `rncartadd`: thêm sản phẩm mới, hoặc tăng `quantity` nếu sản phẩm đã tồn tại.
- `rncartdec`: giảm số lượng và tự xóa sản phẩm khi số lượng về 0.
- `rncarttotal`: tổng số lượng và tổng tiền bằng `reduce()` + `useMemo()`.
- `rncartapp`: bài mẫu độc lập dùng React Native + TypeScript, có danh sách sản phẩm và giỏ hàng.

**Lưu ý:** Các snippet độc lập như `rncartadd` giả định bạn đã khai báo `Product`, `CartItem` và `const [cart, setCart] = useState<CartItem[]>([])`. Prefix `rncartapp` là mẫu chạy đầy đủ.


## Movie Watchlist + Cart (bổ sung)

- `rnmoviefull`: toàn bộ `App.tsx`, gồm Fetch API, Loading/Retry, Search/Filter, List/Grid, Pull-to-refresh, thêm/xóa phim, giỏ hàng, tăng/giảm/xóa, tổng tiền cố định 100.000đ/phim.
- `rnmoviecardfull`: toàn bộ `components/MovieCard.tsx`, gồm `memo`, poster, chi tiết, nút thêm vào giỏ và xóa phim.

Đặt `App.tsx` ở thư mục gốc và tạo `components/MovieCard.tsx` cùng cấp theo đường dẫn import. Hai snippet được thiết kế để sử dụng cùng nhau. Trên Snack, bung snippet trong VS Code rồi copy sang đúng file. Giá mỗi phim cố định 100.000đ để luyện giỏ hàng, add/delete Movie là state local.
