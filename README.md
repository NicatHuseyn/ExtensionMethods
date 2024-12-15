
  <h1>Extension Methods</h1>
    <p>
      Bir class-a ya da interface-ə öz içərisindəki metoddan başqa, fərqli bir
      yerdə bəyan edilmiş bir metodu əlavə etmək istəsək, ya inheritance
      istifadə edəcəyik ya da <strong>extension method.</strong>
    </p>
    <p>
      Interitance ilə extension metod nəticə olaraq eyni işi görür, yəni bir
      metodu özünün bəyan edilmədiyi başqa bir class-a inteqrasiya edir.
      İnheritance və extension metod arasında ki, təməl fərq isə inheritance-də,
      əvvəlcədən bəyan etdiyimiz bir class-ın içərisindəki member-ı bəyan
      edilmiş və ya bəyan edilməkdə olan miras yolu ilə ötürür. Extension
      metodda isə o anda bəyan edilən metodu, əvvəlcədən bəyan edilmiş bir
      class-ın içərisinə inteqrasiya etməkdir.
    </p>
    <p>
      C#-da, .NET içərisində verilən ya da istifadə edilən fərqli bir kitabxana
      tərəfindən gətirilən class yaxud interface içərisinə özümüz bir metod
      əlavə edə bilərikmi?
      <br />
      Təbii ki, Xeyr...! Başqasının yaratdığı class-ın source-unu əldə etmədən
      ora bir metod əlavə edə bilmərik!
      <br />
      Məzh, C# proqramlaşdırma gah öz yaratdığımız gah source-i əlimizdə olmayan
      və .NET ya da fərqli bir kitabxana vasitəsilə gəlmiş olan class və ya
      interface-lər də Extension metod sayəsində yeni bir metod bəyan edə və
      istifadə edə bilərik.
    </p>

  <h1>Extension metodlar hansı hallarda istifadə edilir?</h1>

  <p>
      Mövcud class-ın funksionallıqlarını irəlilətmək istəyiriksə, bu zaman
      extension method istifadə edə bilərik. Extension metodlarla biz bir
      class-ın içərisinə dinamik bir metod əlavə edə bilirik, həmin class-ın
      source kodunu dəyişmirik.
      <br />
      Third party kitabxanalarla da uyğunlaşır.
      <br />
      Daha oxunaqlı kod yazmış oluruq.
      <br />
      Kod təkrarını azaldırıq.
    </p>

  <h3>Extension Metodların Avantajları:</h3>
    <ul>
      <li>
        Extension metodlar, mövcud class-lara yaxud interfeyslərə yeni
        funksionallıqlar əlavə etməyin flexible bir yoludur. Bu özəllik
        sayəsində kodu daha modular və dəyişikliklərə az müqavimət göstərir.
      </li>
      <li>
        Class ya da interfeysin mövcud kodunu dəyişdirmədən, yeni bir
        funksionallıq gətirməyi asanlaşdırır.
      </li>
    </ul>

  <h1>Extension Metod Necə İstifadə Edilir?</h1>
    <div style="margin: 10px 0">
      <img style="width: 300px" src="https://github.com/user-attachments/assets/c1089f8f-110f-4f01-b7b2-600246f8d34c" alt="" />
    </div>

  <p>
      Tutaq ki, bir class-ımız var. İndi bu class-ın içərisinə bir Extension
      Metod qazandırmaq istəyirik. İndi biz bir extension metod qazandırmaq
      istəyiriksə, bu metod fərqli bir yerdə olmalıdır.
    </p>
    <br />
    <p>Extension metodları fərqli bir class-da bəyan edirik.</p>
    <div style="margin: 10px 0">
      <img style="width: 300px" src="https://github.com/user-attachments/assets/0337a8d1-1715-46ed-9f6d-f6038ecc0b86" alt="" />
    </div>
    <br />

  <p>
      Extension Metodlar static class-larda bəyan edilmək məcburiyyətindədir.
      Buradan da deyə bilərik ki, Extension metodlar static cass-ların
      içərisində olacağına görə, static metodlardır.
    </p>
    <br />
    <p>
      Ardı ilə hədəf class ya da interface-ə əlavə etmək istədiyimiz metodu
      yazaq.
    </p>
    <div style="margin: 10px 0">
      <img style="width: 600px" src="https://github.com/user-attachments/assets/a6ebcfc8-f293-4436-9418-e971c5a89f5e" alt="" />
    </div>

  <p>
      Belə baxanda deyə bilərik ki, bu normal metoddur. Bunu Extension metod
      edən nədir?
      <br />
      <strong
        >Bunu Extension Metod edən parametrindəki “this” keyword-üdür.</strong
      >
      <br />
      Bir metodu, hədəf bir class-a, interfeysə, yəni bir referansa Extension
      metod kimi vermək istəyiriksə, bu metodun parametrində “this” olmalıdır.
      Parametrdəki referans hədəf referansı təmsil edir.
      <br />
      Biz “this MyClass” deyiriksə, bu o deməkdir ki, bu metod MyClass
      referansına Extension metod olaraq əlavə ediləcəkdir.
    </p>
    <div style="margin: 10px 0">
      <img style="width: 600px" src="https://github.com/user-attachments/assets/59dbbb8f-1b28-47ec-9e8a-a6443214a0a1" alt="" />
    </div>
    <p>
      Koddan görüldüyü kimi artıq MyClass-ın içərisində Extension Metod əlavə
      edilmişdir.
      <br />
      Extension metodun istifadə edildiyi bir class-ın instansı üzərindən
      əlaqəli metodu əldə etdikdə, bu instansa this keyword-ü ilə bəyan edilmiş
      olan bu parametr tərəfindən metod içərisində əldə edib işlərimizi görə
      bilərik. Yəni aşağıdakı kimi
    </p>
    <div style="margin: 10px 0">
      <img style="width: 600px" src="https://github.com/user-attachments/assets/97854eac-8810-4ffb-a976-69accd46a96f" alt="" />
  </div>
