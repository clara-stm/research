# Arhitectura rolurilor AI în CLARA

Notă publică de arhitectură pentru publicul general.

## Statut public

Acest document explică, la nivel general, cele patru roluri AI principale utilizate în arhitectura CLARA. Textul descrie responsabilități și moduri de colaborare, nu detalii confidențiale de implementare, prompturi interne, seturi de date private, identificatori de infrastructură sau proceduri operaționale.

Un rol AI nu este, în mod obligatoriu, un model AI separat. Rolul descrie o responsabilitate în sistem. În funcție de etapa de implementare, un rol poate fi susținut de un model, de mai multe modele sau de o combinație de modele, unelte, reguli și verificare umană.

## Explicație simplă

CLARA poate fi privit ca o echipă de asistenți pentru securitate cibernetică:

- **CLARA Core** este coordonatorul.
- **Agentul de Audit** verifică nivelul de protecție și configurațiile.
- **Agentul de Rețea** analizează comunicarea dintre sisteme și dovezile de rețea.
- **Agentul de Risc Browser / URL** verifică riscurile asociate paginilor web, linkurilor și navigării.

Scopul nu este înlocuirea specialiștilor în securitate cibernetică, ci sprijinirea lor: citirea mai rapidă a dovezilor, formularea unor întrebări mai bune, compararea semnalelor, documentarea raționamentului și păstrarea unei urme clare de audit.

## Rolul 1: CLARA Core

CLARA Core este rolul central de coordonare. Primește întrebarea sau sarcina utilizatorului, interpretează intenția, decide ce tip de analiză este necesar și direcționează activitatea către rolul specializat potrivit.

Pentru utilizatorul general, CLARA Core este componenta care oferă coerență experienței. O întrebare largă, de exemplu "este această activitate suspectă?", este transformată în pași mai mici, care pot fi verificați de rolurile specializate.

Responsabilități principale:

- înțelege cererea utilizatorului exprimată în limbaj natural;
- identifică dacă sarcina ține de audit, dovezi de rețea, risc în browser sau o situație combinată;
- selectează rolul sau rolurile specializate potrivite;
- combină rezultatele într-o explicație clară;
- păstrează trasabilitatea prin înregistrarea cererii, verificărilor și modului în care este generat răspunsul;
- evită concluziile nesusținute atunci când dovezile sunt incomplete.

CLARA Core este important deoarece întrebările de securitate cibernetică combină frecvent mai multe domenii. Un link suspect poate avea legătură cu trafic de rețea neobișnuit. O configurație slabă poate face o tentativă de phishing mai periculoasă. Rolul de coordonare păstrează legătura dintre aceste semnale.

## Rolul 2: Agentul de Audit

Agentul de Audit se concentrează pe nivelul de protecție al sistemelor. Ajută la verificarea configurațiilor, politicilor și controalelor tehnice în raport cu practici de securitate așteptate.

Pentru publicul general, acest rol seamănă cu un inspector. Nu spune doar că ceva este "bun" sau "rău"; explică ce a fost verificat, de ce contează și ce ar trebui îmbunătățit.

Responsabilități tipice:

- examinează dovezi de configurare și descrieri ale controalelor de securitate;
- identifică setări lipsă, slabe sau inconsecvente;
- organizează observațiile după severitate și impact;
- leagă constatările de principii și cadre publice de referință, acolo unde este potrivit;
- sugerează pași de remediere într-un limbaj ușor de înțeles;
- produce explicații utile pentru audit, care pot fi revizuite de un operator uman.

Agentul de Audit sprijină responsabilitatea și transparența. O recomandare de securitate trebuie să poată fi explicată, repetată și legată de dovezile disponibile la momentul analizei.

## Rolul 3: Agentul de Rețea

Agentul de Rețea se concentrează pe dovezi de comunicare: jurnale, evenimente, fluxuri, alerte și alți indicatori care descriu cum comunică sistemele.

Pentru publicul general, acest rol seamănă cu un analist de trafic. Caută tipare de comunicare normale, neobișnuite sau suspecte și explică de ce merită atenție.

Responsabilități tipice:

- citește și rezumă dovezi legate de rețea;
- detectează tipare neobișnuite de timp, volum, destinație, protocol sau comportament;
- corelează evenimente care pot fi slabe individual, dar mai relevante împreună;
- separă dovezile clare de ipoteze;
- ajută la prioritizarea verificărilor următoare pentru analistul uman;
- sprijină trierea incidentelor prin explicații concise.

Agentul de Rețea este util deoarece multe incidente de securitate lasă urme în comportamentul de comunicare înainte de a fi pe deplin înțelese. Rolul său este să transforme semnalele brute într-un traseu de investigație structurat.

## Rolul 4: Agentul de Risc Browser / URL

Agentul de Risc Browser / URL se concentrează pe riscurile asociate navigării web și linkurilor. Ajută la evaluarea siguranței unei pagini, a unui URL, a unei descărcări sau a unei interacțiuni în browser.

Pentru publicul general, acest rol seamănă cu un asistent prudent pentru navigare web. Analizează indicii vizibile și tehnice înainte de a recomanda încredere, precauție sau escaladare.

Responsabilități tipice:

- examinează structura URL-ului și indiciile legate de domeniu;
- identifică tipare asemănătoare phishingului și prezentări înșelătoare;
- ia în calcul riscuri de descărcare, redirecționare și comportament al paginii;
- explică semnele de avertizare într-un limbaj accesibil;
- sprijină fluxuri sigure de navigare și investigație;
- evită tratarea unui singur semnal slab ca dovadă definitivă.

Acest rol este important deoarece multe atacuri încep cu un link, o pagină, un fișier sau o acțiune în browser. De aceea, CLARA tratează riscul de navigare web ca zonă distinctă de analiză.

## Cum lucrează rolurile împreună

Un flux CLARA tipic poate fi rezumat astfel:

1. Utilizatorul pune o întrebare sau transmite o dovadă.
2. CLARA Core interpretează cererea și decide ce rol specializat este relevant.
3. Rolul selectat analizează tipul potrivit de dovezi.
4. Dacă situația acoperă mai multe domenii, CLARA Core coordonează mai multe roluri.
5. Rezultatele sunt combinate într-un răspuns care separă faptele, interpretarea, incertitudinea și pașii recomandați.
6. Interacțiunea este înregistrată pentru auditabilitate și evaluare ulterioară.

Această arhitectură bazată pe roluri păstrează sistemul modular. Fiecare rol poate fi îmbunătățit independent, dar contribuie la un singur asistent coerent de securitate cibernetică.

## Principii de siguranță și guvernanță

Arhitectura publică CLARA pune accent pe utilizarea controlată și auditabilă a inteligenței artificiale:

- **Unelte controlate:** rolurile specializate trebuie să folosească doar unelte aprobate și parametri permiși.
- **Trasabilitate:** deciziile importante, apelurile de unelte și constatările generate trebuie înregistrate.
- **Supraveghere umană:** CLARA sprijină operatorii umani; nu elimină responsabilitatea acestora.
- **Minimizarea datelor:** informațiile sensibile trebuie folosite doar când sunt necesare și nu trebuie expuse în materiale publice.
- **Incertitudine clară:** sistemul trebuie să spună când dovezile sunt incomplete sau când o concluzie este doar o ipoteză.
- **Delimitare public/privat:** documentația publică explică concepte și progres de cercetare, nu detalii operaționale confidențiale.

## De ce patru roluri

Designul cu patru roluri reflectă o împărțire practică în securitate cibernetică:

- este nevoie de un coordonator care înțelege cererea utilizatorului și organizează activitatea;
- analiza de audit are nevoie de raționament structurat despre controale și conformitate;
- analiza de rețea are nevoie de corelare de evenimente și interpretare de anomalii;
- riscul asociat browserului și URL-urilor are nevoie de raționament specific navigării web.

Împreună, aceste roluri acoperă direcțiile principale ale primei arhitecturi CLARA fără a forța toate sarcinile printr-o singură componentă generală.

## Evoluție

Pe măsură ce CLARA se dezvoltă, rolurile pot fi rafinate, împărțite, combinate sau susținute de combinații diferite de modele și unelte. Denumirile publice ale rolurilor descriu responsabilități care trebuie să rămână ușor de înțeles pentru utilizatori, evaluatori și părți interesate, chiar dacă implementarea tehnică evoluează.
