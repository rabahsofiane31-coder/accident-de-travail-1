# سجل دخول وخروج العمال — SOMIPHOS
# Registre d'entrée et de sortie des travailleurs — SOMIPHOS

تطبيق ويب في ملف واحد (`index.html`)، يعمل **بدون إنترنت** وبدون أي خادم أو مكتبة خارجية.
Application web en un seul fichier (`index.html`), fonctionne **hors ligne**, sans serveur ni bibliothèque externe.

## المزايا / Fonctionnalités
- رمز سري من 6 أرقام عند الدخول / Code secret à 6 chiffres
- واجهة بالعربية والفرنسية / Interface arabe et français
- وثيقة حسب التاريخ والفوج (1، 2، 3) وصفحتان لكل فوج / Document par date, équipe (1, 2, 3) et 2 pages
- القيد ← الاسم واللقب والمصلحة تلقائيًا من قاعدة البيانات / Matricule → nom et service automatiques
- حساب ساعات العمل تلقائيًا / Calcul automatique des heures
- طباعة كل صفحة في ورقة A4 واحدة مع الترويسة والإمضاءات / Impression : une feuille A4 par page
- قاعدة بيانات العمال برمز سري خاص، مع استيراد جماعي ونسخ احتياطي وحذف الكل / Base de données protégée par un code distinct

## الاستعمال محليًا / Utilisation locale
افتح `index.html` في المتصفح بالنقر المزدوج. / Ouvrez `index.html` dans le navigateur.

## النشر على GitHub Pages / Publication
1. ارفع الملفات إلى مستودع جديد. / Poussez les fichiers dans un dépôt.
2. من **Settings ← Pages** اختر **Deploy from a branch**، ثم الفرع `main` والمجلد `/ (root)`.
3. يظهر الرابط بعد دقائق. / Le lien apparaît après quelques minutes.

## البيانات والخصوصية / Données et confidentialité
- بيانات العمال والوثائق تُحفظ **في متصفح كل جهاز فقط** (localStorage)، ولا تُرسل إلى أي خادم ولا توجد في المستودع.
  Les données restent **dans le navigateur de chaque appareil** ; rien n'est envoyé ni stocké dans le dépôt.
- لنقل البيانات بين الأجهزة استعمل «حفظ نسخة احتياطية» ثم «استرجاع نسخة».
  Pour transférer les données, utilisez « Sauvegarder » puis « Restaurer ».
- لا ترفع ملفات النسخ الاحتياطي (`backup_*.json`) إلى GitHub لأنها تحتوي أسماء العمال (مستبعدة في `.gitignore`).
  Ne publiez pas les sauvegardes (`backup_*.json`) : elles contiennent des noms de travailleurs.
- الرمز السري يقفل الوصول من داخل التطبيق فقط، وليس تشفيرًا حقيقيًا للبيانات.
  Le code secret verrouille l'accès dans l'application ; ce n'est pas un chiffrement des données.
