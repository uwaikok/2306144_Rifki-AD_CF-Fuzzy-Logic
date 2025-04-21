# 2306144_Rifki-AD_CF-Fuzzy-Logic

**Analisis Perubahan CF**

- Nilai CF gejala **demam** diturunkan dari **0.7 ke 0.2**.
- Meskipun **demam** adalah gejala penting, penurunan kontribusinya (dari 0.56 → 0.16) **tidak menurunkan hasil akhir secara signifikan**.
- Hal ini karena:
  - Gejala lain seperti **"pilek" (0.72)** dan **"bersin" (0.72)** memiliki nilai kontribusi besar.
  - Metode perhitungan CF bersifat *kumulatif*, tetapi semakin tinggi CF total, kontribusi tambahan dari gejala berikutnya akan berkurang karena dikalikan dengan `(1 - CF_total)`.
- Hasil akhir tetap tinggi: **CF diagnosis Flu ≈ 0.99**
  **Kesimpulan**:
Perubahan nilai satu gejala (meskipun penting) tidak selalu berdampak besar jika gejala lain mendukung kuat diagnosis tersebut.

**Analisis FUZZY**
Dalam sistem fuzzy, batas antar kategori tidak tegas (tidak 100% pasti).
- Suhu 28°C dapat:
  - Derajat keanggotaan ≈ 1 di "Nyaman" (puncak)
  - Derajat keanggotaan ≈ 0.2–0.3 di "Panas" (awal naik)
- Ini memungkinkan sistem fuzzy mempertimbangkan kondisi ambigu seperti "sedikit panas" atau "nyaman tapi mulai panas".
