<h1 align="center">💡 C# - Unity Notları</h1>

<p align="center">
Hazırlayan: <b>Esat Alpaslan</b>  
Bu notlar, Unity ve C# temellerini pekiştirmek amacıyla hazırlanmıştır.
</p>

---

## 🧠 Değişkenler ve String Interpolation

<pre style="background:#0d1117; color:#c9d1d9; padding:12px; border-radius:10px;">
<code>
public class TestManager : MonoBehaviour
{
    string benimAdim = "Esat";
    int yasim = 22;

    void Start()
    {
        print($"bu eğitimin yazarının adı: {benimAdim} ve yaşı: {yasim}");
    }
}
</code>
</pre>

<div style="border-left:4px solid #58a6ff; padding:10px; background:#161b22;">
💡 <b>Not:</b> <code>$</code> işareti string içerisinde değişkenleri doğrudan kullanmamızı sağlar.
</div>

---

## ⚙️ Mantıksal Operatörler ve Koşullar

<pre style="background:#0d1117; color:#c9d1d9; padding:12px; border-radius:10px;">
<code>
public class TestManager : MonoBehaviour
{
    bool oyunBittimi = true;

    void Start()
    {
        if(!oyunBittimi)
        {
            print("gerçekten oyun bitti");
        }
    }
}
</code>
</pre>

<div style="border-left:4px solid #58a6ff; padding:10px; background:#161b22;">
💬 <b>! işareti</b> ifadenin tersini alır (true ise false, false ise true).
</div>

---

### 🔸 “ve” (&&) – “veya” (||) Operatörleri

<pre style="background:#0d1117; color:#c9d1d9; padding:12px; border-radius:10px;">
<code>
public class TestManager : MonoBehaviour
{
    public int yas;
    public bool kadinmi;

    void Start()
    {
        if (yas >= 18 && kadinmi)
        {
            print("sınava girebilir");
        }
        else
        {
            print("sınava giremez");
        }
    }
}
</code>
</pre>

---

## 🔄 Switch Yapısı

<pre style="background:#0d1117; color:#c9d1d9; padding:12px; border-radius:10px;">
<code>
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
}
</code>
</pre>

---

## 🔁 For Döngüsü

<pre style="background:#0d1117; color:#c9d1d9; padding:12px; border-radius:10px;">
<code>
public class TestManager : MonoBehaviour
{ 
    int dusmanSayisi = 3;

    void Start()
    {
        for(int i = 0; i < dusmanSayisi; i++)
        {
            print("Oluşturulan düşman sayısı " + i);
        }
    }
}
</code>
</pre>

<div style="border-left:4px solid #58a6ff; padding:10px; background:#161b22;">
💡 <b>İpucu:</b> Visual Studio’da <code>for</code> yazıp <b>Tab</b> tuşuna 2 kez bastığında otomatik for şablonu oluşur.
</div>

---

## 🧮 Mod Alma (Kalan Hesaplama)

<pre style="background:#0d1117; color:#c9d1d9; padding:12px; border-radius:10px;">
<code>
public class TestManager : MonoBehaviour
{
    int bolenAdet;

    void Start()
    {
        for (int i = 0; i < 100; i++)
        {
            if (i % 2 == 0)
            {
                bolenAdet++;
            }
        }
        print(bolenAdet);
    }
}
</code>
</pre>

---

## 🧩 Fonksiyonlar

<pre style="background:#0d1117; color:#c9d1d9; padding:12px; border-radius:10px;">
<code>
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
        int toplam = a + b;
        print("toplam sonuç: " + toplam);
    }

    int IkiIleCarp(int number)
    {
        int sonuc = number * 2;
        return sonuc;
    }
}
</code>
</pre>

<div style="border-left:4px solid #58a6ff; padding:10px; background:#161b22;">
🧠 <b>Not:</b> Fonksiyonun dönüş tipi <code>int</code> ise mutlaka <code>return</code> ifadesi kullanılmalıdır.
</div>

---

## 📚 Diziler
