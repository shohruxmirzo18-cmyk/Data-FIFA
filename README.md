[16/10/26 18:17] FIFA World Cup 2026 Player Performance Analysis Ushbu loyiha Kaggle platformasidagi "FIFA World Cup 2026 Player Performance Dataset" simulyatsiya qilingan ma'lumotlar to'plami asosida tayyorlangan. Loyihada Excel (Pivot Table, Dashboard, Formulalar) hamda Python (Pandas, Matplotlib/Seaborn) imkoniyatlaridan foydalanib, o'yinchilar va jamoalarning statistik samaradorligi tahlil qilingan hamda ikkala vosita natijalari o'zaro solishtirilgan.

📌 Dataset Tavsifi Qatorlar soni: 54 600 ta

Ustunlar soni: 75 ta

Noyob ko'rsatkichlar: 1 248 ta noyob o'yinchi, 1 050 ta o'yin, 48 ta jamoa

Pozitsiyalar: Goalkeeper, Defender, Midfielder, Forward

Ma'lumotlar sifati: O'tkazib yuborilgan qiymatlar (NULL/NaN) va dublikatlar mavjud emas.

🎯 Loyiha Tuzilmasi Loyiha ikkita asosiy bosqichda va fayllar ko'rinishida taqdim etilgan:

fifa_analysis.xlsx:

Data: Rasmiy Excel jadvaliga aylantirilgan barcha 54 600 qatorli ma'lumotlar (match_date Date formatida, pass_accuracy hamda save_percentage Percentage formatida). Yomon zarbalarda xatolik bermasligi uchun goal_conversion_rate = IFERROR(goals / shots, 0) ustuni qo'shilgan.

Tekshiruv: COUNTBLANK va Remove Duplicates yordamida ma'lumotlar tozaligi tasdiqlangan bo'lim.

Pivot 1-6: 6 ta alohida varaqda yaratilgan Pivot jadval va ko'rsatkichlar.

Dashboard: 4 ta KPI karta, 3 ta asosiy diagramma (Top-10 bombardirlar, bosqichlar bo'yicha gollar va pozitsiyalar taqsimoti) hamda interaktiv team va tournament_stage Slicer-lari bilan jihozlangan yaxlit ekranli boshqaruv paneli.

Xulosalar: Har bir Pivot jadval natijalaridan kelib chiqqan holda yozilgan tahliliy xulosalar.

fifa_analysis.ipynb:

Pandas yordamida ma'lumotlarni o'qish, strukturaviy tahlil (.info(), .describe()).

Excel'dagi Pivot Table 1-6 natijalarini Python (groupby, pd.crosstab) orqali qayta hosil qilish va tasdiqlash.

Visual tahlil uchun Matplotlib va Seaborn grafiklari.

📊 Asosiy 5 ta Tahliliy Xulosa Eng Ko'p Gol Urgan Jamoa va Hujum Korrelyatsiyasi:

Pivot 1 natijalariga ko'ra, eng ko'p gol urgan Top-10 jamoalar ro'yxatini shakllantirildi. Yuqori pozitsiyadagi jamoalarda zarbalarning golga aylanish ko'rsatkichi (goal_conversion_rate) sezilarli darajada yuqori ekani kuzatildi.

Pozitsiyalar bo'yicha O'rtacha Reyting va Pas Aniqligi:

Pivot 2 va Python groupby('position') tahlillariga ko'ra, Midfielder va Forward pozitsiyalaridagi o'yinchilar eng yuqori o'rtacha reytingga (player_rating) ega bo'ldi. Pas berish aniqligi (pass_accuracy) bo'yicha esa yarim himoyachilar eng barqaror ko'rsatkichni namoyish etdi.

Tarkib Qiymati va Natijadorlik Bog'liqligi:

Pivot 4 tahlili orqali eng yuqori bozor qiymatiga (market_value_eur) ega 10 ta jamoa aniqlandi. Tahlillar shuni ko'rsatdiki, tarkib qiymatining yuqoriligi har doim ham urilgan gollar sonining mutlaq yetakchiligini kafolatlamaydi, ammo o'yinchilarning individual reytingiga ijobiy ta'sir ko'rsatadi.

Turnirning Eng Samarali Bombardirlari:

Pivot 5 bo'yicha uzatilgan paslar va urilgan gollar yig'indisi (goals + assists) bo'yicha Top-10 o'yinchilar saralab olindi. Eng yaxshi 3 ta bombardir o'yinchining samaradorlik indeksi umumiy jamoa gollarining salmoqli qismini tashkil etdi.

Zarba Samaradorligi (goal_conversion_rate) Bo'yicha Yetakchilar:

Pivot 6 tahlilida darvozaga berilgan zarbalarning golga aylanish ko mezoniga ko'ra top-5 jamoa aniqlandi. Ba'zi kamroq zarba bergan jamoalar yuqori aniqlik hisobiga zarba samaradorligi bo'yicha yetakchi o'rinlarni egallagani ma'lum bo'ldi.

🔄 Excel va Python Natijalarining Solishtiruvi Excel'dagi Pivot Table hamda Python'dagi Pandas (groupby, pd.crosstab) orqali olingan barcha ko'rsatkichlar 100% bir xil natijani berdi.

Yaxlitlash va Saralash: Python groupby bajarilganda sukut bo'yicha (default) indekslar bo'yicha saralaydi, Excel Pivot Table esa qiymatlar bo'yicha saralaydi. Python'da .sort_values(ascending=False) qo'llanilgach, ikkala vositadagi jadval ketma-ketligi to'liq mos keldi.
[16/10/26 18:17] Muhammadali: Nollarga bo'lish (ZeroDivision): Excel'da IFERROR(goals / shots, 0) ishlatilgan bo'lsa, Python'da .fillna(0) funksiyasi qo mezon qilinib, NaN qiymatlari nolga tenglashtirildi va hisob-kitoblar aniqligi ta'minlandi.

🛠 Ishlatilingan Texnologiyalar Excel: Pivot Tables, Conditional Formatting, Slicers, Data Validation, Excel Dashboards.

Python 3.x: pandas, numpy, matplotlib, seaborn.

Jupyter Notebook / Google Colab.

