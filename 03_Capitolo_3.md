# Capitolo 3: Formalismo della Meccanica Quantistica

## 3.2 Postulati della Meccanica Quantistica

Definizione: un raggio in uno spazio di Hilbert è un insieme di vettori di stato proporzionali tra loro.
$$\ket{\psi} \simeq \alpha \ket{\psi}$$

**Postulato 1: Descrizione degli stati di un sistema fisico**$\\$
A ciascun sistema fisico è associato uno spazio di Hilbert $\mathcal{H}$ complesso e separabile. Gli stati del sistema sono rappresentati da, a un tempo fissato, i raggi in $\mathcal{H}$.

Nel caso in cui uno vettore non sia normalizzato:
$$\ket{\psi} = \frac{\ket{\psi}}{|| \psi ||}$$

La sovrapposizione di stati è un concetto fondamentale della meccanica quantistica. Se $\ket{\psi_1}$ e $\ket{\psi_2}$ sono due stati di un sistema, allora anche $\alpha \ket{\psi_1} + \beta \ket{\psi_2}$ è uno stato del sistema.

La fase globale di uno stato non è osservabile, quindi due stati che differiscono per una fase globale sono equivalenti. Invce la fase relativa tra due stati è osservabile.

**Postulato 2: Descrizione delle osservabili fisiche**$\\$
Ogni grandezza osservabile $F(p, q, t)$ è associata a un operatore lineare hermitiano $F$ definito su $\mathcal{H}$.

L'insieme degli autovalori di $F$ è lo spettro di $F$. Soddisfa l'equazione agli autovalori:
$$F \ket{k} = f_k \ket{k}$$

Dove tutti gli autovettori $\ket{k}$ sono ortogonali e ammette una decomposizione spettrale:
$$F = \sum_k f_k \ket{k} \bra{k}$$

Dove $E_k = \ket{k} \bra{k}$ è il proiettore sullo stato $\ket{k} relative all'autovalore $f_k$.
Soddisfano el relazioni:
$$E_k E_j = \delta_{kj} E_k$$

**Postulato 3: Misura di osservali fisiche**$\\$
La misura di una grandezza osservabile $F$ su uno stato $\ket{\psi}$ proietta lo stato su uno degli autostati di $F$(autovettori) e il risultato della misura è il valore corrispondente dell'autovalore. L'autovalore $f_k$ è il risultato della misura con probabilità:
$$P_k = || E_k \ket{\psi} ||^2 = \bra{\psi} E_k \ket{\psi}$$

ovvero:
- $P_k = | \bra{k} \ket{\psi} |^2$ nel caso di autovalori discreti non degeneri
- $P_k = \sum_{i=1}^{g_k} | \bra{k_i} \ket{\psi} |^2$ (dove $g_k$ è la degenerazione dell'autovalore $f_k$) nel caso di autovalori discreti degeneri
- nel caso di autovalori continui si parlerà di densità di probabilità $\rho(k) = | \bra{k} \ket{\psi} |^2$

Da qui si comprende perchè si scelgono operatori hermitiani per le osservabili fisiche, in quanto hanno autovalori reali.$\\$
Se lo spettro di $F$ è discreto, si osserverà un fenomeno di quantizzazione.$\\$
I numeri $\ket{\psi} \bra{\psi}$ sono detti ampiezze di probabilità.$\\$
Dopo una misura di $F$, il sistema collassa in uno stato $\ket{k}$. In caso di degenerazione, il sistema si trova nella proiezione dello stato originale nell'autospazio di $F$.

**Postulato 4: Dinamica ed evoluzione temporale degli stati**$\\$
L'evoluzione temporale di uno stato $\ket{\psi(t)}$ è descritta dall'equazione di Schrödinger:
$$i \hbar \frac{d}{dt} \ket{\psi(t)} = H \ket{\psi(t)}$$

Dove $H$ è l'operatore hamiltoniano $H = H(p, q)$ associato al sistema. In generale $q_i$ e $p_i$ non commutano.$\\$
La loro combinazione simmetrica è l'operatore di Poisson:
$$\frac{1}{2} \{ q_i, p_j \} = \frac{qp + pq}{2}$$

Quindi per convenzione utilizziamo $qp$ e $pq$ ugualmente.$\\$

**Postulato 5: Sistemi composti**$\\$
Lo spazio di Hilbert di un sistema composto è il prodotto tensore degli spazi di Hilbert dei sottosistemi. Se $\mathcal{H}_1$ e $\mathcal{H}_2$ sono gli spazi di Hilbert dei sottosistemi, lo spazio di Hilbert del sistema composto è $\mathcal{H} = \mathcal{H}_1 \otimes \mathcal{H}_2$.$\\$
Se il sistema $A$ è descritto da $\ket{\psi_A}$ e il sistema $B$ da $\ket{\phi_B}$, lo stato del sistema composto è $\ket{\psi_A , \phi_B} = \ket{\psi_A} \otimes \ket{\phi_B}$.$\\$

**Osservazioni:**$\\$
- l'equazione della dinamica è lineare e deterministica
- ci sono due modi differenti di cambiare lo stato di un sistema: misura(proiezione) e evoluzione temporale(deteministica)

## 3.9 Valori medi e scarti quadratici medi

Definiamo il valore medio di un'osservabile $F$ su uno stato $\ket{\psi}$ come:
$$\langle F \rangle = \frac{\bra{\psi} F \ket{\psi}}{\bra{\psi} \ket{\psi}}$$

Oltre al valore medio, per calcolare l'incertezza di una misura, si calcola lo scarto quadratico medio:
$$\Delta F = \sqrt{\langle F^2 \rangle - \langle F \rangle^2}$$

Partendo dall'annullabilità dello scarto quadratico medio:
$$\Delta F = \sqrt{\langle F^2 \rangle - \langle F \rangle^2} = \frac{|| (F - f) \ket{\psi} ||^2}{|| \ket{\psi} ||^2} = 0$$

Che implica che lo stato $(F - f) \ket{\psi}$ ha norma nulla, possiamo dedurre che:
$$F \ket{\psi} = f \ket{\psi}$$

Abbiamo dimostrato che se lo scarto quadratico medio è nullo, allora lo stato è un autostato dell'osservabile.

*Teorema:*$\\$
Una misura di $F$ su uno stato $\ket{\psi}$ restituisce un risultato determinato se e solo se $\ket{\psi}$ è un autostato di $F$.

## 3.10 Teorema di Ehrenfest

L'evoluzione temporale di qualunque osservabile $F$ è data dall'equazione di Schrödinger, questo è vero anche per i valori medi:
$$\frac{d}{dt} \langle F \rangle_{\psi} = - \frac{1}{i \hbar} \bra{\psi} H F \ket{\psi} + \langle \frac{\partial F}{\partial t} \rangle + \frac{1}{i \hbar} \bra{\psi} F H \ket{\psi}$$

Dunque:
$$\dot{\langle F \rangle} = - \frac{i}{\hbar} \langle [F, H] \rangle + \langle \frac{\partial F}{\partial t} \rangle$$

Tutte le quantità osservabili sono in funzione delle coordinate e degli impulsi $F = F(p, q, t)$, ricordiamo che una funzione di un operatore può essere definita tramite la sua serie di Taylor:
$$f(q) = \sum_{n=0}^{\infty} f_n q^n$$

Con la sua derivata:
$$\frac{df}{dq} = \sum_{n=0}^{\infty} n f_n q^{n-1}$$

Dove $[q, f(q)] = 0$ e $[p, f(q)] = i \hbar \frac{d}{dq} f(q)$.

Da cui possiamo dimostrare che:
$$[q, p^n] = i \hbar n p^{n-1}$$

Che ci porta a:
$$[q, F(p, q)] = i \hbar \frac{\partial}{\partial p} F(p, q)$$
$$[p, F(p, q)] = -i \hbar \frac{\partial}{\partial q} F(p, q)$$

L'hamiltoniana è funzione delle coordinate e degli impulsi, quindi:
$$\dot{\langle q \rangle} = \langle \frac{\partial H}{\partial p} \rangle$$
$$\dot{\langle p \rangle} = - \langle \frac{\partial H}{\partial q} \rangle$$

Utilizzando poi le relazioni di commutazione tra $q$ e $p$:
$$F(q, p, t) = \sum_{n,m}^{\infty} F_{nm}(t) q^n p^m$$

**Teorema di Ehrenfest:**$\\$
I valori medi degli osservabili fisiche evolvono nel tempo come le corrispondenti quantità classiche.
$$\dot{\langle F \rangle} = \langle \{ F, H \}_{p} \rangle + \frac{\partial \langle F \rangle}{\partial t}$$

Essa riporta anche alla relazione $\{.,.\}_{p} \rightarrow - \frac{i}{\hbar} [.,.]$.

## 3.11 Principio di Heisenberg generalizzato

Consideriamo due osservabili $F$ e $G$ e definiamo i vettori:
$$\ket{f} = (F - \langle F \rangle) \ket{\psi}$$
$$\ket{g} = (G - \langle G \rangle) \ket{\psi}$$

Gli scarti quadratici medi sono:
$$(\Delta F)^2 = \bra{f} \ket{f}$$
$$(\Delta G)^2 = \bra{g} \ket{g}$$

La disuguaglianza di Schwarz ci dice che:
$$(\Delta F)^2 (\Delta G)^2 \geq | \bra{f} \ket{g} |^2$$

Se prendiamo la relazione che vale per un numero complesso:
$$|z|^2 = \frac{(z - z^*)^2}{2i}^2$$

Se prendiamo $z = \bra{f} \ket{g}$, otteniamo:
$$(\Delta F)^2 (\Delta G)^2 \geq \frac{( \bra{f} \ket{g} - \bra{g} \ket{f} )^2}{2i}^2$$

Sappiamo che $\bra{f} \ket{g} = \langle FG \rangle - \langle F \rangle \langle G \rangle$, quindi:
$$(\Delta F)^2 (\Delta G)^2 \geq \frac{\langle [F, G] \rangle^2}{2i}^2$$

Da cui la relazione di Heisenberg generalizzata:
$$\Delta F \Delta G \geq | \frac{\langle [F, G] \rangle}{2i} |$$

Poichè due operatori hermitiani sono diagonalizzabili simultaneamente se e solo se commutano, possiamo dire che due grandezze commutanti sono misurabili simultaneamente.

Prendendo l'operatore di posizione($x$) e l'operatore di impulso($p$), possiamo dimostrare che:
$$\Delta x_i \Delta p_i \geq \frac{\hbar}{2} \delta_{ij}$$

Più in generale per un sisema descritto da coordinate generalizzate $q_i$ e momenti coniugati $p_i$:
$$\Delta q_i \Delta p_i \geq \frac{\hbar}{2} \delta_{ij}$$

Questo è il principio di indeterminazione di Heisenberg.$\\$
L'osservazione chiave è che esso mette in crisi la definizione classica di traiettoria, basata sulla conoscenza precisa delle posizioni e degli impulsi.$\\$

## 3.13 Equazione di Schrödinger stazionaria

Se l'hamiltoniana è indipendente dal tempo, possiamo fattorizzare la funzione d'onda in una parte spaziale e una temporale:
$$\psi(q, t) = \psi(q) \phi(t)$$

Sostituendo nella equazione di Schrödinger:
$$\frac{i \hbar}{\phi(t)} \frac{d \phi(t)}{dt} = \frac{H \psi(q)}{\psi(q)}$$

Possiamo porli uguali a una costante $E$, in quanto sono indipendenti.$\\$
La parte temporale è quindi:
$$i \hbar \frac{d \phi(t)}{dt} = E \phi(t)$$

Da cui:
$$\phi(t) = A e^{-\frac{i}{\hbar} Et}$$

La parte spaziale è:
$$H \psi(q) = E \psi(q)$$

Che è l'equazione agli autovalori dell'hamiltoniana, anche chiamata equazione di Schrödinger stazionaria. Essendo un'equazione agli autovalori, possiamo quindi esplicitare i singoli valori $E_n$:
$$H \psi_{n,(k)}(q) = E_n \psi_{n,(k)}(q)$$

Dove $n$ è l'indice dell'autovalore e $k$ è l'indice della degenerazione.$\\$
L'ambiguità nella scelta degli $\psi_{n,(k)}$ può essere rimossa se si identificano altri operatori che commutano con l'hamiltoniana che costruiscono un $ICOC = \{ H, G_1, G_2, ... \}$(insieme completo di operatori che commutano).$\\$

La funzione completa di energia $E_n$, corrispondendo al livello n-esimo si scrive quindi:
$$\psi_n(q, t) = e^{-\frac{i}{\hbar} E_n t} \sum_k A_{n,(k)} \psi_{n,(k)}(q) = e^{-\frac{i}{\hbar} E_n t} \psi_n(q)$$

Dove $A_{n,(k)}$ sono le costanti di normalizzazione.$\\$
L'unica dipendenza temporale è quindi nella fase, che è una fase globale e non è osservabile.$\\$
Infatti la corrispondente densità di probabilità è:
$$| \psi_n(q, t) |^2 = \sum_k | A_{n,(k)} \psi_{n,(k)}(q) |^2$$

Che è indipendente dal tempo, quindi gli stati vengono detti stazionari.

Un generico stato $\ket{\psi(t)}$ è la sovrapposizione di stati stazionari:
$$\psi(q, t) = \sum_n B_n e^{-\frac{i}{\hbar} E_n t} \psi_n(q)$$

## 3.15 Relazione di indeterminazione energia-tempo

La vita media di uno stato è intrensicamente legata alla sua energia: $\tau \Delta E = \hbar$.$\\$

Possiamo riscriverla come:
$$\Delta E \Delta t \sim \hbar$$

Se consideriamo uno stato $\ket{\psi}$, il valore medio dell'energia è su questo stato è:
$$E_0 = \bra{\psi} H \ket{\psi}$$

Indipendentemente dal tempo ove il sistema è isolato. L'energia di questo stato è definita a meno di un'indeterminazione $\Delta E = \sqrt{\langle H^2 \rangle - \langle H \rangle^2}$.$\\$
Se consideriamo $F$ un osservabile non dipendente dal tempo, per il teorema di Ehrenfest:
$$\frac{d}{dt} \langle F \rangle = \frac{i}{\hbar} \langle [F, H] \rangle$$

Considerando anche l'incertezza di $F$:
$$\Delta F \Delta H \geq \frac{1}{2} | \langle [F, H] \rangle |$$

Che combinata a quella precedente ci porta a:
$$\Delta F \Delta H \geq \frac{\hbar}{2} | \frac{d}{dt} \langle F \rangle |$$

Se indichiamo $\Delta t = \frac{\Delta F}{| \frac{d}{dt} \langle F \rangle |}$ l'intervallo di tempo in cui il valore medio di $F$ varia di una quantità $\Delta F$, possiamo scrivere:
$$\Delta E \Delta t \geq \frac{\hbar}{2}$$

Il tempo $\Delta t$ che in media può sopravvivere un sistema che abbia energia $\Delta E$. Quindi in MQ può essere violata la conservazione dell'energia per intervalli di tempo brevi.$\\$


