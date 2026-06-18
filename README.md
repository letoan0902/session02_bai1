# BAI 1: Phan tich va Lua chon cong cu toi uu

## 1. Dap an lua chon

Phuong an toi uu nhat la: C.

## 2. Phan tich vi sao phuong an C toi uu

Phuong an C la cach phan bo cong cu hop ly nhat vi moi cong cu duoc dung dung voi pham vi ngu canh va tinh chat cong viec.

Voi tac vu viet tai lieu huong dan su dung API, Web Chat nhu ChatGPT hoac Claude phu hop vi day la cong viec can kha nang tong hop, dien dat, sap xep noi dung va ly giai bang ngon ngu tu nhien. Lap trinh vien co the cung cap mo ta nghiep vu, endpoint, input, output va quy tac xu ly de AI phac thao tai lieu Markdown. Tac vu nay khong nhat thiet phai doc toan bo ma nguon cua repository neu nguoi dung da dua du thong tin can thiet.

Voi tac vu tai cau truc lop du lieu Book tren nhieu tep nhu Book.java, BookService.java, BookController.java va BookRepository.java, can mot tro ly lap trinh cap cao co kha nang hieu ngu canh repository rong. Viec refactor mot doi tuong du lieu thuong anh huong den model, service, controller, repository, DTO, validation va test. Neu chi sua tung file rieng le, nguy co lech kieu du lieu, loi bien dich hoac bo sot noi phu thuoc rat cao. Agentic hoac repository-wide assistant phu hop hon vi no co the doc, lap ke hoach va cap nhat dong bo nhieu file trong cung ngu canh du an.

Voi tac vu sua loi cu phap nho tai mot dong dang mo, inline completion la lua chon nang suat cao nhat. Loi thieu dau cham phay hoac khai bao sai kieu du lieu chi can ngu canh cuc bo quanh dong hien tai. Dung Web Chat hay agent repository-wide cho loi nay se tao them thao tac thua, lam cham tien do va tang chuyen doi ngu canh khong can thiet.

Xet ve quan ly context window, phuong an C tranh viec dua qua nhieu noi dung khong can thiet vao mot cong cu duy nhat. Noi dung can lap luan ngon ngu duoc dua vao Web Chat, noi dung can hieu quan he nhieu file duoc giao cho assistant co kha nang doc repository, con loi cuc bo duoc xu ly ngay trong IDE. Cach nay giam copy-paste, giam mat ngu canh, giam rui ro AI khong nhin thay file lien quan va tang toc do lap trinh.

Xet ve context switching, phuong an C cung giam viec lap trinh vien phai lien tuc roi IDE, sao chep ma nguon sang trinh duyet, nhan ket qua roi dan nguoc lai. Cang it chuyen doi moi truong lam viec, lap trinh vien cang giu duoc dong suy nghi va tranh loi do sao chep thieu file, thieu dong, hoac dung phien ban ma nguon cu.

## 3. Nhuoc diem cua phuong an A

Phuong an A dung Web Chat cho ca 3 tac vu nen khong toi uu ve ngu canh va nang suat.

Thu nhat, voi refactor Book tren nhieu file, Web Chat khong tu dong thay duoc cau truc repository, quan he phu thuoc, import, test va cac noi su dung khac. Lap trinh vien phai sao chep tung file vao chat, rat de thieu thong tin hoac dua len phien ban da cu.

Thu hai, viec copy-paste lien tuc giua IDE va Web Chat lam tang context switching. Moi lan chuyen cua so, lap trinh vien phai tai nap lai trang thai cong viec trong dau, de mat tap trung va de tao loi thu cong.

Thu ba, neu trong ma nguon co thong tin nhay cam nhu API key, token, cau hinh database, viec dan truc tiep len Web Chat cong cong co the gay rui ro bao mat.

Thu tu, voi loi cu phap nho tai mot dong, dung Web Chat la qua nang. Tac vu nay nen duoc xu ly ngay tai IDE bang inline assistant hoac chinh tay.

## 4. Nhuoc diem cua phuong an B

Phuong an B dung inline code assistant cho ca 3 tac vu cung khong phu hop.

Inline assistant rat manh voi hoan thanh ma cuc bo, sua nhanh mot dong, goi y ten bien hoac bo sung mot doan nho. Tuy nhien, no thuong khong co du ngu canh toan bo repository de dam bao refactor Book tren 4 file duoc dong bo chinh xac. Neu thay doi cau truc Book ma khong cap nhat dung service, controller va repository, du an co the bi loi bien dich hoac loi logic.

Voi tac vu viet API Guide, inline assistant cung khong phai lua chon tot nhat. Tai lieu API can cau truc Markdown ro rang, mo ta nghiep vu, vi du request/response va giai thich cho thanh vien trong nhom. Cong viec nay can kha nang tong hop ngon ngu va lap luan tai lieu nhieu hon la goi y ma tai dong hien tai.

Do do, phuong an B lam giam chat luong o cac tac vu can ngu canh rong hoac can dien dat tai lieu, du co the nhanh voi tac vu Quick Fix.

## 5. Ket luan

Chon phuong an C vi day la cach dung dung cong cu cho dung pham vi cong viec:

- Web Chat cho tai lieu API.
- Agentic hoac repository-wide assistant cho refactor nhieu file.
- Inline completion cho loi cu phap nho tai cho.

Cach phan bo nay quan ly context window tot hon, giam context switching va tang nang suat lap trinh trong tinh huong thoi gian ngan.
