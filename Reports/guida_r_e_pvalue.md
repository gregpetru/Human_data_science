# Correlazione di Pearson (*r*) e *p*-value  
Guida rapida alla comprensione e al corretto uso

---

## 1. Che cos’è il coefficiente *r* di Pearson?

| Valore di *r* | Significato intuitivo |
|---------------|----------------------|
| **+1,00** | Relazione lineare perfetta crescente: tutti i punti su una retta inclinata verso l’alto. |
| **0,00** | Nessuna relazione lineare (nuvola di punti circolare). |
| **−1,00** | Relazione lineare perfetta decrescente: tutti i punti su una retta inclinata verso il basso. |
| {–1; 0} | Correlazione **negativa** (quando *X* cresce, *Y* tende a diminuire). |
| {0; +1} | Correlazione **positiva** (quando *X* cresce, *Y* tende ad aumentare). |

### 1.1 Formula  
\[
r \;=\; \frac{\operatorname{cov}(X,Y)}{\sigma_X\,\sigma_Y}
\]

### 1.2 Dimensione dell’effetto (linee guida di Cohen)  
| Grandezza | Valore assoluto di *r* |
|-----------|-----------------------|
| Piccolo   | ≈ 0,10 |
| Medio     | ≈ 0,30 |
| Grande    | ≥ 0,50 |

> **Nota:** elevate dimensioni campionarie possono rendere “significativo” anche un *r* molto piccolo: occorre sempre guardare *quanto* è grande l’effetto, non solo il p‑value.

### 1.3 Da *r* a *r²*  
\[
r^{2} = \text{quota di varianza di } Y \text{ spiegata linearmente da } X
\]  
Esempio: *r* = 0,60 ⇒ *r²* = 0,36 ⇒ 36 % della variabilità di *Y* è spiegata (linearmente) da *X*.

### 1.4 Correlazione ≠ causalità  
Un *r* elevato indica solo **co‑variazione** lineare. Non prova che *X* “causi” *Y*.

---

## 2. Differenza fra coefficiente *r* e *p*-value

| Aspetto | coefficiente *r* | *p*-value |
|---------|-----------------|-----------|
| **Che cos’è** | Indice **di direzione e intensità** del legame lineare (–1 ≤ *r* ≤ +1). | **Probabilità**, assumendo *r* = 0 (ipotesi nulla), di osservare un coefficiente almeno altrettanto estremo. |
| **Cosa dice** | “**Quanto** forte è la relazione?”. | “**Quanto** sono solidi i dati nell’indicare che la relazione è diversa da zero?”. |
| **Dipende da** | Configurazione dei dati, *non* dal campione in scala. | Valore di *r* **e** dimensione del campione (*n*). |
| **Formula / test** | \( r = \tfrac{\text{cov}(X,Y)}{\sigma_X\sigma_Y} \) | \( t = r \sqrt{\tfrac{n-2}{1-r^{2}}} \) → si ricava il *p*-value dalla *t*-Student con *(n − 2)* d.f. |
| **Interpretazione tipica** | Vedi linee guida di Cohen. | Confronto con livello di significatività α (0,05, 0,01, …). |
| **Messaggio chiave** | **Quantifica l’effetto**. | **Valuta la credibilità statistica** dell’effetto. |

---

## 3. Esempi pratici

| Scenario | *n* | *r* | *p*-value | Interpretazione |
|----------|-----|-----|-----------|-----------------|
| Campione **enorme** | 10 000 | 0,05 | < 0,001 | Effetto trascurabile ma “significativo” (statisticamente, non praticamente). |
| Campione **piccolo** | 10 | 0,30 | 0,38 | Effetto medio ma “non significativo” → dati insufficienti per concludere. |

---

## 4. In sintesi
- **_r_** → **dimensione dell’effetto** (quanto e in che direzione varia *Y* al variare di *X* in modo lineare).  
- **p‑value** → **evidenza statistica** contro l’ipotesi che l’effetto sia zero.  
- Valutare **entrambi** è essenziale: un *r* piccolo ma “significativo” può essere irrilevante; un *r* grande ma non “significativo” può indicare la necessità di più dati.  
- E, sempre, **correlazione ≠ causalità**.

---

*Preparato per chiarire le basi della correlazione di Pearson e dell’interpretazione del p‑value in analisi statistiche.*
