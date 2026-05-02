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

Primul raport tehnic CLARA documentează trecerea de la ideea de produs la o fundație tehnică verificabilă. Activitatea a urmărit definirea cerințelor, înțelegerea stadiului tehnologic pentru AI aplicat în securitate cibernetică și proiectarea unei arhitecturi multi-agent care să poată fi extinsă incremental.

CLARA este conceput ca un sistem de securitate cibernetică asistat de AI, în care un nucleu de orchestrare, numit CLARA Core, interpretează solicitări în limbaj natural, selectează agenți specializați, controlează apelurile către unelte și produce răspunsuri explicabile. Direcția de cercetare combină modele de limbaj, agenți specializați, auditabilitate, confidențialitate, mecanisme de feedback expert și posibilitatea rulării locale pentru scenarii sensibile.

## 2. Obiectivul Perioadei

Obiectivul principal a fost reducerea riscului de proiectare printr-o tranziție controlată de la analiză la prototip. Echipa a urmărit:

- definirea cerințelor funcționale și non-funcționale;
- stabilirea criteriilor de acceptanță pentru demonstrații tehnice;
- documentarea literaturii relevante despre LLM/SLM, multi-agent systems și cybersecurity;
- proiectarea arhitecturii conceptuale CLARA;
- validarea timpurie printr-un schelet funcțional de orchestrare.

## 3. Direcții De Cercetare Analizate

### 3.1 Modele De Limbaj Pentru Cybersecurity

Raportul analizează modul în care modelele de limbaj pot sprijini activități precum interpretarea evenimentelor, explicarea alertelor, sumarizarea investigațiilor, generarea de recomandări și producerea de rapoarte tehnice. În CLARA, modelul de limbaj nu este tratat ca un înlocuitor al operatorului uman, ci ca o componentă de augmentare care ajută la structurarea informației și la formularea unor explicații utile.

### 3.2 Agenți Specializați

Arhitectura separă nucleul de orchestrare de agenții specializați. Agenții pot acoperi sarcini precum audit local, analiză de rețea, protecție browser sau verificări de configurare. Această separare permite evoluția independentă a componentelor și limitează impactul erorilor.

### 3.3 Confidențialitate Și Rulare Locală

Raportul pune accent pe rularea locală sau controlată a agenților, minimizarea datelor trimise către componente centrale și mascarea informațiilor sensibile în loguri. Au fost analizate concepte precum învățarea federată, differential privacy, criptarea și anonimizarea, ca posibile mecanisme pentru etapele ulterioare.

### 3.4 Tool-Calling Controlat

Pentru a limita riscurile de abuz, CLARA introduce de la început ideea unui Tool Registry cu allowlist, validare de parametri, timeouts, logging și politici de execuție. Această decizie este importantă pentru sistemele agentice, unde un model poate solicita acțiuni externe prin unelte.

### 3.5 Auditabilitate Și Explicabilitate

Auditul nu este adăugat ulterior, ci este introdus ca cerință de bază. Evenimentele de tip routing decision, tool call, agent result și final response permit reconstruirea traseului decizional și susțin explicații verificabile.

## 4. Arhitectura Conceptuală

Prima arhitectură CLARA include următoarele componente:

| Componentă | Rol în raportul 1 |
| --- | --- |
| CLARA Core | Interpretează solicitări, planifică, rutează sarcini și agregă rezultatele. |
| Agenți specializați | Execută sarcini cyber delimitate și returnează rezultate structurate. |
| Tool Registry | Controlează apelurile către unelte și reduce suprafața de atac. |
| Mesagerie internă | Standardizează cererile, răspunsurile și evenimentele de audit. |
| Audit/Trace | Înregistrează deciziile, apelurile de tool și răspunsurile finale. |
| Platformă educațională | Componentă planificată pentru instruire și transfer de cunoștințe. |

Fluxul validat la nivel conceptual este:

1. Utilizatorul transmite o solicitare în limbaj natural.
2. CLARA Core interpretează solicitarea și generează un plan minimal.
3. Orchestratorul selectează agenții potriviți.
4. Agenții execută sarcini prin interfețe standardizate.
5. Rezultatele sunt agregate într-un răspuns explicativ.
6. Auditul înregistrează traseul execuției.

## 5. Cerințe Inițiale

Raportul definește cerințe funcționale precum interpretarea comenzilor în limbaj natural, rutarea către agenți, agregarea rezultatelor, explicația alertelor și generarea de rapoarte. Cerințele non-funcționale includ confidențialitate, auditabilitate, performanță, extensibilitate și securitate prin design.

Exemple de criterii de acceptanță definite în această etapă:

- CLARA poate produce un plan coerent pentru scenarii predefinite.
- Solicitările sunt rutate către agentul potrivit.
- Răspunsurile includ sumar, evidențe, recomandări și pași următori.
- Datele sensibile sunt mascate în loguri.
- Fiecare scenariu demonstrativ are un jurnal de audit.
- Un agent nou poate fi adăugat prin interfața standard și înregistrare în registry.

## 6. Prototipare Inițială

Prototipul inițial a fost construit pentru a valida fluxul end-to-end, nu pentru a livra o implementare completă. Elementele demonstrate includ:

- schelet de orchestrare pentru CLARA Core;
- agent runner minimal;
- format standard pentru AgentRequest, AgentResponse și CoreEvent;
- Tool Registry inițial cu allowlist;
- log local pentru audit și trace;
- stub pentru Agentul de Audit;
- scenarii minime de integrare și documentație de rulare.

Această abordare a redus riscul de supra-complexitate și a permis testarea timpurie a deciziilor arhitecturale.

## 7. Cooperare Și Execuție Distribuită

Raportul include o direcție de cercetare privind execuția distribuită și auditul imuabil. Au fost analizate concepte de orchestrare edge, execuție containerizată și validare adversarială controlată. Scopul acestei direcții este evaluarea fezabilității pentru scenarii în care agenții CLARA rulează pe infrastructuri distribuite, cu evidențe verificabile ale execuției.

## 8. Riscuri Identificate

| Risc | Măsură de reducere |
| --- | --- |
| Cerințe ambigue și extindere necontrolată a scopului | Backlog structurat, criterii de acceptanță și delimitare PoC. |
| Explicabilitate greu de adăugat ulterior | Audit/trace introdus ca cerință de bază. |
| Expunerea datelor sensibile | Privacy by design, mascarea logurilor și opțiuni de rulare locală. |
| Tool-calling nesigur | Tool Registry, allowlist, validare de parametri și logging. |
| Agregare incoerentă multi-agent | Scheme standard pentru rezultate, severitate și evidențe. |

## 9. Rezultate

Primul raport stabilește fundația CLARA:

- cerințe funcționale și non-funcționale inițiale;
- arhitectură conceptuală modulară;
- prototip demonstrativ pentru fluxul multi-agent;
- mecanisme timpurii de audit și control al tool-urilor;
- direcții de cercetare pentru confidențialitate, execuție distribuită și validare.

## 10. Pași Următori

Următoarea etapă logică este extinderea agenților de la stub la funcționalitate reală, definirea scenariilor de evaluare repetabile, dezvoltarea mecanismelor de protecție a datelor și consolidarea cadrului de testare pentru atacuri simulate, phishing, anomalii de rețea și scenarii de tool-injection.

## 11. Referințe Selective

Raportul tehnic sursă utilizează repere precum AI Act, Cyber Resilience Act, GDPR, NIST AI RMF, OWASP Top 10 for LLM Applications, ReAct, AutoGen, Toolformer, Chain-of-Thought prompting, RLHF, LoRA, federated learning, differential privacy, k-anonymity, l-diversity, MITRE ATT&CK și ghiduri NIST pentru incident handling.

## 12. Notă De Publicare

Acest document este o sinteză publică. Nu include cod intern, date operaționale, credențiale, endpoint-uri, loguri brute, materiale confidențiale sau detalii de infrastructură care ar putea expune suprafața de atac a proiectului.
