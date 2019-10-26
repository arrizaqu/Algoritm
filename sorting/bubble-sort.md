# Bubble Sort

Solving : 

```
Proses Bubble Sort(Ascending):
Iterasi 1 :
10    5    2    15    1    → (10 bandingkan dengan 5)
5    10    2    15    1    → (10 tukar dengan 5. Bandingkan 10 dengan 2)
5    2    10    15    1    → (2 tukar dengan 10. Bandingkan 10 dengan 15)
5    2    10    15    1    → (Tidak ada pertukaran. Bandingkan 15 dengan 1)
5    2    10    1    15    → (15 tukar dengan 1)

Iterasi 2 :
5    2    10    1    15    → (5 bandingkan dengan 2)
2    5    10    1    15    → (5 tukar dengan 2. Bandingkan 5 dengan 10)
2    5    10    1    15    → (Tidak ada pertukaran. Bandingkan 10 dengan 1)
2    5    1    10    15    → (10 tukar dengan 1)

Iterasi 3 :
2    5    1    10    15    → (2 bandingkan dengan 5)
2    5    1    10    15    → (Tidak ada pertukaran. Bandingkan 5 dengan 1)
2    1    5    10    15    → (5 tukar dengan 1)

Iterasi 4 :
2    1    5    10    15    → (2 bandingkan dengan 1)
1    2    5    10    15    → (2 tukar dengan 1)

Iterasi 5 :
1    2    5    10    15    → (1 bandingkan dengan 2)


Maka, Data diatas setelah di sorting ialah sebagai berikut :
1    2    5    10    15
```

Java Code : 

```java
/**
 *
 * @author arrizaqu
 */
public class BubbleSort {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        int[] angka = {7, 200, 20, 9, 12, 4};
        for (int i = 0; i < angka.length-1; i++) {
            sortImplemetation(angka);
        }     
        System.out.println(Arrays.toString(angka));
    }
   
    public static int[] sortImplemetation(int[] angka){
        for(int bangun = 0; bangun < angka.length-1; bangun++){
            for(int i = 0; i < angka.length-1; i++){
                for (int j = 0; j < angka.length; j++) {
                    //tukar posisi
                    if(i == bangun && j == bangun && angka[j] > angka[j+1]){
                        int temp2 = angka[j];
                        angka[j] = angka[j+1];
                        angka[j+1] = temp2;
                    }
                }
            }
        }
        return angka;
    }
}

```



