1. cùng cấp ./
2. truy xuất ra ngoài 1 cấp ../
3. css nó sẽ chạy từ trên xuống dưới, nếu có 2 đoạn code cùng thực hiện 1 chức năng thì nó sẽ ưu tiên đoạn code ở dưới
4. div là thẻ block, có độ rộng 100% phần tử chứa nó, lưu ý: chưa nói tới vấn đề khi sử dụng với CSS.
5. div thường dùng rất nhìu khi chia layout, gom 1 khối nào đó
6. image là thẻ inline, thẻ tự đóng ( inline là css trực tiếp vào thẻ ), dùng để hiển thị hình ảnh với 2 thuộc tính là 'src' và 'alt'
7. alt viết tắt của 'alternate text' nó dùng trong việc SEO, khi hình ảnh bị lỗi hoặc sai đường link thì alt sẽ hiển thị để người dùng biết hình ảnh nói về gì
8. span là thẻ inline thường dùng cho những đoạn chữ ngắn
9. class là thuộc tính dùng để sử dụng các class cho thẻ, sau đó dùng style trong CSS
10. thẻ tiêu đề : h1 đến h6
11. h1: mỗi page chỉ có tối đa 1 thẻ h1, thẻ này thường được dùng cho những tiêu đề lớn của trang
12. h2 dùng được nhìu, thường được dùng cho những block to
13. h3 dùng được nhìu, thường đc dùng cho những block nhỏ
14. h4,h5,h6; tương ứng cho những tiêu đề nhỏ hơn
15. thẻ a : là thẻ inline, chắc chắn dùng cho liên kết, nó có 3 thuộc tính hay dùng _'href', 'target', và 'rel'_
16. khi dùng target có giá trị là \_blank thì thẻ a nên thêm thuộc tính rel = "noopener noreferrer",để tránh web load ở new tab nặng dẫn đến web chính load nặng theo ( đây là vấn đề bảo mật mà chrome đề xuất để fix lỗi này)
17. fonts chữ:+ sẽ có sẵn ở google fonts + ko có ở google fonts mà được mua, tải trên mạng về máy
18. font-weight độ đậm nhạt của chữ ( 100 -> 900), normal, bold, bolder, extra-bol, light, tin, regular, medium, semibold
19. font-family : thiết lập font chữ, truyền vào là font name (tên của font chữ)

- "sans-serif" : chữ ko có chân
- "serif" : chữ có chân

* CSS Selectors : tag, class, id, attribute

- tags : h1,h2,h3, div, body, span, a
- class: .name, .tour,.tour-header
- Id : #header, #content
- attributes : nói sau
- special selector: \*

---------------------- cấu trúc 1 đoạn code CSS --------------------

- cssSelectors, cssSelectors, cssSelectors{
  property: value
  }
  ex:
  h1,.name,#header,input[Type='email']{
  font-family: 'Inter'
  }

* _user agent stylesheet_ : CSS mặc định của trình duyệt, mỗi trình duyệt sẽ có CSS mặc định
* _CSS reset_ : dùng để reset CSS mặc định của các trình duyệt, và bắt buộc phải có đầu tiên

* color : màu chữ
* background-color : màu nền
* mã màu: hexa(#ffa400)

* box-sizing:

  - _content-box_: độ rộng lúc này của 1 khối sẽ bằng width + padding[left + right] + border[left + right]
  - _border-box_ : độ rộng lúc này của 1 khối sẽ bao gồm padding và border, nên áp dụng cho toàn bộ selector(\*)

* border : viền (khoảng cách giữa các phần tử trong 1 ko gian)

* padding : khoảng không gian xung quanh 1 đối tượng trong box

* khi tăng size của padding lớn hơn width và height thì width, height = 0

* box-sizing bao gồm padding khi chúng ta xét width và height cố định

* đơn vi: px,em,rem, vw, vh,%

* margin : là khoảng cách giữa phần tử này với phần tử khác ko ảnh hưởng tới chìu cao của phần tử đang xét như padding

* text-decoration: gạch dưới của thẻ a (none: ko có gạch dưới, underline : gạch dưới, overline: gạch trên đầu, line-through : gạch ngang)

* border-radius : độ bo góc của khối, càng lớn thì càng bo góc, nếu hình vuông mà có bo góc lớn thì sẽ tạo ra hình tròn, nếu là hình chữ nhật có bo góc lớn thì sẽ tạo ra hình

- _border-top-left-radius_
- _border-top-right-radius_
- _border-bottom-left-radius_
- _border-bottom-right-radius_

* _line-height_: khoảng cách giữa các dòng

* khi thẻ inline nằm canh nhau thì nó sẽ nằm trên 1 hàng, ngược lại thẻ block thì nó sẽ tạo ra hàng mới

* display: block, inline, inline-block, none, flex, grid

- inline: biến thành thẻ inline, nó sẽ bị hạn chế vài thuộc tính CSS liên quan tới box-sizing như là padding-top, padding-bottom,margin-top, margin-bottom

- block: biến thành thẻ block

- inline-block: biến thành thẻ inline-block, là sự kết hợp giữa inline và block, khi các thẻ có thuộc tính inline-block nó sẽ kế thừa đặc tính của inline tức là nằm cạnh nhau thì sẽ nằm trên 1 hàng, có độ rộng = nội dung mà nó chứa, ko bị hạn chế css

- none: ẩn luôn, ko thấy ko nhấn được

* flex: dùng rất nhìu hiện nay, nếu master được nó thì code layout vô tư lol

* font-weight thiết lập độ dày, mỏng của chữ trong HTML CSS

* _overflow_ : hidden" : xử lý những thứ bị tràn ra ngoài và cut nó đi nhưng cách giải quyết tốt nhất để tránh xung đột vs những thứ xung quanh ta dùng border-radius

* _padding_ : ko thể dùng số âm
* _margin_ : có thể dùng số âm, có giá trị "auto"

* "min-width": độ rộng tối thiểu, vd: 1000px -> >= 1000px

* "max-width": độ rộng tối đa, vd: 1000px -> <= 1000px

* flexbox: áp dụng thuộc tính display: flex vào phần tử mình muốn dàn layout

* calc: hàm dùng để tính toán, + - \* / , lưu ý là phải có khoảng cách giữa các phép toán

* thuộc tính trong flex box làm cho độ dài các cột cao bằng nhau là "align-items: stretch"

* "align-items: flex-start": canh phần trên đầu
* "align-items: flex-end": canh phần dưới cùng
* align-items: flex-center": canh giữa
* "align-items: baseline": canh theo đít chữ của dòng chữ đầu tiên

* "flex-direction: colum, row"

* "flex-wrap: nowrap" : ko cho phép rớt xuống hàng
* "flex-wrap: wrap" : cho phep rớt xuống hàng

* component: có thể tái sử dụng và có thể tùy chỉnh 1 chỗ để sử dụng nhiều nơi

* pug:
* sass
* javasript:

* mixins: giống function trong javascript mục đích là tái sử dụng code

* Biến: =, #{biến}

------------------------------- position -------------------------------

position: có 5 giá trị chính: static, relative, absolute, sticky, fixed, khi sử dụng thuộc tính position này thì đi kèm sẽ có các thuộc tính khác như top right bottom left z-index

- relative: khi sử dụng giá trị này phải lưu ý xem phần tử con nó có sử dụng position là absolute hay ko?

- absolute: khi sử dụng giá trị này phải lưu ý xem phần tử chứa nó gần nhất có sử dụng position là absolute hay relative ko?

- sass:

---------------------------- _Responsive_ -----------------------------

- breakpoints : 320px 480px 720px ...

@media screen and (max-width: breakpoints - 1px)

@media screen and (max-width: breakpoints - 0.2px)

@media screen and (min-width: breakpoints) and (max-width: breakpoints)

+++++ _review_ ++++

- display: flex // hien thi tren cung 1 hang
  tai sao no ko rot xuong hang vi flex-wrap : no-wrap la mac dinh

- img{
  display: block; // khắc phục vấn đề j? hình nó sẽ bị 1 khoảng trống ở dưới mặc dù ta ko css cho chúng để khắc phục nó code display: block hoặc code (display : inline-block, vertical-align : middle hoặc là bottom)
  max-width: 100%;
  } css mặc định cho image tránh bị hình tràn ra ngoài đây gọi là behavior của image

- transform : tác động vào vật thể làm cho vật thể to lên dịch chuyền qua trái, phải , méo .. nhưng vị trí vẫn giữ nguyên
  translate(translateX, translateY), skew(X,Y), rotate (rotateX,y,Z), scale(X,Y)

- "translateX" : nếu giá trị là số dương thì nó sẽ di chuyển qua bên phải, ngược lại di chuyển qua trái
- "translateY": nếu gt là số dương thì nó sẽ di chuyển đi xuống, ngược lại di chuyển đi lên

- "value": 10px, 20px, -15px, 10%, lưu ý sử dụng % thì & ở đây chính là độ rộng hoặc chiều cao của khối chúng ta đang áp dụng thuộc tính transform và hàm translate

---- _variables_ ---
KHAI BAO
--primary-color: blue;
--secondary-color: orange;
--font-size-sm: 16px;
--text-color: red;
SU DUNG
var(--font-size-sm)

------------- _PHÂN BIỆT display inline, block, inline-block css_ -----------------

- display: inline

* các phần tử có display inline nằm cạnh nhau sẽ hiển thị trên một hàng ngang
* ko thể tác động vào padding trên dưới của phần tử chỉ trái phải
* thẻ mặc định inline: a, span, b,i ,...

- display: block

* các phần tử display block sẽ chiếm ko gian và nằm 1 mk trên 1 hàng
* có thể tác động trên dưới trái phải
* thẻ mặc định block: div,h1....h6,p,section,...

- display: inline-block

* các phần tử có inline-block khi ở gần nhau sẽ nằm trên 1 hàng
* có thể tác động trên dưới trái phải

- kinh nghiệm áp dụng: khi xây dựng menu nên cho thẻ a inline block để tăng ko gian người dùng có thể nhấp chuột.

------------ _4 cách CĂN GIỮA khối trong html css_ --------------

1. margin: 0px auto
2. dùng display: inline-block cho tk con sau đó _text-align: center_ cho tk cha
3. dùng position: relative cho tk cha và position: absolute cho tk con sau đó dùng top,left: 50%
   transform: translate(-50%,-50%)
4. đi vào khối cha display: flex
   justify-content: center // căn giữa theo chìu ngang
   align-items: center // căn giữa theo chìu dọc

----------------_Grid CSS_--------------------------
display: grid
grid-template-colums: value value value ... n-value
grid-template-colums: 1fr 1fr 1fr 1fr
gird-template-colums: repeat(4,1fr)
gap: 30px

--------------- _Dùng để phủ full hình lên khung tránh bị méo_ ---------------
.popular-img{
width: 100%;
height: 100%;
object-fit: cover;
}
object-fit: cover; // bao phủ hết toàn bộ khung ( hình sẽ cố gắng scale và làm cho hình ko bị méo mó)
object-fit: fill; // thường dùng cho video

---

1. grid: dàn layout cực nhanh
2. time : là thẻ inline
3. each in pug: dùng để duyệt qua danh sách các phần tử trong mảng để hiển thị

4. object-fit: thuộc tính này dùng cho thẻ img hoặc video, mục đích là để hiển thị hình ảnh hoặc video vừa với khung chứa nó hay ko?

5. object-position: dùng để căn chỉnh vị tri hiển thị của img hoặc video khi dùng với thuộc tính object-fit

6. css selectors child: :nth-child(number), :nth-last-child(number),:first-child, :last-child, :not(selectors),những phần tử cùng cấp
7. track-line

---------------------- _Phân biệt_ ---------------

1. _align-items_:

-là thuộc tính dùng để _căn chỉnh các phần tử con theo hướng dọc_ trong một container.
-Nó ảnh hưởng đến việc căn chỉnh các phần tử con riêng lẻ trong container.
-Các giá trị thông thường của _align-items_ bao gồm: _flex-start (mặc định), flex-end, center, stretch, và baseline._

- _align-item: stretch_

được sử dụng để căn chỉnh các phần tử con trong một container flexbox hoặc grid layout sao cho chúng kéo dãn để phù hợp với _chiều cao_ của container. _Nghĩa là các phần tử con sẽ được căn chỉnh để chiếm toàn bộ chiều cao của container trên trục dọc_ (trục chính).

2. _justify-content_:

-là thuộc tính dùng để _căn chỉnh các phần tử con theo hướng ngang_ (trục chéo) của container.
-Nó ảnh hưởng đến việc căn chỉnh các phần tử con theo chiều ngang trong container.
-Các giá trị thông thường của justify-content bao gồm: _flex-start (mặc định), flex-end, center, space-between, space-around, và space-evenly._

3. _align-content_:

-là thuộc tính dùng để _căn chỉnh toàn bộ nhóm các phần tử con trong một container flexbox hoặc grid layout_.
-Nó ảnh hưởng đến khoảng cách giữa các dòng (hoặc hàng) của phần tử con, không phải là căn chỉnh từng phần tử con.
-Các giá trị thông thường của align-content bao gồm: _flex-start, flex-end, center, space-between, space-around, và stretch._

*https://topdev.vn/blog/su-dung-bo-cuc-trang-flexbox-trong-css/*

------ new knowledge --------------------------

1. _width: fit-content_: có độ rộng = vs nội dung nó chứa

2. _margin-inline_ : tương ứng margin-left và margin-right

3. _padding-inline_ : tương ứng padding-left và padding-right

4. _margin-block_ : tương ứng margin-top và margin-bottom

5. _padding-block_ : tương ứng padding-top và padding-bottom

6. _caniuse_ : là 1 web giúp chúng ta kiểm tra những thuộc tính trong css xem nó có được nhìu trình duyệt hỗ trợ hay không ? từ đó chúng ta có thể sử dụng vào trong dự án

7. _semantic tags_ : header, footer, main, section, article, nav(menu), aside

8. _list-style_: thuộc tính này dùng cho thẻ ul(disc) và ol(decimal)

9. _form_ : dùng để làm các _form_(_bỉu mẩu_) nhận thông tin để làm việc gì đó ví dụ như đăng ký tài khoản, đăng nhập, gửi email, điền thông tin cá nhân,..

   - _autocomplete_: tự động điền
   - _input_ : có attributes và nó là thẻ tự đóng _type_ có nhìu loại tùy thuộc vào mục đích chúng ta sử dụng: text, email, number, time, file, date, password, checkbox, radio, submit ...,

     - _placeholder_ là 1 lớp chữ giả mờ để nói cho chúng ta bk input đó làm gì

     - _name_ dùng đề truy xuất dữ liệu

     - _required_ bắt buộc phải nhập data

     - _disabled_ ko cho phép nhập vào, và khi submit form nó cũng ko lấy đc data

     - _readonly_ chỉ đọc, ko sửa được tuy nhiên khi submit form thì vẫn lấy đc dữ liệu

     - _min_: thường dùng cho number, số nhỏ nhất
     - _max_: thường dùng cho number, số lớn nhất
     - _min-length_ : tối thỉu kí tự
     - _max-length_ : tối đa kí tự

   - _button_:

     - _type_: button, submit, reset

   - _select_: thường sẽ đc tùy biến lại bằng cách dùng ul li

   -_textarea_

------ install _sass_ --------

- cài đặt sass với lệnh _npm install -g sass_

- lệnh để chạy sass: _sass path-of-sass-file path-of-css-file --watch_

- _nested_ : lồng nhau
- .header-item, .header-link, .header-top, .header-bottom

<!-- .header{
    code của class .header
    &-item{
        code của class .header-item
    }
    &-link{}
    &-top{}
    &-bottom{}
} -->

- _variables_:
  $primary-color: red;
  color: &primary-color;

- loop: vòng lặp

- sử dụng SASS để viết mixin

@mixin mixin-name($parameter,...){
property: $parameter;
}

- _transition_: làm cho chuyển động trở nên mượt mà hơn, transition: property(all,color,background-color) duration(100ms,200ms,2s,3s) easing(linear, ease, ease-in, ease-in-out,ease-out, cubic bezier)

_flex: 1_

- _flex-shrink_: nếu để giá trị _0_ thì độ rộng (chìu cao) của nó cố định tại kích thước mk thiết lập và không bị bóp lại
- _flex-grow_: nếu giá trị là 1 thì cho phép giãn ra
- _flex-basic_: nó sẽ là độ rộng nếu _flex-direction: row_, hoặc là chìu cao nếu _flex-direction: column_

------ _Grid layout_ -----

display: grid;

grid-template-columns: repeat(auto-fit,minMax(..px,1fr))

grid-template-columns: repeat(auto-fill,minMax(...px,1fr))

auto-fit: nó sẽ lấp đầy khoảng trống còn dư

auto-fill: nó sẽ cố gắng fill đủ số cột

----- _before & after Pseudo_ ----

_background-color_: currentColor -> lấy giá trị theo thuộc tính color

_cursor_: con trỏ, có nhìu loại pointer, not-allow,....

_opacity_: độ trong suốt có giá trị từ 0 -> 1, (0)khi sử dụng opacity thì vẫn có hiển thị con trỏ nếu có sử dụng _cursor: pointer_, vẫn chiếm diện tích

_visibility_: hidden -> khi sử dụng ko thể hiển thị con trỏ nếu có sử dụng _cursor: pointer_, vẫn chiếm diện tích , lưu ý chỉ sử dụng ở phần tử cha thay vì pseudo như _before_ hay _after_

_z-index_: sắp xếp thứ tự ưu tiên khi dùng vài thuộc tính position hoặc flex-box

_pointer-events_ : thường dùng khi mà ko muốn nhấn vào được

_column_ : chia cột cho nội dung thường là đoạn text dài
