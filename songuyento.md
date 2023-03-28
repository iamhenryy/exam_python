### VIẾT HÀM XEM 'N' CÓ PHẢI LÀ SỐ NGUYÊN TỐ HAY KHÔNG?
#### Nhiệm vụ 2 / Thực hành / 129 SGK TIN 10 - KNTTVCS

- Dòng code sẽ có dạng như này:

```
def songuyento(n):
    C = 0
    for i in range(2, n):
        if n%i == 0:
            C += 1 #có thể ghi là C = C + 1
    if C == 0:
        print(n, "là số nguyên tố")
    else:
        print(n, "không phải là số nguyên tố")
```


***Chạy chương trình*** _nên chạy ở IDLE Shell_

_Ở đây tớ chạy trên **terminal** nên giao diện hơi tệ 1 tí_


**CÚ PHÁP:** ```songuyento(n)``` 

**n** là tùy bạn chọn



<img width="682" alt="Screen Shot 2023-03-28 at 6 54 38 PM" src="https://user-images.githubusercontent.com/76782169/228228066-59258da5-9593-422d-9b01-2816be22067b.png">
