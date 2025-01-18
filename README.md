# Tema-SII - Detectarea Știrilor False

Acest proiect are ca scop detectarea știrilor false folosind un model de învățare automată bazat pe rețele neuronale. Modelul utilizează un model pre-antrenat Camembert, care este varianta BERT adaptată pentru limba franceză.

Modelul este antrenat pentru a clasifica articolele de știri în trei categorii:

- **True**: Știri adevărate
- **Fake**: Știri false
- **Biased**: Știri subiective


1. **Preprocesarea datelor**:
   - Textul articolelor a fost tokenizat utilizând tokenizer-ul Camembert, iar etichetele au fost transformate în valori numerice (True = 1, Fake = 0, Biased = 2).
   
2. **Antrenarea modelului**:
   - Modelul Camembert a fost folosit pentru clasificarea secvențelor de text. A fost utilizată o funcție de pierdere de tip Cross-Entropy, iar antrenamentul s-a desfășurat pe 5 epoci cu un set de date de instruire și un set de validare (testare) de 20%.

3. **Evaluarea modelului**:
   - După antrenare, modelul a fost evaluat folosind setul de testare, iar performanța a fost măsurată folosind **acuratețea**.

4. **Rezultate**:
   - Acuratețea obținută pe setul de testare este de **0.836**, ceea ce înseamnă că modelul a prezis corect aproximativ 83.6% dintre etichetele testate.
train.csv: Set de date utilizat pentru antrenare;
test.csv: Set de date utilizat pentru predicții;
predictions.csv: Setul de test completat cu predicțiile.

