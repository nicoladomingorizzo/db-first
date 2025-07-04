# db-first

Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario.

## Table name : Car

<!-- Identificativo univoco dell'auto (es. numero di telaio) -->
ID_Auto | CHAR(17) -NOTNULL UNIQUE
<!-- Marca del veicolo (es. Fiat, BMW, Toyota) -->
Marca | VARCHAR(30) -NOTNULL INDEX
<!-- Modello del veicolo (es. Panda, Serie 3, Yaris) -->
Modello | NOTNULL -INDEX
<!-- Anno di produzione del veicolo -->
Anno | YEAR -NOTNULL INDEX 
<!-- Dettagli specifici del modello (es. 1.2 69cv, 3 porte, Connect) -->
Allestimento | TEXT(1000) -NOTNULL DEFAULT('VERSIONE BASE')
<!-- Colore del veicolo -->
Colore | VARCHAR(20) -NOTNULL DEFAULT('BIANCO')
<!-- Chilometri percorsi -->
Chilometraggio | MEDIUMTEXT - NOTNULL INDEX
<!-- Prezzo di acquisto del veicolo -->
Prezzo_Acquisto | VARCHAR(30) -NOTNULL INDEX 
<!-- Prezzo di vendita del veicolo (se venduto) -->
Prezzo_Vendita | VARCHAR(30) -NOTNULL DEFAULT('---.---') 
<!-- Data di acquisto del veicolo -->
Data_Acquisto | YEAR - 
<!-- Data di vendita del veicolo (se venduto) -->
Data_Vendita |  - 
<!-- Identificativo del proprietario (chiave esterna verso la tabella dei proprietari) -->
Proprietario_ID |  - 
<!-- Stato del veicolo (es. Nuovo, Usato, In Vendita, Venduto) -->
Stato |  - 
<!-- Note aggiuntive (es. difetti, interventi, ecc.) -->
Note |  - 
<!-- Numero di telaio del veicolo -->
Numero_Telaio |  - 
<!-- Tipo di alimentazione (es. Benzina, Diesel, GPL, Elettrico) -->
Alimentazione |  - 
<!-- Cilindrata del motore -->
Cilindrata |  - 
<!-- Potenza del motore -->
Potenza |  - 
<!-- Tipo di cambio (es. Manuale, Automatico) -->
Tipo_Cambio |  - 
<!-- Numero di porte del veicolo -->
Numero_Porte |  - 
<!-- Tipo di carrozzeria (es. Berlina, Coupé, Suv) -->
Tipo_Carrozzeria |  - 
<!-- Optional presenti sul veicolo (lista separata o campo con codici) -->
Optional |  - 
<!-- Tipo di immatricolazione (es. Italiana, Estera) -->
Tipo_Immatricolazione |  - 
<!-- Data di prima immatricolazione -->
Data_Immatricolazione |  - 
<!-- Provenienza del veicolo (es. Importazione, Aziendale) -->
Provenienza |  - 
<!-- Informazioni sui tagliandi (data, officina, descrizione) -->
Tagliandi |  - 
<!-- Informazioni sulla permuta (auto data in permuta, valore) -->
Permuta |  - 
<!-- Informazioni sull'IVA applicata (es. 22%, margine) -->
IVA |  - 
<!-- Sconto applicato al prezzo -->
Sconto |  - 
<!-- Informazioni sulla garanzia (tipo, durata) -->
Garanzia |  - 
<!-- Accessori forniti con il veicolo -->
Accessori |  - 
<!-- Ulteriori note tecniche sul veicolo -->
Note_Tecniche |  - 
<!-- Codice Fiscale del proprietario (se necessario per motivi fiscali) -->
Codice_Fiscale_Proprietario |  - 
<!-- Indirizzo del proprietario (se necessario per motivi fiscali) -->
Indirizzo_Proprietario |  - 
<!-- Città del proprietario (se necessario per motivi fiscali) -->
Citta_Proprietario |  - 
<!-- CAP del proprietario (se necessario per motivi fiscali) -->
CAP_Proprietario |  - 
<!-- Telefono del proprietario (se necessario per motivi fiscali) -->
Telefono_Proprietario |  - 
<!-- Email del proprietario (se necessario per motivi fiscali) -->
Email_Proprietario |  - 