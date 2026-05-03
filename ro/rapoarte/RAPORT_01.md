# RAPORT 01 - Sinteză publică de cercetare CLARA

| Câmp | Valoare |
| --- | --- |
| Proiect | CLARA - CyberSecurity Learning And Response Agent |
| Tip document | Sinteză publică a raportului tehnic/de cercetare |
| Raport sursă | Raport Tehnic nr. 1 |
| Perioadă acoperită | Fundamentare inițială, analiză tehnică și arhitectură conceptuală |
| Limbă | Română |
| Statut | Material public de diseminare |

## 1. Rezumat

Primul raport tehnic CLARA documentează trecerea de la ideea de produs la o fundație tehnică verificabilă. Activitatea a urmărit definirea cerințelor, înțelegerea stadiului tehnologic pentru inteligența artificială aplicată în securitate cibernetică și proiectarea unei arhitecturi multi-agent care poate fi extinsă incremental.

Proiectul CLARA este conceput ca sistem de securitate cibernetică asistat de inteligență artificială. În această arhitectură, nucleul de orchestrare CLARA Core interpretează solicitări în limbaj natural, selectează agenți specializați, controlează apelurile către unelte și produce răspunsuri explicabile. Direcția de cercetare combină modele de limbaj, agenți specializați, auditabilitate, confidențialitate, feedback de la experți și posibilitatea rulării locale în scenarii sensibile.

## 2. Obiectivul perioadei

Obiectivul principal a fost reducerea riscului de proiectare printr-o tranziție controlată de la analiză la prototip. Echipa a urmărit:

- definirea cerințelor funcționale și non-funcționale;
- stabilirea criteriilor de acceptanță pentru demonstrații tehnice;
- documentarea literaturii relevante despre LLM/SLM, sisteme multi-agent și securitate cibernetică;
- proiectarea arhitecturii conceptuale CLARA;
- validarea timpurie printr-un schelet funcțional de orchestrare.

## 3. Direcții de cercetare analizate

### 3.1 Modele de limbaj pentru securitate cibernetică

Raportul analizează modul în care modelele de limbaj pot sprijini interpretarea evenimentelor, explicarea alertelor, sintetizarea investigațiilor, generarea de recomandări și producerea de rapoarte tehnice. În CLARA, modelul de limbaj nu este tratat ca înlocuitor al operatorului uman, ci ca o componentă de augmentare care ajută la structurarea informației și la formularea unor explicații utile.

### 3.2 Agenți specializați

Arhitectura separă nucleul de orchestrare de agenții specializați. Agenții pot acoperi sarcini precum audit local, analiză de rețea, protecție browser sau verificări de configurare. Această separare permite evoluția independentă a componentelor și limitează impactul erorilor.

### 3.3 Confidențialitate și rulare locală

Raportul pune accent pe rularea locală sau controlată a agenților, minimizarea datelor trimise către componente centrale și mascarea informațiilor sensibile în jurnale. Au fost analizate concepte precum învățarea federată, confidențialitatea diferențială, criptarea și anonimizarea, ca posibile mecanisme pentru etapele ulterioare.

### 3.4 Apelarea controlată a uneltelor

Pentru a limita riscurile de abuz, CLARA introduce de la început un Tool Registry cu liste de permisiuni, validarea parametrilor, limite de timp, jurnalizare și politici de execuție. Această decizie este importantă pentru sistemele agentice, unde un model poate solicita acțiuni externe prin unelte.

### 3.5 Auditabilitate și explicabilitate

Auditul nu este adăugat ulterior, ci este introdus ca cerință de bază. Evenimentele de tip decizie de rutare, apel către unealtă, rezultat de agent și răspuns final permit reconstruirea traseului decizional și susțin explicații verificabile.

## 4. Arhitectura conceptuală

Prima arhitectură CLARA include următoarele componente:

| Componentă | Rol în raportul 1 |
| --- | --- |
| CLARA Core | Interpretează solicitări, planifică, rutează sarcini și agregă rezultatele. |
| Agenți specializați | Execută sarcini delimitate de securitate cibernetică și returnează rezultate structurate. |
| Tool Registry | Controlează apelurile către unelte și reduce suprafața de atac. |
| Mesagerie internă | Standardizează cererile, răspunsurile și evenimentele de audit. |
| Audit și trasabilitate | Înregistrează deciziile, apelurile către unelte și răspunsurile finale. |
| Platformă educațională | Componentă planificată pentru instruire și transfer de cunoștințe. |

Fluxul validat la nivel conceptual este:

1. Utilizatorul transmite o solicitare în limbaj natural.
2. CLARA Core interpretează solicitarea și generează un plan minimal.
3. Orchestratorul selectează agenții potriviți.
4. Agenții execută sarcini prin interfețe standardizate.
5. Rezultatele sunt agregate într-un răspuns explicativ.
6. Auditul înregistrează traseul execuției.

## 5. Cerințe inițiale

Raportul definește cerințe funcționale precum interpretarea comenzilor în limbaj natural, rutarea către agenți, agregarea rezultatelor, explicarea alertelor și generarea de rapoarte. Cerințele non-funcționale includ confidențialitate, auditabilitate, performanță, extensibilitate și securitate prin proiectare.

Exemple de criterii de acceptanță definite în această etapă:

- CLARA poate produce un plan coerent pentru scenarii predefinite.
- Solicitările sunt rutate către agentul potrivit.
- Răspunsurile includ sinteză, dovezi, recomandări și pași următori.
- Datele sensibile sunt mascate în jurnale.
- Fiecare scenariu demonstrativ are un jurnal de audit.
- Un agent nou poate fi adăugat prin interfața standard și înregistrare în registru.

## 6. Prototipare inițială

Prototipul inițial a fost construit pentru a valida fluxul cap-coadă, nu pentru a livra o implementare completă. Elementele demonstrate includ:

- schelet de orchestrare pentru CLARA Core;
- mecanism minimal de rulare a agenților;
- format standard pentru AgentRequest, AgentResponse și CoreEvent;
- Tool Registry inițial cu listă de permisiuni;
- jurnal local pentru audit și trasabilitate;
- componentă minimală pentru Agentul de Audit;
- scenarii minime de integrare și documentație de rulare.

Această abordare a redus riscul de supra-complexitate și a permis testarea timpurie a deciziilor arhitecturale.

## 7. Cooperare și execuție distribuită

Raportul include o direcție de cercetare privind execuția distribuită și auditul imuabil. Au fost analizate concepte de orchestrare edge, execuție containerizată și validare adversarială controlată. Scopul acestei direcții este evaluarea fezabilității pentru scenarii în care agenții CLARA rulează pe infrastructuri distribuite, cu dovezi verificabile ale execuției.

## 8. Riscuri identificate

| Risc | Măsură de reducere |
| --- | --- |
| Cerințe ambigue și extindere necontrolată a scopului | Backlog structurat, criterii de acceptanță și delimitarea demonstrației de concept. |
| Explicabilitate greu de adăugat ulterior | Audit și trasabilitate introduse ca cerințe de bază. |
| Expunerea datelor sensibile | Confidențialitate prin proiectare, mascarea jurnalelor și opțiuni de rulare locală. |
| Apelare nesigură a uneltelor | Tool Registry, liste de permisiuni, validarea parametrilor și jurnalizare. |
| Agregare incoerentă multi-agent | Scheme standard pentru rezultate, severitate și dovezi. |

## 9. Rezultate

Primul raport stabilește fundația CLARA:

- cerințe funcționale și non-funcționale inițiale;
- arhitectură conceptuală modulară;
- prototip demonstrativ pentru fluxul multi-agent;
- mecanisme timpurii de audit și control al uneltelor;
- direcții de cercetare pentru confidențialitate, execuție distribuită și validare.

## 10. Pași următori

Următoarea etapă logică este extinderea agenților de la schelet demonstrativ la funcționalități reale, definirea scenariilor de evaluare repetabile, dezvoltarea mecanismelor de protecție a datelor și consolidarea cadrului de testare pentru atacuri simulate, phishing, anomalii de rețea și scenarii de injectare prin unelte.

## 11. Referințe selective

Raportul tehnic sursă utilizează repere precum AI Act, Cyber Resilience Act, GDPR, NIST AI RMF, OWASP Top 10 for LLM Applications, ReAct, AutoGen, Toolformer, Chain-of-Thought prompting, RLHF, LoRA, învățare federată, confidențialitate diferențială, k-anonymity, l-diversity, MITRE ATT&CK și ghiduri NIST pentru gestionarea incidentelor.

## 12. Notă de publicare

Acest document este o sinteză publică. Nu include cod intern, date operaționale, credențiale, endpoint-uri, jurnale brute, materiale confidențiale sau detalii de infrastructură care ar putea expune suprafața de atac a proiectului.
