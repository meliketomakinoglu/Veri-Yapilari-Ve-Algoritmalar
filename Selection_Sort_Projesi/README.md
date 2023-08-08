# Insertion Sort

<b>Soru 1:</b> [22,27,16,2,18,6] -> Insertion Sort

Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.

---

<b>Cevap 1:</b> Karşılaştırma işlemine ikinci elemandan başlanılır. "*" işareti olan elemanlar soldaki elemanlarla tek tek karşılaştırılır. Soldakinden küçük ise yer değiştirirler. Bu işlem seçilen eleman soldaki sayıdan büyük olana kadar devam eder.

İşlem bittiğinde seçildiğinde kaçıncı elemansa sonraki eleman karşılaştırma için seçilir.

1. [22, 27*, 16, 2, 18, 6] -> Aynı kalır, sağdaki diğer elemanın karşılaştırma işlemine geçilir.
2. [22, 27, 16*, 2, 18, 6] -> [16, 22, 27, 2, 18, 6]
3. [22, 27, 16, 2*, 18, 6] -> [2, 16, 22, 27, 18, 6]
4. [2, 16, 22, 27, 18*, 6] -> [2, 16, 18, 22, 27, 6]
5. [2, 16, 18, 22, 27, 6*] -> [2, 6, 16, 18, 22, 27]




---
<b>Soru 2:</b> Big-O gösterimini yazınız.

---
<b>Cevap 2:</b> Eleman sayısı n olduğunda, her eleman için en fazla (n-1) karşılaştırma yapılır. Algoritmanın tüm elemanlarını bu şekilde işlemesi gerektiğinde, toplam karşılaştırma sayısı (n-1) + (n-2) + ... + 1 olur, ki bu toplam (n * (n-1) / 2)'ye eşittir.

Big-O gösterimi için en yüksek dereceli terimi göstermemiz lazım. Onun için formülden (n^2) geldiği için gösterimi <b>O(n^2)</b> olur. 

---
<b>Soru 3:</b> Time Complexity: Dizi sıralandıktan sonra 18 sayısı aşağıdaki case'lerden hangisinin kapsamına girer? Yazınız.

1. Average case: Aradığımız sayının ortada olması
2. Worst case: Aradığımız sayının sonda olması
3. Best case: Aradığımız sayının dizinin en başında olması.

---
<b>Cevap 3:</b> Dizi sıralandıktan sonraki hali <b>[2, 6, 16, 18, 22, 27]</b> olacaktır. 18 sayısı dizinin ortasındaki eleman olduğu için cevap "Average case" olacaktır.

---
<b>Soru 4:</b> [7,3,5,8,2,9,4,15,6] dizisinin Selection Sort'a göre ilk 4 adımını yazınız.

---
<b>Cevap 4:</b>

1. [7, 3*, 5, 8, 2, 9, 4, 15, 6] -> [3, 7, 5, 8, 2, 9, 4, 15, 6]
2. [3, 7, 5*, 8, 2, 9, 4, 15, 6] -> [3, 5, 7, 8, 2, 9, 4, 15, 6]
3. [3, 5, 7, 8*, 2, 9, 4, 15, 6] -> [3, 5, 7, 8, 2, 9, 4, 15, 6]
4. [3, 5, 7, 8, 2*, 9, 4, 15, 6] -> [2, 3, 5, 7, 8, 9, 4, 15, 6]
5. [2, 3, 5, 7, 8, 9*, 4, 15, 6] -> [2, 3, 5, 7, 8, 9, 4, 15, 6]
6. [2, 3, 5, 7, 8, 9, 4*, 15, 6] -> [2, 3, 4, 5, 7, 8, 9, 15, 6]
7. [2, 3, 4, 5, 7, 8, 9, 15*, 6] -> [2, 3, 4, 5, 7, 8, 9, 15, 6]
8. [2, 3, 4, 5, 7, 8, 9, 15, 6*] -> [2, 3, 4, 5, 6, 7, 8, 9, 15]

<b>Not:</b> Karşılaştırması yapılan elemana "*" işareti koydum. Soldaki elemanlarla karşılaştırılır ve uygun yere yazılır. Listenin ilk halindeki elemanlar sırasıyla karşılaştırılır.