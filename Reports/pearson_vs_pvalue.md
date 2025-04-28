# Differenza fra coefficiente *r* di Pearson e *p*-value

| Aspetto | Coefficiente *r* | *p*-value |
|---------|-----------------|-----------|
| **Che cos’è** | Numero tra –1 e +1 che misura **direzione e intensità** della relazione lineare. | **Probabilità**, sotto l’ipotesi nulla (r = 0), di ottenere un coefficiente almeno altrettanto estremo. |
| **Cosa dice** | “**Quanto** sono legate le due variabili in modo lineare?” (grandezza dell’effetto). | “**Se** l’effetto osservato può essere attribuito al caso” (significatività statistica). |
| **Dipende da** | - Configurazione dei dati.<br>- Non dipende da *n* in termini di scala (resta sempre in ±1). | - Valore di *r*.<br>- **Dimensione del campione** (*n*). |
| **Formula / test** | \( r = \dfrac{\text{cov}(X,Y)}{\sigma_X\sigma_Y} \) | \( t = r \sqrt{\dfrac{n-2}{1-r^{2}}} \) → confronto con la *t*-Student a *(n − 2)* d.f. |
| **Interpretazione tipica** | \|r\| ≈ 0,10 → piccolo<br>\|r\| ≈ 0,30 → medio<br>\|r\| ≥ 0,50 → grande | Confronto con livello α (es. 0,05).<br>• *p* < α ⇒ effetto “significativo”.<br>• *p* ≥ α ⇒ effetto “non significativo”. |
| **Messaggio chiave** | **Quanto** forte è la relazione. | **Quanto** sono solidi i dati nell’indicare che la relazione non è zero. |

---

## Esempi pratici

1. **Campione enorme (n = 10 000)**  
   *r* = 0,05 → effetto trascurabile, ma *p* < 0,001 ⇒ statisticamente “significativo”.

2. **Campione piccolo (n = 10)**  
   *r* = 0,30 → effetto medio, ma *p* = 0,38 ⇒ non significativo (dati insufficienti).

---

## In sintesi

- **_r_** descrive **intensità e direzione** del legame lineare → **dimensione dell’effetto**.  
- Il **p‑value** misura **l’evidenza statistica** contro l’ipotesi di nessuna correlazione.  
- Puoi ottenere *p* piccoli con *r* minuscoli (effetto irrilevante ma “significativo”) e viceversa.  
- Una corretta interpretazione richiede di **valutare entrambi insieme** (e il contesto applicativo).
