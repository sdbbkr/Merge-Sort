# Merge-Sort
Merge Sort
 Diziyi her seferinde iki grup olarak parçalıyoruz. Parçalanan dizileri de iki grup olarak parçalıyoruz, ta ki tek elemanlı olana kadar. Sonra tekrar parçaladığımız grupları birleştiriyoruz. Her grubu birleştirmeden önce kendi içinde sıralıyoruz, sonra iki diziyi birleştirirken sıralıyoruz. Son olarak soldan sağa doğru küçükten büyüğe elemanlar dizinin içinde sıralanmış oluyor.

<div style="text-align:center; font-weight:bold;"><p>[16,21,11,8,12,22]</p>
<p>[16,21,11]<--->[8,12,22]</p>
<p>[16]<--->[21,11]<--->[8]<--->[12,22]</p>
<p>[16]<--->[21]<--->[11]<--->[8]<--->[12]<--->[22]</p>
<p>[16]<--->[11,21]<--->[8]<--->[12,22]</p>
<p>[11,16,21]<--->[8,12,22]</p>
<p>[8,11,12,16,21,22]</p>
</div>

---
<b>Soru 2:</b> Big-O gösterimini yazınız.

---
<b>Cevap 2:</b>

"<em> Merge Sort, bir "böl-ve-fethet" (divide and conquer) algoritmasıdır. Aşağıda Merge Sort'un <span style="font-weight:bold; color:aqua">O(n*logn)</span> zaman karmaşıklığını açıklayan adımları bulabilirsiniz:

1. Bölme (Divide) Adımı:
Verilen diziyi ortadan ikiye böleriz. Bu işlem log(n) adımda gerçekleşir, çünkü her seferinde dizi ikiye bölünür.

2. Fethetme (Conquer) Adımı:
Bölünmüş dizileri tekrar tekrar bölerek (rekürsif olarak) en küçük parçalara (genellikle tek elemanlı veya boş dizilere) ulaşırız. Bu adımda her alt dizinin sıralanması O(1) zaman alır.

3. Birleştirme (Merge) Adımı:
Sıralı alt dizileri birleştirerek, her bir birleştirme adımında iki alt diziyi birleştirir ve sıralı bir alt dizi oluştururuz. Bu birleştirme işlemi, alt dizilerin toplam eleman sayısı kadar zaman alır. Tüm alt diziler birleştirilene kadar bu adım tekrarlanır.

Birleştirme adımı, iki sıralı alt diziyi birleştirirken elemanları karşılaştırır ve sıralı bir şekilde birleştirir. Bu işlem, her alt dizi için O(n) zaman alır. Toplamda, bölme adımında log(n) kez bölündüğü için birleştirme adımı O(n*logn) zaman karmaşıklığına sahiptir.

Sonuç olarak, bölme adımının log(n) zaman aldığını ve birleştirme adımının O(nlogn) zaman aldığını düşündüğümüzde, Merge Sort'un toplam zaman karmaşıklığının O(nlogn) olduğunu söyleyebiliriz. </em>"
