# Cercetare CLARA

Spațiu public în limba română pentru diseminarea rezultatelor de cercetare ale proiectului CLARA.

## Proiect

Proiectul CLARA - acronim de la **CyberSecurity Learning And Response Agent** - dezvoltă o arhitectură de securitate cibernetică asistată de inteligență artificială, orientată către detecție, analiză, explicare, învățare și sprijin pentru răspuns. Materialele publicate explicit în acest depozit sunt diseminate ca rezultate publice de cercetare open-source sub licența Apache License 2.0, dacă un fișier nu precizează altfel. Această licență publică nu se extinde asupra materialelor CLARA nepublice și nici asupra operelor proprietare protejate prin drepturi de autor ale AI STM LEARNING S.R.L. care nu sunt incluse explicit aici.

Materialele publice din acest depozit sintetizează progresul tehnic și de cercetare fără a publica secrete operaționale, seturi de date private, dovezi interne, credențiale, artefacte proprietare de implementare sau detalii confidențiale.

CLARA este proiectat ca sistem modular și auditabil. Arhitectura este construită în jurul unui nucleu specializat bazat pe modele de limbaj, al unor agenți dedicați securității cibernetice, al utilizării controlate a uneltelor, al execuției trasabile și al unor resurse de cercetare care permit evaluări repetabile și comparabile.

## Finanțare și referințe de proiect

| Câmp | Valoare |
| --- | --- |
| Program | Program Creștere Inteligentă, Digitalizare și Instrumente Financiare |
| Prioritate | P1. Susținerea și promovarea unui ecosistem de CDI atractiv și competitiv în România |
| Obiectiv specific | RSO1.1. Dezvoltarea și sporirea capacităților de cercetare și inovare și adoptarea tehnologiilor avansate |
| Acțiune | Acțiunea 1.1. Sprijin pentru sectorul privat și pentru colaborarea între actorii din sistemul public și mediul de afaceri în domeniul CDI |
| Apel | `PCIDIF/155/PCIDIF_P1/OP1/RSO1.1/PCIDIF_A1` |
| Titlu proiect | CLARA (CyberSecurity Learning And Response Agent) - Soluție inovatoare de securitate cibernetică |
| Cod SMIS | `334596` |
| Contract de finanțare | `390016/28.08.2025` |
| Perioadă de implementare | `29.08.2025 - 28.08.2027` |
| Beneficiar | AI STM LEARNING S.R.L. |
| Regiune de implementare | Regiunea Sud-Est, România |

## Obiectiv

Obiectivul CLARA este cercetarea, proiectarea și validarea unui sistem de securitate cibernetică asistat de inteligență artificială. Sistemul urmărește să ajute operatorii umani să înțeleagă evenimente de securitate, să coreleze dovezi, să primească recomandări de răspuns și să folosească feedback controlat, cu păstrarea auditabilității, confidențialității și securității prin proiectare.

## Direcții principale de cercetare

- **Modele LLM și SLM în securitate cibernetică:** interpretare în limbaj natural, trierea incidentelor, explicații, sinteze și generare de rapoarte.
- **Orchestrare multi-agent pentru securitate cibernetică:** CLARA Core coordonează agenți specializați pentru audit, monitorizare de rețea, analiză de risc în browser și fluxuri defensive viitoare.
- **Utilizarea controlată a uneltelor:** liste de permisiuni, validarea parametrilor, sandboxing, trasabilitate și reducerea riscurilor de injectare prin unelte.
- **Ancorare în cunoaștere:** cunoaștere structurată de securitate, mapări de tip MITRE ATT&CK, reprezentări de tip STIX, RAG/GraphRAG și explicații legate de dovezi.
- **Învățare cu protecția datelor și execuție locală sau edge:** rulare locală, minimizarea fluxurilor de date sensibile, adaptare de tip LoRA, concepte de învățare federată și evaluare cu protecția confidențialității.
- **Date sintetice pentru securitate cibernetică:** jurnale, evenimente de rețea, indicatori sintetici de amenințare și episoade de atac pentru testare repetabilă fără date operaționale reale.
- **Evaluare repetabilă:** cadru de evaluare, înregistrări de evaluare, trasabilitate pe model și versiune, prompturi, apeluri către unelte și rapoarte tehnice comparabile.
- **Execuție distribuită și auditabilă:** cercetare privind orchestrarea edge, auditul imuabil și validarea adversarială controlată.

## Componente principale ale proiectului

| Componentă | Rol |
| --- | --- |
| CLARA Core | Interpretează intenția utilizatorului, planifică, rutează sarcini, agregă rezultate și produce răspunsuri explicative. |
| Agenți specializați | Execută sarcini delimitate de securitate: audit, analiză de rețea, verificări de risc în browser, triere sau raportare. |
| Tool Registry | Controlează ce unelte pot fi apelate, cu ce parametri, cu jurnalizare și politici de execuție. |
| Mesagerie internă | Standardizează cereri, răspunsuri, evenimente, severitate, dovezi, identificatori de corelare și raportarea erorilor. |
| Strat de audit și trasabilitate | Înregistrează decizii de rutare, apeluri către unelte, rezultate ale agenților și răspunsuri finale. |
| Strat de cunoaștere | Ancorează răspunsurile în taxonomii de securitate cibernetică, cunoaștere despre amenințări și referințe aprobate. |
| Pachet de date sintetice | Oferă scenarii de securitate cibernetică repetabile pentru testare, validare și evaluare de modele. |
| Cadru de evaluare | Sprijină măsurarea repetabilă a comportamentului modelelor, agenților și fluxurilor. |
| Strat educațional adaptiv | Componentă planificată pentru învățare, ghidaj și transfer de cunoștințe către utilizatori. |
| Infrastructură de management | Acoperă configurare, monitorizare, control acces și guvernanță operațională. |

## Documente de arhitectură

Directorul de arhitectură are propriul index pentru navigare în GitHub:
[arhitectura/README.md](arhitectura/README.md).
Indexul echivalent în limba engleză este disponibil la
[../en/architecture/README.md](../en/architecture/README.md).

| Subiect | Document |
| --- | --- |
| Roluri AI principale | [arhitectura/ROLURI_AI.md](arhitectura/ROLURI_AI.md) |

## Rapoarte

Directorul de rapoarte are propriul index actualizat:
[rapoarte/README.md](rapoarte/README.md).
Indexul echivalent în limba engleză este disponibil la
[../en/reports/README.md](../en/reports/README.md).

| Română | English |
| --- | --- |
| [rapoarte/RAPORT_01.md](rapoarte/RAPORT_01.md) | [../en/reports/REPORT_01.md](../en/reports/REPORT_01.md) |
| [rapoarte/RAPORT_02.md](rapoarte/RAPORT_02.md) | [../en/reports/REPORT_02.md](../en/reports/REPORT_02.md) |

## Copyright și licență

Copyright (c) 2026 AI STM LEARNING S.R.L. și contribuitorii.

Dacă nu se precizează altfel, doar fișierele și materialele publicate explicit în acest depozit sunt puse la dispoziție sub licența Apache License 2.0. Depozitul conține sinteze publice și materiale de diseminare.

Licența Apache License 2.0 nu acordă drepturi asupra materialelor CLARA nepublice și nici asupra operelor proprietare protejate prin drepturi de autor, software-ului, seturilor de date, modelelor, prompturilor, descrierilor de infrastructură, mărcilor, secretelor comerciale, know-how-ului, datelor personale, credențialelor, conținutului terț sau altor elemente de proprietate intelectuală deținute de AI STM LEARNING S.R.L. care nu sunt incluse explicit aici.

## Notă privind publicarea

Rapoartele din acest depozit sunt sinteze publice de cercetare derivate din rapoarte tehnice ale proiectului. Ele omit intenționat detalii operaționale sensibile, locații interne exacte, credențiale, seturi de date private, dovezi brute, date personale și artefacte de implementare nepublice.
