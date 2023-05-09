## MỘT SỐ CÁCH LÀM TỰ LUẬN TIN 10 

### Câu 1
`.split()` là để tách ra tạo thành danh sách, phần trong dấu `()` là dấu hiệu nhận biết để tách 

`.join()` là để gắn thêm phần tử bất kì vào danh sách `",".join(s)`


**VD** 

`s = 'ga vit cho lon ngua ca'` để tách xâu ra thành danh sách `['ga', 'vit', 'cho', 'lon', 'ngua', 'ca']`
thì ta dùng cú pháp `s = s.split(" ")` *vì giữa các chữ có khoảng cách(" ")*


Để ghép xâu thành `'ga,vit,cho,lon,ngua,ca'` thì chỉ cần thêm "," vào danh sách `s` vừa tạo, ta dùng cú pháp `",".join(s)`

___
### Câu 2
Hiểu rõ cách dùng hàm `def` là được!
___
### Câu 3
#### 1. Viết Chương Trình Tìm 'Ước' Của Số Tự Nhiên 'n' Nhập Từ Bàn Phím
Đầu tiên, ta cần phải hiểu 'ước' là gì ? Thì trong 1 biểu thức `a chia hết cho b` thì **b** là _ước_ của a !
Tức ở đây, đề bảo ta tìm _ước_ của số tự nhiên **n** thì tức là ta lấy số đó chia cho lần lượt từng số từ 1 đến số **n** 

Như thế, ta sẽ hình thành đoạn code như sau:
```
def uoc():
    n = int(input("Nhap n: "))
    print("Cac uoc cua", n, "la: ")
    for i in range(1, n+1):
        if n % i == 0:
            print(i, end=" ")
```            
**DEMO**

  <img width="682" alt="Screen Shot 2023-05-09 at 7 50 50 PM" src="https://github.com/TuaKie/exam_python/assets/76782169/719803db-f388-4eca-8754-958efcf318ab">

#### 2. Viết Phương Trình Tìm Nghiệm Phương Trình   $ax^2 + bx + c = 0 (a \neq 0)$
Như ta có cách giải từ trước, thông qua $\Delta$. Nếu

$\Delta > 0$ : Phương trình có 2 nghiệm
- $x1 = \frac{-b + \sqrt(\Delta)}{2a}$
- $x2 = \frac{-b - \sqrt(\Delta)}{2a}$

$\Delta = 0$ : Phương trình có nghiệm kép
- $x = x1 = x2 = \frac{-b}{2a}$

$\Delta < 0$ : Phương trình vô nghiệm

Như vậy, ta sẽ dùng $\Delta$ để giải bài nhưng để có được $\surd$ thì ta sẽ dùng đến thư viện _math_ bằng cách `import math` 
```
def ptbh():
    import math
    a = float(input("Nhập a (a khác 0): "))
    b = float(input("Nhập b: "))
    c = float(input("Nhập c: "))
    delta = b**2 - 4*a*c
    if delta > 0:
        print("Phương trình có 2 nghiệm phân biệt:")
        print("x1 = ", (-b + math.sqrt(delta))/(2*a))
        print("x2 = ", (-b - math.sqrt(delta))/(2*a))
    elif delta == 0: #elif là else if
        print("Phương trình có nghiệm kép x1 = x2 = ", -b/(2*a))
    else:
        print("Phương trình vô nghiệm")
```

**DEMO**

#### 3. Viết Chương Trình Tính Giai Thừa Của 'n'

Như được biết, giai thừa của 1 số n thì sẽ `n! = n(n-1)(n-2)(n-3)*...*2*1`
Tức là giai thừa một số sẽ là `n! = 1*2*3*...*n`

Ta có, đoạn code như sau:
*Nếu đề bảo 'n' nhập từ bàn phím
```
def giaithua():
    n = int(input("Nhập số 'n' cần tính giai thừa: "))
    t = 1
    for i in range(1, n+1):
        t = t * i
    print(f'{n}! = {t}')
```

*Nếu đề không bảo n nhập từ bàn phím
```
def giaithua(n):
    t = 1
    for i in range(1, n+1):
        t = t * i
    print(f'{n}! = {t}')
```

**DEMO**


<img width="682" alt="Screen Shot 2023-05-09 at 8 25 52 PM" src="https://github.com/TuaKie/exam_python/assets/76782169/7d17f36e-c11d-482d-9e93-ee94644450be">
<img width="682" alt="Screen Shot 2023-05-09 at 8 30 04 PM" src="https://github.com/TuaKie/exam_python/assets/76782169/960e2b3f-d474-4f01-a12f-385d46fb46f1">


#### 4. Viết Phương Trình Tìm $ƯCLN$ Của 2 Số Tự Nhiên 'm', 'n' Từ Bàn Phím

```
def UCLN():
  m = int(input("Nhap m: "))
  n = int(input("Nhap n: "))
  while m != n:
    if m > n: 
      m = m - n
    else:
      n = n - m
  print("UCLN la: ", m)

```  
#### 5. Viết Chương Trình Nhập Danh Sách Từ Bàn Phím
##### a. Sau Đó Tính Tổng Phần Tử (Chẵn/Lẻ)

```
def tong():
    n = int(input("Nhập so phan tu trong danh sach: "))
    A = []
    s = 0
    for i in range(n):
        A.append(float(input(f"Nhap phan tu thu {i}: ")))
    for h in A:
        if h%2 == 0: # Nếu đề tìm số lẻ thì đổi thành "h%2 != 0"
            s = s + h
    # Đổi dòng in ra sao cho phù hợp với đề bài
    print(f"Tong cac so chan trong danh sach la: {s}") 
```
##### b. Sau Đó Đếm Phần Tử (Chẵn/Lẻ)
```
def dem():
    n = int(input("Nhập so phan tu trong danh sach: "))
    A = []
    c = 0
    for i in range(n):
        A.append(float(input(f"Nhap phan tu thu {i}: ")))
    for h in A:
        if h%2 == 0: # Nếu đề tìm số lẻ thì đổi thành "h%2 != 0"
            c = c + 1
    # Đổi dòng in ra sao cho phù hợp với đề bài
    print(f"So luong so chan trong day so la {c}")
```

