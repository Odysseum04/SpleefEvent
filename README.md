# SpleefEvent


Pour calculer l'intégrale \(\int_{4}^{+\infty} e^{-x^3} \cos x \, dx\) en utilisant la méthode des trapèzes avec 11 pivots, nous devons d'abord effectuer un changement de variable adéquat pour transformer l'intervalle infini en un intervalle fini. Considérons une substitution courante pour des limites infinies, telle que \( x = \frac{1}{t} \).

En effectuant ce changement de variable \( x = \frac{1}{t} \), nous avons :

\[ dx = -\frac{1}{t^2} dt \]

et les bornes changent comme suit :

- Quand \( x \to +\infty \), \( t \to 0 \)
- Quand \( x = 4 \), \( t = \frac{1}{4} \)

L'intégrale devient alors :

\[ I = \int_{0}^{1/4} e^{-\left(\frac{1}{t}\right)^3} \cos \left(\frac{1}{t}\right) \left(-\frac{1}{t^2}\right) dt \]

\[ I = \int_{0}^{1/4} -\frac{e^{-\frac{1}{t^3}} \cos \left(\frac{1}{t}\right)}{t^2} \, dt \]

Retirons le signe moins par changement de borne :

\[ I = \int_{1/4}^{0} \frac{e^{-\frac{1}{t^3}} \cos \left(\frac{1}{t}\right)}{t^2} \, dt \]

\[ I = \int_{0}^{1/4} \frac{e^{-\frac{1}{t^3}} \cos \left(\frac{1}{t}\right)}{t^2} \, dt \]

Maintenant, nous pouvons appliquer la méthode des trapèzes. 

Avec 11 pivots, l'intervalle \([0, 1/4]\) est divisé en 10 sous-intervalles égaux. La largeur de chaque sous-intervalle est :

\[ h = \frac{1/4 - 0}{11-1} = \frac{1}{40} = 0.025 \]

Les points de pivot sont donc :

\[ t_i = i \cdot h = i \cdot 0.025 \quad \text{pour} \quad i = 0, 1, 2, \ldots, 10 \]

Ensuite, nous utilisons la formule des trapèzes :

\[ I \approx \frac{h}{2} \left[ f(t_0) + 2 \sum_{i=1}^{n-1} f(t_i) + f(t_n) \right] \]

où \( f(t) = \frac{e^{-1/t^3} \cos (1/t)}{t^2} \).
