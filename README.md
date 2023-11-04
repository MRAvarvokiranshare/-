 Web security tools 

![Screenshot_۲۰۲۳۱۱۰۴_۱۹۵۰۴۴_Termux](https://github.com/MRAvarvokiranshare/-/assets/146922434/bce8c943-5e43-4c6f-9c9b-e45a1001e0bb)



ابزار ارزیابی امنیت وب، Bypass 403
ابزاری پیشرفته که منحصراً برای علاقه مندان به امنیت وب، تسترهای نفوذ و مدیران سیستم طراحی شده است. WebSecProbe ابزار پیشرفته شما برای انجام ارزیابی های پیچیده امنیتی وب با دقت و عمق است. این ابزار قوی، فرآیند پیچیده بررسی وب سرورها و برنامه‌های کاربردی را ساده می‌کند، و به شما امکان می‌دهد تا به نکات ظریف فنی امنیت وب بپردازید و دارایی‌های دیجیتال خود را به طور موثر تقویت کنید.

این ابزار یک Proof of Concept است و فقط برای اهداف آموزشی است.
WebSecProbe برای انجام یک سری درخواست های HTTP به یک URL هدف با بارهای مختلف به منظور آزمایش آسیب پذیری های امنیتی بالقوه یا پیکربندی نادرست طراحی شده است. در اینجا یک مرور مختصر از آنچه که کد انجام می دهد آورده شده است:

ورودی کاربر را برای URL هدف و مسیر می گیرد.
فهرستی از بارهای پرداختی را تعریف می‌کند که نشان‌دهنده تغییرات مختلف درخواست HTTP هستند، مانند کاراکترهای کدگذاری شده با URL، سرصفحه‌های خاص و روش‌های مختلف HTTP.
از طریق هر بار بارگذاری تکرار می شود و یک URL کامل با اضافه کردن بار به URL هدف ایجاد می کند.
برای هر URL ساخته شده، یک درخواست HTTP GET با استفاده از کتابخانه درخواست ها ارسال می کند و کد وضعیت پاسخ و طول محتوا را می گیرد.
URL ساخته شده، کد وضعیت، و طول محتوا را برای هر درخواست چاپ می کند، و به طور موثر نتایج پاسخ هر تغییر را از سرور مورد نظر نشان می دهد.
پس از آزمایش تمام بارها، از ماشین Wayback (یک بایگانی وب) درخواست می‌کند تا بررسی کند که آیا عکس‌های فوری آرشیو شده از URL/مسیر هدف وجود دارد یا خیر. در صورت موجود بودن، نزدیکترین اطلاعات بایگانی شده را چاپ می کند.
آیا این ابزار 403 را دور می زند؟

مستقیماً تلاشی برای دور زدن کد وضعیت 403 Forbidden نمی کند. هدف کد بیشتر در مورد آزمایش رفتار سرور در هنگام درخواست های مختلف است، از جمله درخواست هایی با بارهای مختلف، هدرها و تغییرات URL. در حالی که ممکن است برخی از محموله‌ها و هدرهای کد در سناریوهای خاصی برای آزمایش پیکربندی‌های نادرست امنیتی یا ضعف‌ها استفاده شوند، اما تضمین نمی‌کند که کد وضعیت 403 Forbidden را دور بزند.

به طور خلاصه، این کد ابزاری برای کاوش و تجزیه و تحلیل پاسخ‌های یک وب سرور به درخواست‌های مختلف است، اما اینکه آیا می‌تواند کد وضعیت ۴۰۳ Forbidden را دور بزند یا نه، بستگی به تنظیمات و اقدامات امنیتی خاصی دارد که توسط سرور هدف اجرا شده است.





سازگاری با سیستم عامل: اندروید لینوکس ویندوز Macos

    
الزامات:

 پایتون و GIT


 نصب 

 https://pypi.org/project/WebSecProbe/



 اجرا در ترموکس :

 pip install WebSecProbe

 
نحوه اجرا در CLI:


WebSecProbe <URL> <Path> 



مثال:

WebSecProbe https://example.com admin-login
