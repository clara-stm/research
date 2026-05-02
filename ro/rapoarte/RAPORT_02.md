# RAPORT 02 - Sinteză publică de cercetare CLARA

| Câmp | Valoare |
| --- | --- |
| Proiect | CLARA - CyberSecurity Learning And Response Agent |
| Tip document | Sinteză publică a raportului tehnic/de cercetare |
| Raport sursă | Raport Tehnic nr. 2 |
| Perioadă acoperită | Consolidare arhitectură, cercetare LLM avansată, date sintetice |
| Limbă | Română |
| Statut | Material public de diseminare |

## 1. Rezumat

Al doilea raport tehnic CLARA documentează consolidarea fundamentelor de cercetare și avansul de la arhitectură conceptuală către validare operațională. Activitățile s-au concentrat pe închiderea etapelor inițiale de analiză și arhitectură, definirea capabilităților defensive măsurabile și punerea în funcțiune inițială a unui pachet mare de date sintetice pentru evaluare reproductibilă.

În această etapă, CLARA este descris ca ecosistem compus din CLARA Core, agenți specializați, Tool Registry, comunicații descentralizate, audit imuabil, platformă educațională adaptivă și infrastructură de management. Raportul marchează trecerea de la cerințe și prototipare minimală la metodologie de evaluare, guvernanță a datelor și pregătire pentru experimente controlate.

## 2. Obiectivul Perioadei

Obiectivul perioadei a fost reducerea riscului tehnic prin consolidarea proiectării și pregătirea validării repetabile. Activitățile au urmărit:

- finalizarea logică a analizei fundamentale și arhitecturii conceptuale;
- definirea unei taxonomii de sarcini defensive pentru fluxuri SOC;
- proiectarea unei metodologii de evaluare reproductibile;
- integrarea datelor sintetice ca suport de testare fără date reale;
- definirea controalelor de siguranță pentru sisteme LLM agentice;
- pregătirea criteriilor de recepție pentru interfața web, fără declararea recepției finale în această etapă.

## 3. Consolidarea Fundamentării Științifice

Raportul extinde analiza literaturii și a cadrelor relevante pentru un sistem distribuit de detecție și răspuns la incidente. Direcțiile consolidate includ:

- orchestrare descentralizată și reducerea punctelor unice de eșec;
- red-teaming continuu și telemetrie proactivă;
- adaptare eficientă a modelelor prin LoRA și concepte de învățare federată;
- guvernanță și siguranță pentru aplicații LLM prin NIST AI RMF și OWASP Top 10 for LLM Applications;
- reprezentare standardizată a cunoașterii prin STIX, MITRE ATT&CK, RAG și GraphRAG.

Rezultatul este o orientare clară: CLARA trebuie să combine infrastructură distribuită, învățare adaptivă, ancorare în cunoaștere și controale stricte pentru execuția agentică.

## 4. Ecosistemul CLARA Pe Șapte Componente

Al doilea raport rafinează arhitectura conceptuală într-un ecosistem cu șapte componente principale:

| Componentă | Rol |
| --- | --- |
| CLARA Core | Nucleu cognitiv și orchestrator al solicitărilor, agenților și răspunsurilor. |
| Agenți specializați | Module pentru audit, rețea, browser și alte sarcini cyber defensive. |
| Tool Registry | Registru de capabilități și unelte, cu politici, validare și trasabilitate. |
| Magistrală de comunicații descentralizată | Schimb de mesaje agent-agent și agent-tool în condiții de reziliență. |
| Sistem de audit imuabil | Trasabilitate, non-repudiere și verificabilitate a deciziilor. |
| Platformă educațională adaptivă | Ghidaj și învățare pentru operatori și utilizatori. |
| Infrastructură de management | Configurare, monitorizare, politici, acces și operare. |

Mecanismele tehnice cheie includ optimizare pentru inferență, quantizare, RAG/GraphRAG, memorie contextuală, sandboxing, controlul privilegiilor și audit pe ciclul de viață.

## 5. Cercetare LLM Avansată Pentru Cybersecurity

Raportul mută accentul de la arhitectură generală la funcții defensive măsurabile. A fost definită o taxonomie de tip "cyber normal" pentru sarcini relevante în fluxuri SOC:

- triere de incidente;
- corelare de evenimente multi-sursă;
- mapare la MITRE ATT&CK;
- prioritizare de vulnerabilități;
- recomandări de remediere;
- raportare structurată și audit;
- extragere și modelare de informații CTI;
- clasificare de telemetrie și secvențe;
- analiză de anomalii și diagnostic asistat.

LLM-ul este tratat ca mijloc, nu ca obiectiv în sine. Performanța trebuie măsurată prin criterii cyber: calitatea trierii, reducerea falselor pozitive, acuratețea mapării, utilitatea recomandărilor și calitatea evidențelor.

## 6. Evaluare Reproductibilă

O contribuție importantă a raportului 2 este definirea unei metodologii de evaluare reproductibile:

- **evaluation harness:** suită de scenarii și teste controlate;
- **eval record:** înregistrare completă a versiunii modelului, prompturilor, tool-calls, intrărilor, ieșirilor, referințelor de date și logurilor;
- **data refs:** referințe stabile către versiuni de date;
- **comparabilitate temporală:** posibilitatea de a compara rezultate între iterații.

Această abordare răspunde riscurilor precum drift de distribuție, reward hacking, sandbagging, tool-injection și lipsa trasabilității în evaluările AI.

## 7. Date Sintetice Pentru Validare

Raportul documentează punerea în funcțiune inițială a unui pachet de date sintetice de securitate cibernetică. Pachetul combinat are aproximativ 300 GB și include două tranșe de câte aproximativ 150 GB. Datele sunt declarate sintetice și sunt proiectate pentru testare fără date operaționale reale, PII sau credențiale.

Structura sintetizată a pachetului:

| Categorie | Rol |
| --- | --- |
| Network | Evenimente de trafic de rețea, DNS, HTTP, TCP, TLS, SMB și fluxuri similare. |
| Logs | Jurnale de autentificare, procese, fișiere, aplicații și schimbări de configurare. |
| Episodes | Scenarii de atac și secvențe relevante pentru validare. |
| Threat Intel | Indicatori sintetici și informații de tip threat-intelligence-like. |
| Docs | Documente sintetice și metadate pentru scenarii de conformitate. |

Indicatori publicabili din raportul sursă:

- aproximativ 300,06 GB total;
- peste 573 milioane evenimente cumulate;
- peste 10.000 fișiere cumulate;
- 21 tipuri distincte de evenimente;
- 20 scenarii de atac prezente în ambele livrabile;
- validare de schemă declarată 100%;
- hash-uri SHA-256 și manifest pentru verificarea integrității;
- adrese IP private, domenii sintetice și identități generate sintetic.

## 8. Pregătirea Interfeței Web

Raportul precizează că pentru interfața web CLARA au fost definite criterii de pregătire și recepție, dar nu a fost declarată punerea în funcțiune finală în perioada raportată. Criteriile includ RBAC, autentificare, fluxuri de verificare, resetare, 2FA/TOTP și audit pentru evenimente UI/API.

## 9. Riscuri Și Controale

| Risc | Control propus |
| --- | --- |
| Prompt injection și output handling nesigur | Validare intrări/ieșiri, sandboxing, privilegii minime, audit. |
| Autonomie excesivă a agenților | Politici de tool-calling, limite de execuție și control uman. |
| Integritate slabă a evaluării | Evaluation harness, eval record și data refs stabile. |
| Expunerea datelor operaționale | Date sintetice, manifest, hashing și separare de date reale. |
| Tool-injection | Tool Registry, allowlist, jurnalizare completă a apelurilor. |
| Drift sau comparații nereproductibile | Versionare modele/date/prompturi și rapoarte comparabile. |

## 10. Rezultate

Al doilea raport marchează patru rezultate majore:

- consolidarea arhitecturii CLARA în jurul a șapte componente;
- definirea taxonomiei de sarcini defensive pentru evaluarea capabilităților LLM/agentice;
- proiectarea metodologiei de evaluare reproductibile;
- punerea în funcțiune inițială a pachetului de date sintetice pentru validare fără date reale.

## 11. Pași Următori

Direcțiile pentru etapa următoare includ:

- transpunerea arhitecturii conceptuale într-un prototip funcțional;
- operaționalizarea evaluation harness și eval record;
- conectarea controlată la pachetul de date sintetice;
- experimente cu selecție de model, RAG/GraphRAG, LoRA și învățare federată;
- hardening de securitate pentru tool-calls, sandboxing, output validation și audit;
- continuarea pregătirii și testării interfeței web.

## 12. Referințe Selective

Raportul sursă folosește repere precum NIST AI RMF, OWASP Top 10 for LLM Applications, STIX 2.1, MITRE ATT&CK, RAG/GraphRAG, LoRA, federated learning, metodologii de red-teaming și bune practici pentru auditabilitate și guvernanță AI.

## 13. Notă De Publicare

Acest document este o sinteză publică. Nu include setul de date, fișiere brute, manifest intern complet, hash-uri concrete, locații de stocare, proceduri operaționale detaliate, credențiale, endpoint-uri sau materiale confidențiale.
