# C#-Unity


public class TestManager : MonoBehavior

string benimAdim= "Esat";

int yasim = 22;

void Start()
{
print($"bu eğitimin yazarının adı:{benimAdim} ve yaşı :{yasim}");
}
(Burada $ işaretini print çıktısında böyle pratik de kullanılabilir)

********************************************************************************************************

public class TestManager : MonoBehavior

bool oyunBittimi=true;

void Start()
{
if(!oyunBittimi)
{
    print("gerçekten oyun bitti");
}
}
(burada ! işareti oyunBittimi true değilse demek anlamında kullanıldı)



************************************************************************************************

- ve operatörü  && 
- veya operatörü ||

Örn:


public class TestManager : MonoBehaviour
{

public int yas;  //int 0 olarak alınır değer vermediğimiz için
public bool kadinmi;   //bool değeri belirtmediğimiz için false olur
 void Start()
 { if(yas>=18 && kadinmi)
   {
      print("sınava girebilir"
 } 
 else
 {   
   print("sınava giremez");
   }}}



*********************************************************************************************************************

Switch Yapısı:


Örn:

public class TestManager : MonoBehaviour
{
    public int zekaPuani = 5;


   void Start()
   {
      switch(zekaPuani)
      {
         case 5:
            print("sana trigonometri öğretebilirim");
            break;
        case 4:
            print("hala iyi seviyedesin");
            break;
        case 3:
            print("bu ders sana göre değil");
            break;
        case 2:
            print("sanırım berbat bir günündesin");
            break;
        case 1:
            print("eğitimin oldukça eksik");
            break;
        default:
             print("zeka seviyen uygun değil");
             break;
      } 

    }
   
*********************************************************************************************************************


public class TestManager : MonoBehaviour
{ 

   int dusmanSayisi = 3;


   void Start()
   {
     for(int i=0; i<dusmanSayisi;i++)
     {
            print("Oluşturulan düşman sayısı " +i);
     }
   }




   /*  for diyerek tab tuşuna 2 kez basarsak 
   for (int i = 0; i < ; i++)
{

}  yazısı karşımıza çıkar.

   */
********************************************************************************************************

public class TestManager : MonoBehaviour
{

  int bolenAdet;

  void Start()
  {
    for(int i=0; i<100; i++)
    {
      if(i%2==0)     //(i'nin 2 ye bölümünden kalan 0 ise demek)
      {
          bolenAdet++;
      }
      }
      print (bolenAdet);
      }

*************************************************************************************************************

public class TestManager : MonoBehaviour
{

void Start()
    {
        IlkFonksiyonum();
        ToplamaFNC(5, 10);
        print(IkiIleCarp(20));
    }

private void IlkFonksiyonum()
    {
        print("benim ilk fonksiyonum");
    }

 private void ToplamaFNC(int a, int b)
    {
        int toplam;
        toplam = a + b;
        print("toplam sonuc " + toplam);
    }
      ```                                           
    int IkiIlecarp(int number)
 {
      int sonuc;
      sonuc = number * 2 ;
      return sonuc;
(burada IkiIlecarp fonksiyonu altı kırmızı çizgi ile gösterir çünkü fonksiyon içerisinde int değeri döndürmesini bekliyor ,ama burada void dersek direk kırmızı çizgi oluşmaz.Ama eğer içine int değişkeni atarsak kırmızı çizgi kalkar)
    }

yani örnek olarak ;
    int IkiIleCarp(int number)
{
    int sonuc;
    sonuc = number * 2;
    return sonuc;(return dediğimizde çıktıyı aldırırır ve uyarı kalkmış olur)

}                 

    
    



*******************************************************************************************************






















