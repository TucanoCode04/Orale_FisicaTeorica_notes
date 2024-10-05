# Capitolo 5: Momento angoalare

## 5.3 Operatore momento angolare

L'operatore moemnto angolare è deifnito come:
$$L = x \times p = -i\hbar x \times \nabla$$

Vogliamo veder eil comportamento in coordinate polari di $(x \times \nabla)$:
$$(x \times \nabla)_i = \sum_{j,k} \epsilon_{ijk} x_j \frac{\partial}{\partial x_k}$$

L'operatore $(x \times \nabla)^2$ si ottiene sommando su $i$:
$$(x \times \nabla)^2 = \frac{\partial^2}{\partial \theta^2} + cot \theta \frac{\partial}{\partial \phi} + \frac{1}{sin^2 \theta} \frac{\partial^2}{\partial \phi^2}$$

Da qui possiamo identificare l'operatore $L^2$:
$$L^2 = -\hbar^2 (x \times \nabla)^2 = -\hbar^2 \left( \frac{\partial^2}{\partial \theta^2} + cot \theta \frac{\partial}{\partial \phi} + \frac{1}{sin^2 \theta} \frac{\partial^2}{\partial \phi^2} \right)$$

Esiste anche la relaizone importante:
$$p^2 = p_r^2 + \frac{L^2}{r^2}$$

### 5.3.1 Operatore $L_3$: spettro e autofunzioni
Vediamo la qunatizzazione dell'operatore $L_3$, ma vale per tutti gli operatori $L_i$:
$$L_3 = -i\hbar \frac{\partial}{\partial \phi}$$

Passiamo all'equazione agli autovalori:
$$-i\hbar \frac{\partial \psi}{\partial \phi} = l_3 \psi$$

La cui soluzione immediata è:
$$\psi = A e^{\frac{i}{\hbar} l_3 \phi}$$

Dove $\phi$ è un angolo che va da $0$ a $2\pi$. Quindi le autofunzioni devono essere periodiche $\psi(\phi + 2\pi) = \psi(\phi)$, tale condizione impone che gli autovalori $l_3$ siano quantizzati:
$$l_3 = m\hbar$$

Con $m = 0, \pm 1, \pm 2, \pm 3, \ldots$. La normalizzazione delle autofunzioni è:
$$\psi_m(\phi) = \frac{e^{im\phi}}{\sqrt{2\pi}}$$

### 5.3.2 Operatore $L^2$
L'operatore $L^2$ in coordinate polari è:
$$L^2 = -\hbar^2 \left( \frac{\partial^2}{\partial \theta^2} + cot \theta \frac{\partial}{\partial \phi} + \frac{1}{sin^2 \theta} \frac{\partial^2}{\partial \phi^2} \right)$$

La sua funzione agli autovalori è:
$$L^2 \psi(\theta, \phi) = \delta \psi(\theta, \phi)$$

Le soluzioni devono essere periodiche $\psi(\theta, \phi + 2\pi) = \psi(\theta, \phi)$ e limitate $|\psi(\theta, \phi)| < M$. $\\$
Abbiamo che $0 \leq \theta \leq \pi$ e $0 \leq \phi \leq 2\pi$. $\\$
Cerchiamo quindi soluzioni fattorizzate dle tipo:
$$\psi(\theta, \phi) = u(\theta) f(\phi)$$

Che rispecchino le condizioni sopra. Sostituendo nell'equazione agli autovalori otteniamo:
$$sin^2 \theta \frac{1}{u} \frac{d^2u}{d\theta^2} + cos \theta sin \theta \frac{1}{u} \frac{du}{d\theta} + \frac{\delta}{\hbar^2} sin^2 \theta = -\frac{1}{f} \frac{d^2f}{d\phi^2} = m^2$$

Dove $m^2$ è il termine di separazione delle variabili. Il membro di destra diventa:
$$\frac{d^2f}{d\phi^2} + m^2 f = 0$$

Che si integra facilmente:
$$f(\phi) = A e^{im\phi} + B e^{-im\phi}$$

Che può essere soddisfatta solo per $m = 0, \pm 1, \pm 2, \ldots$. La soluzione generale è:
$$f(\phi) = \frac{e^{im\phi}}{\sqrt{2\pi}}$$

Quindi per la parte in $\phi$ abbiamo le stesse autofunzioni di $L_3$, come ci aspettavamo. Per la parte in $\theta$ otteniamo:
$$\frac{d^2u}{d\theta^2} + cot \theta \frac{du}{d\theta} + \left( \frac{\delta}{\hbar^2} - \frac{m^2}{sin^2 \theta} \right) u = 0$$

Ponendo $\delta = l(l+1)$ e $x = cos \theta$ otteniamo l'equazione di Legendre:
$$(1-x^2) \frac{d^2u}{dx^2} - 2x \frac{du}{dx} + \left( l(l+1) - \frac{m^2}{1-x^2} \right) u = 0$$

Che riscrivendola nella forma standard:
$$u'' + p(x)u' + q(x)u = 0$$

Vedi che $p(x)$ e $q(x)$ presentano poli del primo e secondo ordine in $x = \pm 1$. L'equazioni indiciale è:
$$\rho^2 - \frac{m^2}{4} = 0$$

Che ha le soluzioni:
$$\rho_{1,2} = \pm \frac{m}{2}$$

Le due soluzioni linearmente indipendenti sono:
$$u_1 = (1-x)^{\frac{m}{2}} \sum_{n=0}^{\infty} c_n (x-1)^n$$
$$u_2 = au_1(x) log(x-1) + (1-x)^{\frac{-m}{2}} \sum_{n=0}^{\infty} d_n (x-1)^n$$

La seconda soluzione non è accettabile in quanto presenta una singolarità logaritmica in $x = 1$. Quindi useremo un *ansatz* per la soluzione:
$$u(x) = (1-x)^{\frac{m}{2}} \sum_{n=0}^{\infty} \frac{(-l+m)_n(l+m+1)_n}{(1+m)_n} \frac{1}{n!} \left( \frac{1-x}{2} \right)^n$$

La serie si deve troncare garantendo al convergenza in $x = -1$, quindi $l \geq m$. In questo caso la serie si tronca ad un polinomio di grado $l-m$, concluendo le soluzioni accettabili:
$$u(x) = P_l^m(x)$$

Ritornando alla determinazione dello spettro di $L^2$ e vedendo la restrizione $l \geq m$ considerando anche valori negativi di $m$, il che ci porta a vederla come $-l \leq m \leq l$. Quindi lo spettro di $L^2$ è:
$$\delta = l(l+1) \hbar^2$$

Fissato $l$ abbiamo $2l+1$ valori possibili di $m$. Le autofunzioni di $L^2$ sono:
$$\psi_{lm}(\theta, \phi) = N_{lm} P_l^m(cos \theta) e^{im\phi}$$

Dove $N_{lm}$ è la costante di normalizzazione. Fissando la normalizzazione si ottengono autofunzioni che chiameremo *armoniche sferiche* $Y_l^m(\theta, \phi)$. $\\$
Esse sono autofunzioni di $L^2$ e $L_3$:
$$L^2 Y_l^m(\theta, \phi) = \hbar^2 l(l+1) Y_l^m(\theta, \phi)$$
$$L_3 Y_l^m(\theta, \phi) = \hbar m Y_l^m(\theta, \phi)$$

Il risultato per la generica armonica sferica normalizzata è:
$$Y_l^m(\theta, \phi) = \frac{(-1)^{l+m}}{2^l l!} \sqrt{\frac{2l+1}{4\pi} \frac{(l-m)!}{(l+m)!}} sin^m \theta \left( \frac{d}{d cos \theta} \right)^{l+m} sin^{2l} \theta e^{im\phi}$$

Soddisfano le relazioni di:
- ortogonalità
- completezza
- simmetria