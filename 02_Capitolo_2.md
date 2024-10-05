# Capitolo 2: Le basi della Meccanica ondulatoria

## 2.1 Ipotesi di de Broglie

De Broglie propose un comportamento dualistico onda-corpuscolo anche per la materia. $\\$
Propose che una particella di energia $E$ può essere associata ad un'onda di frequenza $v$:
$$E = hv = \hbar \omega$$

Come per i fotoni, anche le particelle avranno una relazione tra impulso e lunghezza d'onda:
$$p = \frac{h}{\lambda} = \frac{2\pi \hbar}{\lambda}$$

Utlizziamo il vettore d'onda $k = \frac{p}{\hbar}$ per poter rappresentare un'onda piana:
$$e^{\pm i(kx - \omega t)} = e^{\pm \frac{i}{\hbar}(px - Et)}$$

Che ci dà la possibilità di riscrivere l'impulso come:
$$p = \hbar k$$

Per i fotoni, la relazione tra frequenza e lunghezza d'onda è:
$$v = \frac{c}{\lambda}$$

Per le particelle massive, la relazione diventa:
$$v = \frac{E}{\lambda p}$$

Dove le espresioni di $E$ e $p$ dipendono dall'hamiltoniana del sistema.$\\$
L'ipotesi di de Broglie è stata confermata sperimentalmente da Davisson e Germer nel 1927, che hanno osservato la diffrazione di elettroni su un cristallo. $\\$
Questi risultati sono serviti anche per giustificare l'ipotesi di quantizzazione del momento angolare nell'atomo di Bohr. Infatti, l'onda che percorre l'orbita circolare dell'elettrone(di circonferenza $2\pi r$) deve essere un'onda stazionaria, cioè deve essere un multiplo intero di $\lambda$, altrimenti si avrebbe interferenza distruttiva e l'elettrone cadrebbe nell'atomo:
$$2\pi r = n\lambda$$

Tenendo conto che $\lambda = \frac{2\pi \hbar}{p}$, si ottiene:
$$l = n\hbar$$

Quindi esattamente la quantizzazione del momento angolare proposta da Bohr.$\\$

## 2.2 Discussione critica dell'esperienza della doppia fenditura

Da una sorgente si emettono particelle che attraversano una doppia fenditura e vengono rilevate su uno schermo. Questo esperimento è stato fatto con elettroni, neutroni, atomi e molecole. $\\$
I risultati sperimentali sono i seguenti:
1. chiusa una delle due fenditure, si osserva una distribuzione di particelle che attraversano l'altra fenditura, come se la particella si comportasse come un corpuscolo classico
2. aperte entrambe le fenditure, non si osserva una somma delle distribuzioni precedenti, ma una distribuzione di interferenza, come se la particella si comportasse come un'onda
3. questa distribuzione di interferenza si vede anche emettendo una sola particella alla volta
4. la singola particella non lascia sul rilevatore una frangia di interferenza, ma un punto luminoso

Le possibili interpretazioni sono:
- si pensava che nel punto 1 e nell'esperimento di Davisson e Germer, le particelle potessero essere vincolate a seguire un percorso ben definito, ma il risultato sperimentale 2 dimostra che non è così
- potrebbe venire da pensare che il fneomeno ondulatorio sia di natura statistica, quando molte particelle attraversano interagiscono tra loro e si comportano come un'onda, ma il punto 3 dimostra che anche una singola particella si comporta come un'onda
- si potrebbe pensare che la particella sia costituita da onde di materia, ma il punto 4 dimostra che la particella è un punto
- l'unica ipotesi che sembra risolvere tutti i problemi è che la particella sia un'onda di probabilità

In altre parole la particella è un'ente non definito, che si manifesta nello spazio-tempo, quando effettuiamo una misura di posizione, come corpuscolo in un punto dello spazio non determinato con una probabilità legata alla forma dell'onda associata.$\\$
Ogni traiettoria ha un "peso" associato, che è la probabilità di trovare la particella in quel punto. $\\$

Potremmo immaginare di fregare la particella con un rilevatore, per sapere da quale fenditura passa, ma in questo caso la particella si comporta come un corpuscolo e non si osserva più l'interferenza. Dunque la nostra misura ha influenzato il sistema.$\\$

## 2.5 Onda piana e particella libera

Seguendo l'ipotesi di de Broglie, assoceremo alla aprticella un'onda monocromatica piana sinusoidale di argomento $kx - \omega t$. Assumiamo che quindi prenda la forma di una delle 4 funzioni seguenti:
$$\psi(x,t) = A sin(kx - \omega t)$$
$$\psi(x,t) = B cos(kx - \omega t)$$
$$\psi(x,t) = C e^{i(kx - \omega t)}$$
$$\psi(x,t) = D e^{-i(kx - \omega t)}$$

L'equazione deve essere lineare, per il principio di sovrapposizione degli stati, e non deve contenere quantità dinamiche(come l'impulso), altrimenti tale equazione sarebbe soddifatta solo da una particolare soluzione. $\\$
Avendo la relazione:
$$\omega = \frac{\hbar k^2}{2m}$$

Data dalla relazione tra energia e impulso, valide per le particelle massive, possiamo intuire che cerchiamo qualcosa del primo ordine nelle derivate temporali e del secondo ordine nelle derivate spaziali. Proviamo dunque:
$$\frac{\partial \psi}{\partial t} = \gamma \frac{\partial^2 \psi}{\partial x^2}$$

Con $\gamma$ da determinare. Seno e coseno non vanno bene, in quanto non sono stabili per le derivate. Mentre
le esponenziali si per $\gamma = \frac{i\hbar}{2m}$. $\\$
Non contiene quantità dinamiche, è lineare e soddisfa l'equazione di Schrödinger. $\\$

Se sostituiamo la nostra onda piana $\psi(x,t) = C e^{i(kx - \omega t)}$ nell'equazione di Schrödinger, otteniamo:
$$\hbar \omega \psi = \frac{\hbar^2 k^2}{2m} \psi$$

Da cui riotteniamo la relazione tra energia e impulso:
$$E \psi = \frac{p^2}{2m} \psi$$

Se vogliamo generalizzarla ad uno spazio tri-dimensionale, possiamo scrivere:
$$\psi(\vec{x},t) = C e^{i(\vec{k} \cdot \vec{x} - \omega t)}$$

Che ci porta all'equazione di Schrödinger in tre dimensioni:
$$i\hbar \frac{\partial \psi}{\partial t} = -\frac{\hbar^2}{2m} \nabla^2 \psi$$

Due precisazioni ulteriori per ocmletare la trattazione dell'onda piana:
- l'onda si propaga con velocità pari alla velocità di fase $v_f = \frac{\omega}{k} = \frac{p}{2m}$, mentre la velocità associata alla particella è la velocità di gruppo $v_g = \frac{\partial \omega}{\partial k} = \frac{\partial E}{\partial p} = \frac{p}{m}$ da cui $v_f = 2v_g$ (la prima c'entra con come sono fatte le onde piane ma non descrive il moto della particella, la seconda descrive il moto della particella)
- le onde piane non sono localizzate in quanto l'integrale di normalizzazione $\int |\psi|^2 d^3x$ diverge. Per avere una funzione d'onda normalizzata, dobbiamo considerare una sovrapposizione di onde piane, cioè un pacchetto d'onde.

## 2.6 Pacchetto d'onde

Per quanto si cerhci di creare un'onda monocrmatica, ci sarà sempre una minima dispersione, quindi l'onda diventerà una sovrapposizione di onde piane con impulsi vicino ma non coincidenti compresi tra $p - \Delta p$ e $p + \Delta p$. $\\$
Rappresentiamo quindi il pacchetto d'onde come:
$$\psi(x,t) = \int C(k) e^{i(kx - \omega t)} d^3k$$

Ritornando ad una dimensione, possiamo scrivere:
$$\psi(x,t) = \int_{k_0 - \Delta k}^{k_0 + \Delta k} C(k) e^{i(kx - \omega(k)t)} dk$$

Supponendo che le onde con k esterno a $k_0 \pm \Delta k$ si annullino. $\\$
Supponiamo anche che $\Delta k = \xi$ sia piccolo, la funzione diventa:
$$\psi(x,t) = C e^{i(k_0 x - \omega_0 t)} \int_{- \Delta k}^{+ \Delta k} e^{i(x - \omega_1 t) \xi} d\xi$$

Calcolando l'integrale, otteniamo il pacchetto d'onde quasi monocromatico:
$$\psi(x,t) = 2C \frac{sin[(x - \omega_1 t)\Delta k]}{x - \omega_1 t} e^{i(k_0 x - \omega_0 t)}$$

Che è composta dal fattore rapidaente oscillante $e^{i(k_0 x - \omega_0 t)}$ che da solo rappresenterebbe l'onda perfettamente monocromatica di una particella non localizzata, e dal fattore che ne modula la forma, che può essere considerato come l'ampiezza della funzione d'onda. $\\$
Nell'istante $t = 0$, la funzione d'onda è:
$$A(x, 0) = 2C \frac{sin(x \Delta k)}{x} $$

Che ha un massimo in $x = 0$ dove vale $2C\Delta k$ e si annulla nei punti $x_n = \frac{n\pi}{\Delta k}$, con $n \neq 0$, tra i quali oscilla tra massimi e minimi. $\\$
L'intervallo in cui è sensibilmente diversa da zero è $[-\frac{\pi}{\Delta k}, \frac{\pi}{\Delta k}]$, dove ha ampiezza $\frac{2\pi}{\Delta k}$. Che si può vedere come buona approssimazione dell'estensione spaziale del pacchetto d'onde. $\\$
Al variare del tempo, il pacchetto si sposterà con velocità $\omega_1 = \frac{p_0}{m}$, che è la velocità di gruppo, quindi la velocità della particella. $\\$
La funzione d'onda ora è a quadrato sommabile, quindi normalizzabile. $\\$
$$\int_{-\infty}^{+\infty} |\psi(x,t)|^2 dx = 4|C|^2 \Delta k \int_{-\infty}^{+\infty} \frac{sin^2 \eta}{\eta^2} d\eta $$

Da cui calcolando otteniamo la funziona d'onda normalizzata del pacchetto d'onde:
$$\psi_{norm}(x,t) = \frac{1}{\sqrt{\pi \Delta k}} \frac{sin(x - \omega_1 t)\Delta k}{x - \omega_1 t} e^{i(k_0 x - \omega_0 t)}$$

Essa descrive una particella localizzata in un intervallo $\Delta x \approx \frac{2 \pi}{\Delta k}$, con impulso $\Delta p = \hbar \Delta k$. $\\$
Quindi vale la relazione di indeterminazione di Heisenberg:
$$\Delta x \Delta p \approx \hbar$$

## 2.7 Equazione di Schrödinger in un campo di forze

Se prendiamo una particella materiale in un campo di forze $F$, dipendenti unicamente dal potenziale $V$ tale che $F = -\nabla V$, possiamo partire sostituendo dentro la relazione classica tra energia cinetica e potenziale:
$$\frac{p^2}{2m} + V = E$$

Gli operatori differenziali:
$$E \rightarrow i\hbar \frac{\partial}{\partial t}$$
$$p \rightarrow -i\hbar \nabla$$
$$x \rightarrow x$$

Ci permettono di scrivere l'equazione di Schrödinger come:
$$i\hbar \frac{\partial \psi}{\partial t} = -\frac{\hbar^2}{2m} \nabla^2 \psi + V\psi$$

In maniera più generale, supponiamo di avere un sistema di $N$ particelle con coordinate generalizzate $q_i$ e impulsi generalizzati $p_i$, la cui dinamica è descritta classicaente da una lagrangiana $L(q_i, \dot{q}_i)$, possiamo scrivere l'halmiltoniana come:
$$H(p,q) = p\dot{q} - L(q, \dot{q})$$

Dove $p$ è il momento coniugato alla coordinata $q$, cioè $p_i = \frac{\partial L}{\partial \dot{q}_i}$. $\\$

L'equazione di Schrödinger per un sistema di $N$ particelle è:
$$i\hbar \frac{\partial \psi}{\partial t} = H\psi$$

## 2.8 Equazione di continuità

Se moltiplichiamo $\psi^*$ per l'equazione di Schrödinger e $\psi$ per la sua coniugata, otteniamo:
$$i\hbar \frac{\partial}{\partial t}(\psi^*\psi) = -\frac{\hbar^2}{2m} \nabla \cdot (\psi^*\nabla \psi - \nabla \psi^*\psi)$$

Ricordando che la densità di probabilità è $\Rho = \psi^*\psi$ e ponendo $J = \frac{\hbar}{2mi}(\psi^*\nabla \psi - \nabla \psi^*\psi)$, otteniamo l'equazione di continuità:
$$\frac{\partial \Rho}{\partial t} + \nabla \cdot J = 0$$

Nella forma solita di equazione di continuità, dove alla densità di probabilità $\Rho$ è associata una corrente di probabilità $J$.$\\$
Come tutte le leggi di continuittà, anche questa è una legge di conservazione, in questo caso la conservazione della probabilità totale 1.$\\$