###  Bu seriyi Merge Sort algoritmasına göre sıralayın. -> *[16,21,11,8,12,22]* 
1. Her bir alt liste yalnızca bir öğe içerene kadar listeyi yinelemeli olarak ikiye bölün.
   - Listeyi ikiye bölün:
     - [16,21,11,8,12,22] -> [16,21,11] - [8,12,22]

   - Sol ve sağ yarıları yinelemeli olarak bölün:
     - [16,21,11] -> [16] - [21,11]
     - [8,12,22] -> [8] - [12,22]

   - Yalnızca bir öğe içerene kadar bölünür.:
     - [21,11] -> [21] - [11]
     - [12,22] -> [12] - [22]
   -  **[16] - [21] - [11] - [8] - [12] - [22]**


2. Her bir alt liste sıralanana kadar aynı birleştirme sıralama algoritmasını tekrar tekrar kullanarak her bir alt listeyi sıralayın.
   - Her yarıyı sıralayın:
     - [21] - [11] -> [11,21]
     - [12] - [22] -> [12,22]
   - Sol ve sağ yarıları yinelemeli olarak sıralayın:
     - [16] - [11,21] -> [11,16,21]
     - [8] - [12,22] -> [8,12,22]
   -  **[11,16,21] - [8,12,22]**

3. Sıralanan iki alt listeyi tek bir sıralanmış liste oluşturmak için birleştirin.
   - İki yarıyı birleştirin:
     -  **[8, 11, 12, 16, 21, 22]**