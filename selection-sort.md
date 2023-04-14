###  Bu seriyi seçim sıralama algoritmasına göre sıralayın. -> *[22,27,16,2,18,6]* 
1. Listedeki diğer tüm sayılar incelendikten sonra en küçük olan 2 olan sayı seçilir ve 22 ile değiştirilir.
   - [ **2** ,27,16,22,18,6] **-> n karşılaştırma** 

2. Bir sonraki adımda sıralanmamış kısımdan şu anda 6 olan en küçük sayıyı seçip 27 ile değiştiriyoruz.
   - [2, **6** ,16,22,18,27] **-> (n-1) karşılaştırma** 

3. 3. adımda sıralanmamış kısımdaki en küçük sayıyı ararız. Ancak, numara zaten sıralanmamış bölümün en üstünde olduğu için listede herhangi bir değişiklik yapmanıza gerek yoktur. Bu sayı daha sonra sıralanan kısma dahil edilir.
   - [2,6, **16** ,22,18,27] **-> (n-2) karşılaştırma** 

4. 4. adımda en küçük sayı 18 olduğu için 22 ile değiştiriyoruz.
   - [2,6,16, **18** ,22,27] **-> (n-3) karşılaştırma** 

5. Ardından, en küçük sayı olan 22'yi tekrar ararız, ancak zaten doğru konumda olduğu için onu taşımayız.
   - [2,6,16,18, **22** ,27] **-> (n-4) karşılaştırma** 

6. Sonunda son sayı olan 27'ye geliyoruz. Konumu zaten doğru olsa da, bunu doğrulamak için hala bir karşılaştırma yapılıyor.
   - [2,6,16,18,22, **27** ] **-> 1 karşılaştırma** 

**Tüm Karşılaştırma = (n-1) + (n-2) + ... + 1 = n(n-1)/2** <br>
Bu formül O(n<sup>2</sup>) olarak ifade edilir çünkü n büyüdükçe adım sayısı n<sup>2</sup> ile orantılı hale gelir.


###  Serinin Seçim Sıralamasına göre ilk 4 adım -> [7,3,5,8,2,9,4,15,6]
* [ **2** ,3,5,8,7,9,4,15,6]
* [2, **3** ,5,8,7,9,4,15,6]
* [2,3, **4** ,8,7,9,5,15,6]
* [2,3,4, **5** ,7,9,8,15,6]