public class TestManager : MonoBehavior 

string benimAdim= "Esat"; 
int yasim = 22; 


void Start() 
{

print($"bu eğitimin yazarının adı:{benimAdim} ve yaşı :{yasim}"); 

} (Burada $ işaretini print çıktısında böyle pratik de kullanılabilir)
******************************************************************************************************** 

public class TestManager : MonoBehavior

bool oyunBittimi=true;

void Start()
{

if(!oyunBittimi) 
{ 
print("gerçekten oyun bitti");
} } (burada ! işareti oyunBittimi true değilse demek anlamında kullanıldı) 


************************************************************************************************

- ve operatörü && - veya operatörü ||

 Örn:
public class TestManager : MonoBehaviour
{
public int yas; //int 0 olarak alınır değer vermediğimiz için 

public bool kadinmi; //bool değeri belirtmediğimiz için false olur

void Start()
{ 
if(yas>=18 && kadinmi) 
{ 
print("sınava girebilir" 
} 
else 
{
print("sınava giremez"); 
}}}



********************************************************************************************************************* Switch Yapısı: Örn: public class TestManager : MonoBehaviour { public int zekaPuani = 5; void Start() 
{
switch(zekaPuani)
{ 
case 5: print("sana trigonometri öğretebilirim"); 
break; 
case 4: print("hala iyi seviyedesin");
break;
case 3: print("bu ders sana göre değil");
break; 
case 2: print("sanırım berbat bir günündesin"); 
break;
case 1: print("eğitimin oldukça eksik"); 
break; 
default: print("zeka seviyen uygun değil");
break;
} } 



*********************************************************************************************************************

public class TestManager : MonoBehaviour
{ 
int dusmanSayisi = 3; 

void Start()
{
for(int i=0; i<dusmanSayisi;i++)
{
print("Oluşturulan düşman sayısı " +i);
} } /* for diyerek tab tuşuna 2 kez basarsak for (int i = 0; i < ; i++) { } yazısı karşımıza çıkar.
*/ 

******************************************************************************************************** 
public class TestManager : MonoBehaviour 
{ 
int bolenAdet;
void Start() 
{ 
for(int i=0; i<100; i++) 
{ if(i%2==0) //(i'nin 2 ye bölümünden kalan 0 ise demek) 
{
bolenAdet++; 
} 
} 
print (bolenAdet); 
} 

************************************************************************************************************* public class TestManager : MonoBehaviour { void Start() { IlkFonksiyonum(); ToplamaFNC(5, 10); print(IkiIleCarp(20));
}
private void IlkFonksiyonum() 
{ 
print("benim ilk fonksiyonum");
} 
private void ToplamaFNC(int a, int b) 
{ 
int toplam; toplam = a + b; 
print("toplam sonuc " + toplam);
}
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

 
  
   DİZİLER


<pre
 public class TestManager : MonoBehaviour
 {

     public int[] telefonNumarasi=new int[5]; //telefonNumaralari dizisi 5 elemandan oluşuyor demek istiyoruz
  
     public string[] isimler=new string[]{"Eylül","Buse,"Kübra"};//Böyle kullanarak da dizinin elemanları ile yazabiliriz

     public float[] sayilar = {1f,2.5f};


    void Start()
  {
      print(isimler[1]);  //Burada isimler dizisinden Buse ismini yazdırırız(Diziler 0. ,1. , 2. diye devam ettiği için ilk elemanı istersek print(isimler[0]); demeliydik.

    print(telefonNumaralari.Lenght);  //Burada telefonNumaralari dizisinde kaç eleman olduğunun çıktısını bize verir 

}}


****************************************************************************************************************************************************************


            Foreach Döngüsü




-Unity'den 4 adet cube nesnesi oluşturup bir tane TestManager adında boş nesne oluşturuyoruz
-Scriptimizi boş nesneye atıyoruz

 public class TestManager: MonoBehaviour
{   

     public GameObject[] kupler;     //Sahnedeki her elemana GameObject denir

    private void Start()
    {
       foreach (GameObject obje in kupler) 
    {
            //ilk başta 'var' yerine kullanacağımız dizi içindeki obje ismidir
            //Kupler dizisinin her elemanını obje ismine ata demek.Sonrasında objenin ismini değiştirebiliriz
        print(obje.name);//obje ismine tanımlı isimlerin ismini yazdır
        print(obje.transform.position.x);//obje isminde TestManagere eklediğimiz cubelerin x düzleminde konumunun değerini yazdırır
    }
    //Burada foreach döngüsünde iki tane print basmak için {}içinde foreachi açtık.Eğer yapmazsak ilk printte sıkıntı çıkarmazken ikincisinde foreache almadığı için hata veriyor
    }
}


***************************************************************************************************************************************




                               LİSTELER

*Listeler Dizilerin dinamik halidir.Diziler sabit eleman sayısına sahiptir ama liste oluşturduğumuzda çalışma esnasında(runtime) listedeki eleman sayısı ve içeriğinde değişiklikler yapılabilir.

*Listeler System.Collections.Generic kütüphanesi ile kullanılıyor
*Liste içindeki elemanları rastgele sıralamak için System.Linq kütüphanesini kullanırız
*Aynı elemandan bir daha olmasını istemiyorsak yine System.liq kütüphanesini kullanırız


    

using JetBrains.Annotations;
using NUnit.Framework;
using UnityEngine;
using System.Collections.Generic;
using System.Linq;


public class TestManager : MonoBehaviour
{
    public List<string> evAdresleri=new List<string>();  //ilk önce string formatında liste oluşturtup evAdresleri ismini verdik ve yeni listeye entegre edilip liste oluşturulmuş oldu


    private void Start()
    {
        evAdresleri.Add("Merkez Mahalle");
        evAdresleri.Add("Turan Mahallesi");//buada var olan listeye yeni elemanlar ekledik

        evAdresleri=evAdresleri.OrderBy(i => Random.value).ToList();//Bu kod satırı sayesinde elemanları rastgele sıralarız

        evAdresleri=evAdresleri.Distinct().ToList();//Aynı isimde olan elemanları silmiş olur
        //evAdresleri.Remove("çelebi mahallesi");//Bir elemanı listeden silmiş olduk

        //evAdresleri.RemoveAt(2);//RemoveAt ile istediğimiz indexteki elemanı sileriz.Burada 3. elemanı sileriz

        //evAdresleri.Clear();//Tüm elemanları silmiş oluruz.

    } 
}

    

    











 
