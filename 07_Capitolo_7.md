# Capitolo 7: Algebra dei momenti angolari

## 7.1 Operatori di innalzamento e abbassamento

Si definiscono due operatori:
$$J_{\pm} = J_1 \pm iJ_2$$

Tali che $J^{\dagger}_{\pm} = J_{\mp}$.

Dalla relazione di commutazione $[J_j, J_k] = i\hbar \epsilon_{jkl} J_l$ si ottiene:
$$[J_3, J_{\pm}] = \pm J_{\pm}$$
$$[J_{+}, J_{-}] = 2J_3$$

Oltre ovviamente a $[J_{\pm}, J^2] = 0$.

Chiamiamo $\ket{j,m}$ gli autostati contemporaneamente di $J^2$ e $J_3$:
$$J^2 \ket{j,m} = j(j+1)\ket{j,m}$$
$$J_3 \ket{j,m} = m\ket{j,m}$$

L'azione di $J_{\pm}$ su $\ket{j,m}$ è:
$$J^2 J_{+} \ket{j,m} = J_{+} J^2 \ket{j,m} = j(j+1)J_{+} \ket{j,m}$$

Da cui capiamo che $J_{+} \ket{j,m}$ appartiene all'autospazio $j$ di $J^2$, con cui quindi è degenere.

La degenereazione viene risolta da $J_3$:
$$J_3 J_{+} \ket{j,m} = (m + 1)J_{+} \ket{j,m}$$

Quindi $J_{+} \ket{j,m}$ è un autostato di $J_3$ con autovalore $m+1$. Quindi è un operatore di innalzamento:
$$J_{+} \ket{j,m} = N_{j,m}^{+} \ket{j,m+1}$$

Analogamente si trova:
$$J_{-} \ket{j,m} = N_{j,m}^{-} \ket{j,m-1}$$

Le cui norme sono:
$$|N_{j,m}^{+}|^2 = j(j+1) - m(m+1)$$
$$|N_{j,m}^{-}|^2 = j(j+1) - m(m-1)$$

Le norme devono essere $\geq 0$, quindi $-j \leq m \leq j$. Dunque lo spettro di $J_3$ è limitato dai valori di quello di $J^2$.

Se consideriamo lo stato $\ket{j,m_0}$, ci costruiamo lo stato:
$$J_{-}^k \ket{j,m_0} = N_{j,m_0} N_{j,m_0-1} \ldots N_{j,m_0-k} \ket{j,m_0-k}$$

Esso avrà autovalore di $J_3$ $m_0 - k$, il quale se non è intero non è un autovalore di $J_3$, quindi il valore minimo di $m$ è $-j$.$\\$
Che ci porta allo stato minimo $\ket{j,-j}$. A cui applichiamo l'operatore di innalzamento.$\\$
Capiamo che il numero massimo che possiamo innalzare è $2j$, ovvero che gli unici numeri ammessi per $j$ sono interi o semi-interi.

La novità è che compaiono anche numeri di quantizzazione semi-interi. Ci chiediamo se questo è compatibile con un nuovo fenome fisico o è frutto di una scelta matematica.

## 7.3 Composizione di momenti angolari

Si consideri un sistema in cui sono stati definiti due momenti angolari $J^{(1)}$ e $J^{(2)}$, entrambi commutanti con $H$. Dunque uno stato del sistema a livello energetico $n$ potrà essere descritto da $j_1, m_1$ e $j_2, m_2$.$\\$
Si consideri l'operatore $J = J^{(1)} + J^{(2)}$, anch'essa commuta con $H$. Dunque uno stato del sistema a livello energetico $n$ potrà essere descritto da $j, m$.$\\$
Questi 6 numeri quantici non sono indipendenti.$\\$
Fissiamo $j_1$ e $j_2$, allora ci possiamo limitare al sottospazio di cui $\ket{m_1, m_2}$ è base. Tale spazio ha dimensione $(2j_1 + 1)(2j_2 + 1)$. $\\$
Dobbiamo dimostrare che anche $\ket{j, m}$ è base di tale spazio. Determiniano i valori possibili di $j$.$\\$
Gli autovalori di $J^2$ sono limitati da quelli di $(J^{(1)} + J^{(2)})^2$, più precisamente:
$$J^2 = J^{(1)2} + J^{(2)2} + 2J^{(1)}J^{(2)}$$

Quindi:
$$\lambda_j^2 = \lambda_{j_1}^2 + \lambda_{j_2}^2 + 2\lambda_{j_1}\lambda_{j_2} \cos \theta$$

Essendo che $-1 \leq \cos \theta \leq 1$, allora:
$$|\lambda_{j_1} - \lambda_{j_2}| \leq \lambda_j \leq \lambda_{j_1} + \lambda_{j_2}$$

Il che si ha solo se:
$$|j_1 - j_2| \leq j \leq j_1 + j_2$$

Per $m$ si ha:
$$m = m_1 + m_2$$

I numeri quantici $m_i$ sono limitati da $-j_i \leq m_i \leq j_i$. Il numero totali di stati possibili è quindi valutabile, se supponiamo che $j_1 \geq j_2$:
$$\sum_{j = |j_1 - j_2|}^{j_1 + j_2} (2j + 1) = (2j_1 + 1)(2j_2 + 1)$$

Quindi $\ket{j, m}$ è base di tale spazio.$\\$
La trasformazione tra le due basi è data da:
$$\ket{j, m} = \sum_{m_1=-j_1}^{j_1} \sum_{m_2=-j_2}^{j_2} \braket{m_1, m_2 | j, m} \ket{m_1, m_2}$$

Dove $\braket{m_1, m_2 | j, m}$ è detto coefficiente di Clebsch-Gordan. Esso è nullo se $m \neq m_1 + m_2$.$\\$

Denotiamo con $(j)$ l'autospazio di $J^2$ con autovalore $j(j+1)$ e dimensione $2j + 1$. Allora la regola generale di somma dei momenti angolari in questa notazione è:
$$(j_1) \otimes (j_2) = \bigoplus_{j = |j_1 - j_2|}^{j_1 + j_2} (j)$$
