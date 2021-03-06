---
title: Ensembles et relations
linktitle: Ensembles et relations
toc: true
type: book
date: "2019-10-06T00:00:00+01:00"
draft: false

weight: 1
---

## Lois de Morgan

Soient $A, B$ des ensembles, alors

$$\overline{A \cap B} = \overline{A} \cup \overline{B}\\\\\\
\overline{A \cup B} = \overline{A} \cap \overline{B}$$

**Preuve :**

1.  On commence par montrer $\overline{A \cap B} \subseteq \overline{A} \cup \overline{B}$, donc supposons $x \in \overline{A \cap B}$, i.e., $x \notin A \cap B$. Comme $A \cap B = \\{y \mid y \in A \text{ et } y \in B \\}$, alors $x \notin A$ ou $x \notin B$. Si $x \notin A$ donc $x \in \overline{A} \subseteq \overline{A} \cup \overline{B}$. Si $x \notin B$, donc $x \in \overline{B} \subseteq \overline{A} \cup \overline{B}$. Dans les deux cas $x \in \overline{A} \cup \overline{B}$ et en conséquence $\overline{A \cap B} \subseteq \overline{A} \cup \overline{B}$. 

    Pour montrer l'autre inclusion, supposons en raisonnant par l'absurde que $x \in \overline{A} \cup \overline{B}$ mais que $x \notin \overline{A \cap B}$. Donc $x \in A \cap B$, c'est-à-dire, $x \in A$ et $x \in B$; mais cela implique que $x \notin \overline{A}$ et $x \notin \overline{B}$, i.e., $x \notin \overline{A} \cup \overline{B}$, une contradiction. En conséquence $x \in \overline{A \cap B}$ et alors $\overline{A \cap B} = \overline{A} \cup \overline{B}$

2.  Supposons $x \in \overline{A \cup B}$, i.e., $x \notin A \cup B$. Comme $A \cup B = \\{y \mid y \in A \text{ ou } y \in B \\}$, alors $x \notin A$ et $x \notin B$. On peut en déduire immédiatement $x \notin \overline{A} \cap \overline{B}$.

    Pour l'autre inclusion, supposons $x \in \overline{A} \cap \overline{B}$ mais $x \notin \overline{A \cup B}$. Donc $x \in A \cup B$, c'est-à-dire, $x \in A$ ou $x \in B$, mais de $x \in \overline{A} \cap \overline{B}$ on sait que $x \notin A$ et $x \notin B$. On obtient une contradiction et en consequence $x \in  \overline{A \cup B}$, i.e., $\overline{A \cup B} = \overline{A} \cap \overline{B}$.

## Exercice 2

Soient $A, B, C$ trois parties de $E$.

1.  Montrer que $A \cap \overline{A \cap B} = A \cap \overline{B}$.
   
    **Solution :** En développant $\overline{A \cap B}$ selon les lois de de Morgan, on a $A \cap \overline{A \cap B}=A \cap (\overline A\cup \overline B)$. On utilise ensuite la distributivité de $\cap$ sur $\cup$ $A \cap (\overline A\cup \overline B)=(A \cap \overline A)\cup (A \cap \overline B)$ et $A \cap \overline A=\emptyset$ et on obtient finalement $A \cap \overline{A \cap B}= A \cap \overline B$.

2.  Montrer que si $A \cap B = A \cap C$ alors $A \cap \overline{B} = A \cap \overline{C}$
   
    **Solution :** Si $A\cap B=A\cap C$ alors $\overline{A \cap B}=\overline{A \cap C}$ donc $A\cap \overline{A\cap B} = A\cap \overline{A\cap C}$ et $A \cap \overline B=A \cap \overline C$, d'après la question~1.

3.  En déduire que $$A \cap \overline{B} = A \cap \overline{C} \text{ si et seulement si } A \cap B = A \cap C$$

    **Solution :** On a déjà montré une implication dans la question 2. Montrons l'implication en sens inverse à présent: supposons que $A \cap \overline B=A \cap \overline C$ alors $A \cap \overline{\overline B}=A \cap \overline{\overline C}$, d'après la question~2.  Puisque $\overline{\overline X}=X$ pour toute partie $X$ de $E$, on a donc $A \cap B = A \cap C$ ce qui nous assure donc de l'autre implication et de l'équivalence entre ces propositions.

## Exercice 10

Soit $T$ la relation des réels $\mathbb{R}$ définie par $$xTy \text{ sii } 0 \le x-y \le 1$$

1.  Montrer que $T^{-1}.T = \\{(x,y) \mid |x - z| \le 1\\}$

    **Indication :** Montrez que par définition de la composition, $$T^{-1}.T = \\{(x,y) \mid \exists y \in \mathbb{R} \text{ t.q. } 0 \le y -x \le 1, 0 \le y - z \le 1\\}$$ Après, supposons $S = \\{(x,y) \mid |x - z| \le 1\\}$ et montrez que $S = T^{-1}.T$. Pour montrer $T^{-1}.T \subseteq S$, commencez par montrer que $$0 \le y - x \le 1, 0 \le y - z \le 1 \Longrightarrow x - z \le 1.$$ Mais aussi que $$0 \le y - x \le 1, 0 \le y - z \le 1 \Longrightarrow -1 \le x - z.$$ Pour montrer $S \subseteq T^{-1}.T$, prenez $(x,z) \in S$ et $y = \max(x,z)$. Essayez de montrer aussi que $T.T^{-1} = \\{(x,y) \mid |x - z| \le 1\\}$.
