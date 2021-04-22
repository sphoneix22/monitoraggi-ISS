# Dati monitoraggi settimanali dell'ISS in formato CSV
I dati sono stati riportati a mano dai vari report dell'ISS, pertanto potrebbero esserci degli errori. Inoltre, non tutti i report presentano tutti i dati. 
Ho raccolto i dati per uso personale, ma sono comunque fruibili a chiunque possano servire.
## Strutture file
### monitoraggio-nazionale.csv
Rt nazionale
| Campo | Tipo di dati | Descrizione |
| --- | --- | --- |
| numero_report | integer | Numero del report. |
| inizio_range | date | Data di inizio range del periodo di osservazione del report |
| fine_range | date | Data di fine range del periodio di osservazione del report. |
| data_report | date | Data di pubblicazione del report |
| rt_puntuale | integer | Stima Rt puntuale. |
| rt_range_inizio | integer | Inizio intervallo di confidenza Rt |
| rt_range_fine | integer | Fine intervallo di confidenza Rt |
### monitoraggio-nazionale-latest.csv
Stessa struttura di ``monitoraggi-nazionale.csv`` ma con solo i dati dell'ultimo report pubblicato.
### monitoraggio-regioni.csv
Dati suddivvisi per regione e per report
| Campo | Tipo di dati | Descrizione |
| --- | --- | --- |
| numero_report | integer | Numero del report. |
| inizio_range | date | Data di inizio range del periodo di osservazione del report |
| fine_range | date | Data di fine range del periodio di osservazione del report. |
| data_report | date | Data di pubblicazione del report |
| regione | string | Regione a cui si riferiscono i dati (Per le PA: "P.A Trento", "P.A. Bolzano") |
| nuovi_casi_settimanali | string | Casi rilevati nel periodo di osservazione |
| trend_casi | string | "+", "-", "=" |
| trend_focolai | string | "+", "=", "=" |
| rt_puntuale | integer | Stima Rt puntuale. |
| rt_range_inizio | integer | Inizio intervallo di confidenza Rt |
| rt_range_fine | integer | Fine intervallo di confidenza Rt |
| trasmissione_non_gestibile | bool | Si riferisce al campo della tabella ISS "Dichiarata trasmissione non gestibile in modo efficace con misure locali (zone rosse)" |
| valutazione_probabilità | string | |
| valutazione_impatto | string | |
| compatibilità_rt | integer | Si riferisce al campo della tabella ISS "Compatibilità Rt sintomi puntuale con gli scenari di trasmissione" |
| classificazione_rischio | string | |
| classificazione_alta_tre_settimane | bool | Si riferisce al campo della tabella ISS "Classificazione Alta e/o equiparata ad Alta per 3 o più settimane consecutive" |
### monitoraggio-regioni-latest.csv
Stessa struttura di ``monitoraggio-regioni.csv`` ma con solo con i dati dell'ultimo report disponibile.