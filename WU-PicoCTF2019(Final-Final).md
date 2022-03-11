- [1. The Numbers](#1-the-numbers)
  - [1.1. Đề bài](#11-đề-bài)
  - [1.2. Cách giải](#12-cách-giải)
- [2. Easy1](#2-easy1)
  - [2.1. Đề bài](#21-đề-bài)
  - [2.2. Cách giải](#22-cách-giải)
- [3. 13](#3-13)
  - [3.1. Đề bài](#31-đề-bài)
  - [3.2. Cách giải](#32-cách-giải)
- [4. ceasar](#4-ceasar)
  - [4.1. Đề bài](#41-đề-bài)
  - [4.2. Cách giải](#42-cách-giải)
- [5. la cifra de](#5-la-cifra-de)
  - [5.1. Đề bài](#51-đề-bài)
  - [5.2. Cách giải](#52-cách-giải)
- [6. Tapping](#6-tapping)
  - [6.1. Đề bài](#61-đề-bài)
  - [6.2. Cách giải](#62-cách-giải)
- [7. Flags](#7-flags)
  - [7.1. Đề bài](#71-đề-bài)
  - [7.2. Cách giải](#72-cách-giải)
- [8. Mr-Worldwide](#8-mr-worldwide)
  - [8.1. Đề bài](#81-đề-bài)
  - [8.2. Cách giải](#82-cách-giải)
- [9. rsa-pop-quiz](#9-rsa-pop-quiz)
  - [9.1. Đề bài](#91-đề-bài)
  - [9.2. Cách giải](#92-cách-giải)
- [10. waves over lambda](#10-waves-over-lambda)
  - [10.1. Đề bài](#101-đề-bài)
  - [10.2. Cách làm](#102-cách-làm)
- [11. miniRSA](#11-minirsa)
  - [11.1. Đề bài](#111-đề-bài)
  - [11.2. Cách giải](#112-cách-giải)
- [12. b00tl3gRSA2](#12-b00tl3grsa2)
- [13. AES-ABC](#13-aes-abc)
- [14. b00tl3gRSA3](#14-b00tl3grsa3)
  - [14.1. Đề bài](#141-đề-bài)
  - [14.2. Cách giải](#142-cách-giải)
- [15. john_pollard](#15-john_pollard)
  - [15.1. Đề bài](#151-đề-bài)
  - [15.2. Cách giải](#152-cách-giải)

# 1. The Numbers
## 1.1. Đề bài
![2022-01-14-17-47-42](https://user-images.githubusercontent.com/97771705/149625076-3388d156-533e-403c-8670-7fd8a0f35590.png)
<img width="387" alt="the_numbers" src="https://user-images.githubusercontent.com/97771705/149625012-579e6351-4d6b-483e-a27f-1cca1c775de1.png">
## 1.2. Cách giải
Nhìn cái biết ngay đổi các chữ số về kí tự là có flag

```python
a = (16,9,3,15,3,20,6)
b = (20,8,5,14,21,13,2,5,18,19,13,1,19,15,14)
c = a+b
flag = ''.join([chr(int(i) + ord('a'))for i in c])
print(flag)
```
Kết quả ra: qjdpduguifovncfstnbtpo
Vẫn chưa có flag :(
Thế thì chắc loại này là mã dịch vòng rồi!!!
Ném lên https://www.dcode.fr/shift-cipher
![2022-01-14-17-41-51](https://user-images.githubusercontent.com/97771705/149625176-b0aeea1b-9151-416e-9cad-ad8fc9b7c723.png)
>Đã có flag : picoctf{thenumbersmason}


# 2. Easy1
## 2.1. Đề bài
![2022-01-14-17-48-15](https://user-images.githubusercontent.com/97771705/149625171-fda247e8-fe50-4348-b250-169436b12f4f.png)
![2022-01-14-17-49-14](https://user-images.githubusercontent.com/97771705/149625169-b2f29590-36e0-4b69-aa83-e2e25ecc058d.png)
## 2.2. Cách giải
Ta thấy A + B = B; B + B = C; Z + B = A
Lại giống kiểu vigenere 
Ném lên https://www.dcode.fr/vigenere-cipher
![2022-01-14-17-55-16](https://user-images.githubusercontent.com/97771705/149625167-c4bca44c-711c-48ba-8152-ce1bdd54ae19.png)
>Flag : PicoCTF{CRYPTOISFUN} 

# 3. 13
## 3.1. Đề bài
![2022-01-14-17-57-19](https://user-images.githubusercontent.com/97771705/149625166-6abbe11c-36c2-4b76-af90-0e643953e64e.png)
## 3.2. Cách giải
 Đề bài có gợi ý ROT13 :)...Triển luôn https://www.dcode.fr/rot-cipher
![2022-01-14-17-59-40](https://user-images.githubusercontent.com/97771705/149625164-3e979656-83a6-4afa-811e-2d53847a1f0c.png)
>Flag: picoCTF{not_too_bad_of_a_problem}

# 4. ceasar
## 4.1. Đề bài
![2022-01-14-18-01-06](https://user-images.githubusercontent.com/97771705/149625162-ebae3cb8-aa49-47bc-bc8a-6260f3d33d62.png)
![2022-01-14-18-02-29](https://user-images.githubusercontent.com/97771705/149625161-e47c7292-6b53-488a-b880-e822f508616a.png)
## 4.2. Cách giải
 Đề cho mã Caesar https://www.dcode.fr/caesar-cipher
Chỉ bruteforce phần trong {} thôi
![2022-01-14-18-05-37](https://user-images.githubusercontent.com/97771705/149625160-56eb9b15-d438-4d54-aebd-6a5dbc975b44.png)
>Flag: PicoCTF{crossingtherubicondjneoach}

# 5. la cifra de
## 5.1. Đề bài
![2022-01-14-18-07-25](https://user-images.githubusercontent.com/97771705/149625158-e7d1f701-7c8f-477d-9c21-1b516df9b9af.png)

Cần connect vào:nc jupiter.challenges.picoctf.org 5726
![2022-01-14-18-14-13](https://user-images.githubusercontent.com/97771705/149625156-c76d7451-b7bc-4e64-83a6-37519a849ac6.png)
## 5.2. Cách giải

Hint 2:Perhaps looking at history will help :))))
Nhìn vào lịch sử à....kiếm lại mớ ***hub hay gì :)
Đùa tý. Vừa xài Shift Cipher, ROT13, Vigenere, Caesar
Thử từng cái xem nào
![2022-01-14-21-46-08](https://user-images.githubusercontent.com/97771705/149625179-809c6c2b-dcfa-41b1-9cd5-a5b2ca8a9bcc.png)
![2022-01-14-21-47-15](https://user-images.githubusercontent.com/97771705/149625616-04f67565-f71c-413d-9556-ed17dd4059ed.png)
![2022-01-14-21-48-12](https://user-images.githubusercontent.com/97771705/149625632-3f25ecbd-235a-45ff-a88e-f0a77cd1e764.png)
Thử Shift Cipher, ROT13, Caesar vẫn không ra
Vigenere trên dcode cần key, thử key là : pico, picoctf vẫn không ra :(
Search Google Vigenere decode thì thấy trang https://www.boxentriq.com/code-breaking/vigenere-cipher
Thử auto solver
Vẫn không có, hoảng thực sự....
Nhưng cái gì đây
![2022-01-14-21-56-36](https://user-images.githubusercontent.com/97771705/149625685-4756e76e-b61f-47aa-a133-b9f24d068949.png)
Mấy chữ đầu có nghĩa kìa, key bên cạnh là flagflagfg,
thử key là flag xem sao
Và nó ra thế này:

It is interesting how in history people often receive credit for things they did not create

During the course of history, the Vigenère Cipher has been reinvented many times

It was falsely attributed to Blaise de Vigenère as it was originally described in 1553 by Giovan Battista Bellaso in his book La cifra del. Sig. Giovan Battista Bellaso

For the implementation of this cipher a table is formed by sliding the lower half of an ordinary alphabet for an apparently random number of places with respect to the upper halfpicoCTF{b311a50_0r_v1gn3r3_c1ph3r6fe60eaa}

The first well-documented description of a polyalphabetic cipher however, was made around 1467 by Leon Battista Alberti.
The Vigenère Cipher is therefore sometimes called the Alberti Disc or Alberti Cipher.

In 1508, Johannes Trithemius invented the so-called tabula recta (a matrix of shifted alphabets) that would later be a critical component of the Vigenère Cipher.

Bellaso’s second booklet appeared in 1555 as a continuation of the first. The lower halves of the alphabets are now shifted regularly, but the alphabets and the index letters are mixed by means of a mnemonic key phrase, which can be different with each correspondent.
>Flag:picoCTF{b311a50_0r_v1gn3r3_c1ph3r6fe60eaa}

# 6. Tapping
## 6.1. Đề bài
![2022-01-14-22-00-51](https://user-images.githubusercontent.com/97771705/149625707-48060acb-ec76-433d-91e8-60baf2756f07.png)
## 6.2. Cách giải
Kết nối vào nc jupiter.challenges.picoctf.org 48247
![2022-01-14-22-02-02](https://user-images.githubusercontent.com/97771705/149625727-b16765fc-d411-42a2-8b38-2ca2aeda9591.png)
Mã Morse!!
Vào https://morsedecoder.com/
![2022-01-14-22-03-58](https://user-images.githubusercontent.com/97771705/149625147-701b60db-c751-4c61-ab6a-f47ee12409ce.png)
>Flag:PICOCTF{M0RS3C0D31SFUN1261438181}

# 7. Flags
## 7.1. Đề bài
![image](https://user-images.githubusercontent.com/97771705/149626907-72ac65c6-1f1d-4043-8548-109ab67d8c8e.png)

 <img width="821" alt="flag" src="https://user-images.githubusercontent.com/97771705/149626940-035c183e-d8e0-489f-8bf9-663691f8e927.png">

## 7.2. Cách giải
Đúng như tên gọi, mật mã lần này là "những lá cờ"(Flags)
![visual_flags_maritime2](https://user-images.githubusercontent.com/97771705/149627236-ec5a0701-394e-4bd4-b75f-5713ea5033d9.gif)
>Flag: picoctf{f1ag5and5tuff}
# 8. Mr-Worldwide
## 8.1. Đề bài
![image](https://user-images.githubusercontent.com/97771705/149627406-c6ef6ff9-c97b-44a0-a0a0-bee3730d8d97.png)
[message.txt](https://github.com/LuluL0g1n/picoctf-2019/files/7875269/message.txt)

## 8.2. Cách giải
Search Google mấy cái số nó ra toạ độ :)
Kyōto, Nhật Bản             (35.028309, 135.753082)
Odessa, Ukraina             (46.469391, 30.740883)
Dayton, Ohio, USA           (39.758949, -84.191605)
Istanbul, Thổ Nhĩ Kỳ (41.015137, 28.979530)
A-bu Đa-bi, Abu Dhabi - UAE (24.466667, 54.366669)
Kuala Lumpur, Malaysia      (3.140853, 101.693207)
_
A-đi A-ba-ba, Ethiopia      (9.005401, 38.763611)
Loja, Ecuador               (-3.989038, -79.203560)
Am-xtéc-đam, Hà Lan         (52.377956, 4.897070)
Sleepy Hollow,New York,USA  (41.085651, -73.858467)
Kodiak, Alaska, USA         (57.790001, -152.407227)
Alexandria Governorate,Egypt(31.205753, 29.924526)
Nếu đề ý thì các bạn sẽ thấy mấy cái chữ cái đầu là KODIAK_ ALASKA
>Flag: picoctf{KODIAK_ALASKA}
# 9. rsa-pop-quiz
## 9.1. Đề bài
![2022-01-14-22-05-23](https://user-images.githubusercontent.com/97771705/149625145-a3f68ce8-53bc-4346-b1af-6cae799e580d.png)
## 9.2. Cách giải
Kết nối vào nc jupiter.challenges.picoctf.org 1981
>![2022-01-14-22-07-02](https://user-images.githubusercontent.com/97771705/149625144-ba5e8d0d-f983-4ab6-a22c-f4850b0b05d1.png)

Câu hỏi 1 là cho p và q, liệu có tìm được n

>Kiến thức cơ bản về RSA là  p * q = n

Nhập Y
![2022-01-14-22-09-25](https://user-images.githubusercontent.com/97771705/149625143-4c045625-e6b1-4ea6-92f6-d49c9f7d4072.png)

 n = p * q = 76753 * 60413 =  4636878989

 **1 lưu ý là phải nhập nhanh, nếu không sẽ bị lỗi server. Mình mất khá nhiều thời gian cho câu này vì bỏ đi tính, xong lúc về nhập lại kết quả thì nó đơ luôn, lại phải làm lại từ đầu**

 >![2022-01-14-22-17-49](https://user-images.githubusercontent.com/97771705/149625142-69bd75d7-1a60-4219-b21b-68fed79eee4e.png)
Câu hỏi số 2 là tìm q khi biết 2 số n và p
Nhập Y và tính q: 
 q = n / p = 5051846941 / 54269 = 93089
  ![2022-01-14-22-35-28](https://user-images.githubusercontent.com/97771705/149625193-b07ce7e6-3ff1-4662-bf87-128ac1332b73.png)

>![2022-01-14-22-36-21](https://user-images.githubusercontent.com/97771705/149625191-4afba15e-0718-4f59-b513-528c4ca8811d.png)
Câu hỏi số 3 là cho e và n, tìm p,q
Mình đưa n lên http://factordb.com/ , nhưng không thành công trong việc phân tích ra p và q
Hệ mã RSA thực sự rất khó để phá vỡ chỉ với n và e
Nhập N

>![2022-01-14-22-19-26](https://user-images.githubusercontent.com/97771705/149625136-4c104497-3be4-46f6-90fa-860a4dedd14a.png)
Câu hỏi số 4: cho p và q, tìm hàm phi Euler
Ta có: Phi = (p - 1) * (q - 1)
Nhập Y, tính được ra $Phi = 836623060$ 
  ![2022-01-14-22-20-25](https://user-images.githubusercontent.com/97771705/149625135-05dee925-e9cc-4939-89ac-e565f40ee167.png)

>![2022-01-14-22-21-08](https://user-images.githubusercontent.com/97771705/149625134-fac7507b-b547-42c6-b38e-29b3069475de.png)
Câu số 5: cho plaintext, e, n và tìm ciphertext
Có 2 công thức phải nhớ 
    ciphertext = plaintext ^ e (mod n)
    plaintext = ciphertext ^ d (mod n)
    với e * d = -1 (mod Phi)
Vậy là có thể tìm được. Nhập Y
```python

plaintext = 6357294171489311547190987615544575133581967886499484091352661406414044440475205342882841236357665973431462491355089413710392273380203038793241564304774271529108729717
e = 3
n = 29129463609326322559521123136222078780585451208149138547799121083622333250646678767769126248182207478527881025116332742616201890576280859777513414460842754045651093593251726785499360828237897586278068419875517543013545369871704159718105354690802726645710699029936754265654381929650494383622583174075805797766685192325859982797796060391271817578087472948205626257717479858369754502615173773514087437504532994142632207906501079835037052797306690891600559321673928943158514646572885986881016569647357891598545880304236145548059520898133142087545369179876065657214225826997676844000054327141666320553082128424707948750331
cyphertext=pow(plaintext,e,n)
print(cyphertext)
```
  ![2022-01-14-22-24-55](https://user-images.githubusercontent.com/97771705/149625132-b40a0a78-f358-4dc2-94a1-2ededcdb357c.png)

>![2022-01-14-22-26-06](https://user-images.githubusercontent.com/97771705/149625126-594cef53-34e8-4a92-9b65-d564cb83972a.png)
Câu số 6: Cho ciphertext, e, n và tìm plaintext
Muốn tìm đươc plaintext, ta phải có d, và muốn có d, ta phải tìm được Phi, hay p và q
Rất khó để từ n phân tích ra p và q
Nhập N

>![2022-01-14-22-26-34](https://user-images.githubusercontent.com/97771705/149625122-610819c7-c227-463a-b98b-deeb93a2f17a.png)
Câu hỏi số 7: Cho p, q, e và tìm d
Hoàn toàn có thể tìm được
Phi = (p - 1) * (q - 1)
e * d = -1 (mod Phi)
```python
q = 92092076805892533739724722602668675840671093008520241548191914215399824020372076186460768206814914423802230398410980218741906960527104568970225804374404612617736579286959865287226538692911376507934256844456333236362669879347073756238894784951597211105734179388300051579994253565459304743059533646753003894559
p = 97846775312392801037224396977012615848433199640105786119757047098757998273009741128821931277074555731813289423891389911801250326299324018557072727051765547115514791337578758859803890173153277252326496062476389498019821358465433398338364421624871010292162533041884897182597065662521825095949253625730631876637
e = 65537
phi = (q-1)*(p-1)
d=pow(e,-1,phi)
print(d)
```
![2022-01-14-22-26-54](https://user-images.githubusercontent.com/97771705/149625961-7702d0d7-c762-49b5-b0f3-f2fb3ae87631.png)

>![2022-01-14-22-27-22](https://user-images.githubusercontent.com/97771705/149625994-9f8136b9-a92a-4e18-8ad5-f76d666c18d8.png)
Câu số 8: Cho p,e,n,ciphertext, tìm plaintext
Rất dễ dàng để tìm được: chúng ta đi từ viêc tìm q, Phi, d và cuối cùng là plaintext
```python
p = 153143042272527868798412612417204434156935146874282990942386694020462861918068684561281763577034706600608387699148071015194725533394126069826857182428660427818277378724977554365910231524827258160904493774748749088477328204812171935987088715261127321911849092207070653272176072509933245978935455542420691737433
ciphertext = 18031488536864379496089550017272599246134435121343229164236671388038630752847645738968455413067773166115234039247540029174331743781203512108626594601293283737392240326020888417252388602914051828980913478927759934805755030493894728974208520271926698905550119698686762813722190657005740866343113838228101687566611695952746931293926696289378849403873881699852860519784750763227733530168282209363348322874740823803639617797763626570478847423136936562441423318948695084910283653593619962163665200322516949205854709192890808315604698217238383629613355109164122397545332736734824591444665706810731112586202816816647839648399
e = 65537
n = 23952937352643527451379227516428377705004894508566304313177880191662177061878993798938496818120987817049538365206671401938265663712351239785237507341311858383628932183083145614696585411921662992078376103990806989257289472590902167457302888198293135333083734504191910953238278860923153746261500759411620299864395158783509535039259714359526738924736952759753503357614939203434092075676169179112452620687731670534906069845965633455748606649062394293289967059348143206600765820021392608270528856238306849191113241355842396325210132358046616312901337987464473799040762271876389031455051640937681745409057246190498795697239
q =n//p
phi = (q-1)*(p-1)
d=pow(e,-1,phi)
plaintext = pow(ciphertext,d,n)
print(plaintext)
```
  ![2022-01-14-22-30-52](https://user-images.githubusercontent.com/97771705/149626028-d69cb870-5e8b-4b62-a3c6-2d04803649ca.png)
Dòng cuối : chuyển plaintext sang hex rồi ascii là được flag
Mình chuyển nó qua long_to_bytes, vẫn ổn :) 
```python
from Crypto.Util.number import long_to_bytes
a= 14311663942709674867122208214901970650496788151239520971623411712977120586163535880168563325
b=(long_to_bytes(a))
print(b)
```
>Flag:picoCTF{wA8_th4t$_ill3aGal..ode01e4bb}

# 10. waves over lambda
## 10.1. Đề bài
![image](https://user-images.githubusercontent.com/97771705/149629520-3a2b2b93-caf1-4642-93ba-296e0b4c62fd.png)
![image](https://user-images.githubusercontent.com/97771705/149642985-e8f9c3f9-9d79-4eba-874b-789338c02da2.png)
## 10.2. Cách làm
Thử Caesar, Vigenere, Shift cipher, ROT13... các kiểu, không ra kết quả
Mình hỏi và xem WU thì thấy 1 loại mã thay thế sử dụng https://www.dcode.fr/monoalphabetic-substitution hoặc https://www.boxentriq.com/code-breaking/cryptogram
![image](https://user-images.githubusercontent.com/97771705/149643078-b9b6c44a-2bfb-42d9-965c-dd173a911527.png)
>Flag:FREQUENCY_IS_C_OVER_LAMBDA_AGFLCGTYUE
# 11. miniRSA
## 11.1. Đề bài
![2022-01-14-23-19-57](https://user-images.githubusercontent.com/97771705/149625189-7d980dec-91bd-4a69-baa5-9378119f6b13.png)
[ciphertext.txt](https://github.com/LuluL0g1n/picoctf-2019/files/7875216/ciphertext.txt)
## 11.2. Cách giải
ciphertext quá bé so với n, và e chỉ bằng 3
Khi đó : $ciphertext = plaintext ^ e (mod n)$ quá dễ để phá vỡ, bởi vì ciphertext quá bé, plaintext ^ 3 trực tiếp ra ciphertext luôn
Để tìm plaintext, ta chỉ việc lấy ciphertext ^ 1/3
```python
import gmpy2
N= 29331922499794985782735976045591164936683059380558950386560160105740343201513369939006307531165922708949619162698623675349030430859547825708994708321803705309459438099340427770580064400911431856656901982789948285309956111848686906152664473350940486507451771223435835260168971210087470894448460745593956840586530527915802541450092946574694809584880896601317519794442862977471129319781313161842056501715040555964011899589002863730868679527184420789010551475067862907739054966183120621407246398518098981106431219207697870293412176440482900183550467375190239898455201170831410460483829448603477361305838743852756938687673
e= 3
ciphertext= 2205316413931134031074603746928247799030155221252519872650080519263755075355825243327515211479747536697517688468095325517209911688684309894900992899707504087647575997847717180766377832435022794675332132906451858990782325436498952049751141 
d=gmpy2.iroot(ciphertext,e)[0]
print(long_to_bytes(d))
```
>Flag:picoCTF{n33d_a_lArg3r_e_d0cd6eae}
# 12. b00tl3gRSA2
## Đề bài

> nc jupiter.challenges.picoctf.org 57464

## Cách giải
> Số e rất lớn, gần bằng n. Đây có thể là Wiener's attack
``` py
import owiener
from Crypto.Util.number import long_to_bytes
c= 53850507910542587658859173561007250395086411337643703949997556035405299093432806117287566553098998523704973619868267127055468279286238237705244262066579626124754863727318736645190663170192892681082148394054295494490753542644765150567505953437282012971270832932321100966187880029202978062768745173384253176237
n= 155041457231398384319690425686075510270429766873337453375316709777765170810536312951874799366468691703712079942812947276993701467170757543128611182586827133598846945711129346482682401814903830457954034662767104986318074113788915165987271761868516913838490317961207401480892652852068747265421579640613530165069
e= 151050506495945600787528170042203966168224676363925666387139660334014467495502442619851472291209941945496685907939128791919798566898894809478032622917877090616460562404925969117987005529641669322595555865158527864570998440105926774323261519769890876350667697441885940486565362712881383837794681198493910749273
d=owiener.attack(e,n)
print(long_to_bytes(pow(c,d,n)))
# b'picoCTF{bad_1d3a5_2438125}'
```

`flag: picoCTF{bad_1d3a5_2438125} `
# 13. AES-ABC
# 14. b00tl3gRSA3
## 14.1. Đề bài
![2022-01-15-07-51-20](https://user-images.githubusercontent.com/97771705/149625187-8cc1176d-277e-4120-8c56-59cb2fffb9a8.png)
![2022-01-15-08-49-02](https://user-images.githubusercontent.com/97771705/149625182-2432c82e-651b-4dcb-9860-b4d00f37d698.png)
## 14.2. Cách giải
Đầu tiên cứ đưa n lên http://factordb.com/
![2022-01-15-08-50-15](https://user-images.githubusercontent.com/97771705/149625522-e7e32532-6297-46cc-af63-34341c07eacc.png)
factor được nhưng nhiều số quá, mỗi số này lại không phải nguyên tố nữa :(
Có thể tính Phi được bằng cách nhập hết các số
Chợt nhớ ra, nếu factordb mà tính được thì https://www.alpertron.com.ar/ECM.HTM cũng tính được
![2022-01-15-08-50-59](https://user-images.githubusercontent.com/97771705/149625178-a6112c51-c699-4d3e-9055-67756cbbe81c.png)
Có được Phi quá dễ dàng!!!(là Euler's totient)
```python
from Crypto.Util.number import long_to_bytes
c = 76838729197937431445423339638495285109021979752814435768929604168480613512282439927501122101671726532076507942097821433468278876240820094199920245865448294549423273319212884135042869057636953723209688219169529104070096203744955010427421376806995639082646806310717403065646034334474430567055311064652521966238477102294065120360427561047301236186
n = 86340989667583110309331473945511768235627850970656631904736767680910122160680226301871758121209507848061641780575168724323628515047648772901859471287408808500910177684243704614975601662012864773845433966817782396378920053311188157041747522918814284470759253537920063282420851324673727088562926246556814939474864589826084981530267214837517503099
d = 4386634620184607762801000587793750259515481791768916771962561468341930606220854701023766669548218466045934401780610047976737541060569047767233232966407059261139155888705565521732661644463232305011086976675086058946799126205570402504673405663364773669941173598470197835249451220890708754668410795843022855903208381453933916175982080132810473473
phi =  86340989438015800740540319041651956187461550560199369593373692298910249337397481701271740017608309416075782092296794574814613769673675237910203387589920571321953119076162554535044858560456807539226749356571324829981046421546648339113071339434412844807624692879890956041450062861105335306328592447446809272801599181531568943398912000000000000000
e = 65537
d=pow(e,-1,phi)
plaintext = pow(c,d,n)

print(long_to_bytes(plaintext))
```
> Flag:picoCTF{too_many_fact0rs_8606199}

# 15. john_pollard
## 15.1. Đề bài
![image](https://user-images.githubusercontent.com/97771705/149643259-cafeb242-00b1-444a-a96b-b381a3e16ac1.png)
[cert.txt](https://github.com/LuluL0g1n/picoctf-2019/files/7876172/cert.txt)

## 15.2. Cách giải
Sử  dụng http://certificate.fyicenter.com/2145_FYIcenter_Public_Private_Key_Decoder_and_Viewer.html để giải mã trong thư mục cert
![image](https://user-images.githubusercontent.com/97771705/149643315-57f893a4-340b-461b-9545-fbd8c7d21d18.png)
Modul n có dạng hex : 11a4d45212b17f
Chuyển nó về int
```python
print(int('11a4d45212b17f',16))
```
n = 4966306421059967
ném n lên http://factordb.com/
![image](https://user-images.githubusercontent.com/97771705/149643352-8be31311-457a-4527-8a10-ff61d335bb3c.png)
>Flag: picoctf{73176001,67867967}
