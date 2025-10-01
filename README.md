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
