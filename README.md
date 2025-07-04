# db-first

Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario.

## Table name : Car

<!-- Identificativo univoco dell'auto -->
ID_Auto | TEXT -NOTNULL INDEX
<!-- Marca del veicolo  -->
Marca | VARCHAR(30) -NOTNULL INDEX
<!-- Modello del veicolo-->
Modello | NOTNULL -INDEX
<!-- Anno di produzione del veicolo -->
Anno | YEAR -NOTNULL INDEX 
<!-- Dettagli specifici del modello -->
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
Data_Acquisto | TIMESTAMP -NULL
<!-- Data di vendita del veicolo (se venduto) -->
Data_Vendita | TIMESTAMP -NULL
<!-- Identificativo del proprietario -->
Proprietario_ID | VARCHAR(255) -NULL DEFAULT('---') 
<!-- Stato del veicolo-->
Stato | VARCHAR(20) -NOTNULL DEFAULT('IN VENDITA')
<!-- Note aggiuntive -->
Note | TEXT -NULL DEFAULT('NESSUN INTERVENTO EFFETTUATO') 
<!-- Numero di telaio del veicolo -->
Numero_Telaio | CHAR(17) -NOTNULL UNIQUE INDEX 
<!-- Tipo di alimentazione -->
Alimentazione | VARCHAR(50) -NOTNULL DEFAULT('BENZINA') 
<!-- Cilindrata del motore -->
Cilindrata | VARCHAR(15) - NOTNULL DEFAULT('1.6 LITRI')
<!-- Potenza del motore -->
Potenza | VARCHAR(30) -NOTNULL 
<!-- Tipo di cambio -->
Tipo_Cambio | VARCHAR(30) -NOTNULL ('CAMBIO MANUALE') 
<!-- Numero di porte del veicolo -->
Numero_Porte | TINYINT -NULL DEFAULT('5')
<!-- Tipo di carrozzeria -->
Tipo_Carrozzeria | VARCHAR(20) -NOTNULL INDEX DEFAULT('BERLINA') 
<!-- Optional presenti sul veicolo-->
Optional | TEXT -NOTNULL DEFAULT('NESSUN OPTIONAL PRESENTE') 
<!-- Tipo di immatricolazione (es. Italiana, Estera) -->
Tipo_Immatricolazione | VARCHAR(50) -NOTNULL 
<!-- Data di prima immatricolazione -->
Data_Immatricolazione | CHAR(20) -NOTNULL INDEX 
<!-- Provenienza del veicolo (es. Importazione, Aziendale) -->
Provenienza | VARCHAR(100) -NOTNULL INDEX DEFAULT('AZIENDALE') 
<!-- Informazioni sui tagliandi (data, officina, descrizione) -->
Tagliandi | TEXT(1000) -NULL DEFAULT('CHIEDERE PER INFO') 
<!-- Informazioni sulla permuta (auto data in permuta, valore) -->
Permuta | VARCHAR(255) -NULL DEFAULT('CHIEDERE PER INFO') 
<!-- Informazioni sull'IVA applicata (es. 22%, margine) -->
IVA | VARCHAR(255) -NULL DEFAULT('CHIEDERE PER INFO') 
<!-- Sconto applicato al prezzo -->
Sconto | VARCHAR(50) -NULL DEFAULT('CHIEDERE PER INFO') 
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