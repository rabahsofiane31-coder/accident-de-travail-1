خطوات الرفع على GitHub
=======================
1) افتح المستودع Accident-de-travail على github.com
2) اضغط Add file  ->  Upload files
3) اسحب هذه الملفات الأربعة: sw.js , manifest.json , icon-192.png , icon-512.png
4) اضغط Commit changes

5) عدّل index.html (قلم التعديل) وأضف:

   - داخل <head> :
     <link rel="manifest" href="manifest.json">
     <link rel="apple-touch-icon" href="icon-192.png">

   - قبل </body> :
     <script>
     if ('serviceWorker' in navigator) {
       navigator.serviceWorker.register('./sw.js');
     }
     </script>

6) انتظر دقيقة، ثم افتح الرابط وأنت متصل بالإنترنت مرة واحدة.
   بعدها يعمل بدون إنترنت.

ملاحظة: إذا كان في الموقع ملفات أخرى (صور، css، js)
أضف أسماءها في القائمة FILES داخل sw.js.
