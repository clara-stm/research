# Cercetare CLARA

Zonă publică în limba română pentru diseminarea rezultatelor de cercetare ale proiectului CLARA.

## Proiect

CLARA înseamnă **CyberSecurity Learning And Response Agent**. Proiectul dezvoltă o arhitectură de securitate cibernetică asistată de inteligență artificială, orientată către detecție, analiză, explicație, învățare și sprijin pentru răspuns. Materialele publicate expres în acest repository sunt diseminate ca artefacte publice de cercetare open-source sub licența Apache License 2.0, dacă un fișier nu precizează altfel. Această licență publică nu include materialele CLARA nepublice și nici operele protejate prin drepturi de autor proprietare ale AI STM LEARNING S.R.L. care nu sunt incluse expres aici.

Materialele publice din acest repository sintetizează progresul tehnic și de cercetare fără a publica secrete operaționale, seturi de date private, dovezi interne, credențiale, artefacte proprietare de implementare sau detalii confidențiale de implementare.

CLARA este poziționat ca sistem modular și auditabil, construit în jurul unui nucleu specializat bazat pe modele de limbaj, agenți specializați pentru securitate cibernetică, utilizare controlată a uneltelor, execuție trasabilă și active de cercetare pentru evaluare reproductibilă.

## Finanțare Și Referințe De Proiect

| Câmp | Valoare |
| --- | --- |
| Program | Program Creștere Inteligentă, Digitalizare și Instrumente Financiare |
| Prioritate | P1. Susținerea și promovarea unui ecosistem de CDI atractiv și competitiv în România |
| Obiectiv specific | RSO1.1. Dezvoltarea și sporirea capacităților de cercetare și inovare și adoptarea tehnologiilor avansate |
| Acțiune | Acțiunea 1.1. Sprijin pentru sectorul privat și pentru colaborarea între actorii din sistemul public și mediul de afaceri în domeniul CDI |
| Apel | `PCIDIF/155/PCIDIF_P1/OP1/RSO1.1/PCIDIF_A1` |
| Titlu proiect | CLARA (CyberSecurity Learning And Response Agent) - Soluție Inovativă de Securitate Cibernetică |
| Cod SMIS | `334596` |
| Contract de finanțare | `390016/28.08.2025` |
| Perioadă de implementare | `29.08.2025 - 28.08.2027` |
| Beneficiar | AI STM LEARNING S.R.L. |
| Regiune de implementare | Regiunea Sud-Est, România |

## Obiectiv

Obiectivul CLARA este cercetarea, proiectarea și validarea unui sistem de securitate cibernetică asistat de AI, capabil să sprijine operatorii umani în înțelegerea evenimentelor de securitate, corelarea evidențelor, recomandarea acțiunilor de răspuns și învățarea din feedback controlat, păstrând în același timp auditabilitatea, confidențialitatea și constrângerile de securitate prin design.

## Direcții Principale De Cercetare

- **LLM și SLM în securitate cibernetică:** interpretare în limbaj natural, triere incidente, explicații, sumarizare și generare de rapoarte.
- **Orchestrare multi-agent pentru cybersecurity:** CLARA Core coordonează agenți specializați pentru audit, monitorizare rețea, analiză risc browser și fluxuri defensive viitoare.
- **Utilizare controlată a uneltelor:** allowlist, validare de parametri, sandboxing, trasabilitate și reducerea riscurilor de tool-injection.
- **Ancorare în cunoaștere:** cunoaștere structurată de securitate, mapări de tip MITRE ATT&CK, reprezentări de tip STIX, RAG/GraphRAG și explicații legate de evidențe.
- **Învățare cu protecția datelor și execuție pe edge:** rulare locală, minimizarea fluxurilor de date sensibile, adaptare de tip LoRA, concepte de învățare federată și evaluare cu protecția confidențialității.
- **Date sintetice de securitate cibernetică:** loguri, evenimente de rețea, înregistrări de tip threat intelligence și episoade de atac pentru testare repetabilă fără date operaționale reale.
- **Evaluare reproductibilă:** evaluation harness, eval records, trasabilitate pe model/versiune, prompturi, tool-calls și rapoarte tehnice comparabile.
- **Execuție distribuită și auditabilă:** aliniere de cercetare cu orchestrare edge, audit imuabil și validare adversarială controlată.

## Componente Principale Ale Proiectului

| Componentă | Rol |
| --- | --- |
| CLARA Core | Interpretează intenția utilizatorului, planifică, rutează sarcini, agregă rezultate și produce răspunsuri explicative. |
| Agenți specializați | Execută sarcini focalizate de securitate: audit, analiză rețea, verificări risc browser, triere sau raportare. |
| Tool Registry | Controlează ce unelte pot fi apelate, cu ce parametri, cu logare și politici de execuție. |
| Mesagerie internă | Standardizează cereri, răspunsuri, evenimente, severitate, evidențe, correlation ID și raportarea erorilor. |
| Strat de audit și trace | Înregistrează decizii de rutare, apeluri de tool, rezultate de agenți și răspunsuri finale. |
| Strat de cunoaștere | Ancorează răspunsurile în taxonomii cyber, cunoaștere despre amenințări și referințe aprobate. |
| Pachet de date sintetice | Oferă scenarii cyber repetabile pentru testare, validare și evaluare de modele. |
| Evaluation harness | Sprijină măsurarea reproductibilă a comportamentului modelelor, agenților și fluxurilor. |
| Strat educațional adaptiv | Componentă planificată pentru învățare, ghidaj și transfer de cunoștințe către utilizatori. |
| Infrastructură de management | Acoperă configurare, monitorizare, control acces și guvernanță operațională. |

## Documente De Arhitectură

| Subiect | Document |
| --- | --- |
| Roluri AI principale | [arhitectura/ROLURI_AI.md](arhitectura/ROLURI_AI.md) |

## Rapoarte

| Română | English |
| --- | --- |
| [rapoarte/RAPORT_01.md](rapoarte/RAPORT_01.md) | [../en/reports/REPORT_01.md](../en/reports/REPORT_01.md) |
| [rapoarte/RAPORT_02.md](rapoarte/RAPORT_02.md) | [../en/reports/REPORT_02.md](../en/reports/REPORT_02.md) |

## Copyright Și Licență

Copyright (c) 2026 AI STM LEARNING S.R.L. și contribuitorii.

Dacă nu se precizează altfel, doar fișierele și materialele publicate expres în acest repository sunt puse la dispoziție sub licența Apache License 2.0. Repository-ul conține sinteze publice și materiale de diseminare.

Licența Apache License 2.0 nu acordă drepturi asupra materialelor CLARA nepublice și nici asupra operelor protejate prin drepturi de autor proprietare, software-ului, seturilor de date, modelelor, prompturilor, descrierilor de infrastructură, mărcilor, secretelor comerciale, know-how-ului, datelor personale, credențialelor, conținutului terț sau altor elemente de proprietate intelectuală deținute de AI STM LEARNING S.R.L. care nu sunt incluse expres aici.

## Notă Privind Publicarea

Rapoartele din acest repository sunt sinteze publice de cercetare derivate din rapoarte tehnice ale proiectului. Ele omit intenționat detalii operaționale sensibile, locații interne exacte, credențiale, seturi de date private, dovezi brute, date personale și artefacte de implementare nepublice.
