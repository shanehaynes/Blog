---
layout: post
title: "Closeness and Complexity: Modal Reasoning in the Vicinity of Nash Equilibrium"
date: 2025-02-17
author: "Shane Haynes"
---

Nash Equilibrium has been a foundational concept in game theory for decades: it has served as a benchmark for rational decision making agents in strategic, interactive contexts. However, real-world conditions, such as bounded rationality, computational complexity, and incomplete or asymmetric information, can make exact equilibria difficult to identify or achieve in practice. The following essay proposes a theoretical extension, employing modal logic and metric spaces, that shifts the paradigm of equilibrium from an exact point towards an approximate, locally stable state which we are then are able to classify as "robust" or "weak" equilibrium. By doing so, we gain a deeper understanding of the approximate equilibrium that captures the complexity of real world strategic behavior. 

### Game Theory

Game theory is the formal study of strategic decision making where multiple agents, or "players", interact (players can be people, computational agents, organizations, genes, etc). Each player's payoff depends not only on their actions but the actions of other players in the game (von Neumann & Morgenstern 1944). Game theory gives us tools, such as mathematical models, equilibrium concepts, and solution techniques, to predict, prescribe, or explain the outcomes of interactive scenarios ranging in complexity from simple contrived games to global economic policies. Fundamental to these models is an assumption that each player is rational: players have well defined preferences and strive to optimize their payoff by performing calculations given their beliefs about other players actions. 

Over decades of development and use, game theory has become a cornerstone in economics, political science, evolutionary biology, and computer science while other fields continually find new ways of incorporating game theoretic models.  Under ideal conditions, this theoretical framework allows analysts to identify stable patterns of behavior that, in principle, should emerge from intelligent, forward-looking agents engaged in strategic interactions. 

### Nash Equilibrium: A Preeminent Concept in Game Theory

A prominent concept in game theory is Nash Equilibrium (Nash 1950). Nash Equilibrium is one of many end-state concepts in game theory and while not the most sophisticated, it is the most widely used. It has even been argued that Nash Equilibrium underpins all economic thought (Meyerson 1999). In Nash Equilibrium, no player can profitably deviate by unilaterally changing their strategy. Formally, a Nash Equilibrium is when:

*N = the set of n players {1,2,..., n} where each player is indexed by i $\in$ N
S = S$_1$ , S$_2$ , ... S$_n$ 
S$_i$ = finite set of actions player i can make*
*s$_i$ = a strategy profile for player i 
s$_{-{i}}$ = (s$_1$ ,.... s$_{i{-{1}}}$ , s$_{i{+{1}}}$ , ... s$_n$)

Let *s = (s$_i$ , s$_{-{i}}$)* be a strategy profile

*u$_i$(s$_i$ , s${_-{_i}}$)* = payoff gained by player *i* given strategy profile *s*

*s* is a Nash Equilibrium $\iff$ *u$_i$(s$_i$ , s${_-{_i}}$)* $\ge$ *u$_i$(s${_i}{^`}$ , s${_-{_i}}$)* for every *s$_i$* $\in$ *S$_i$* and each player *i* 

Nash's theorem states that when the game has finite players and finite games, there is guaranteed to be at least one equilibrium (Nash 1950). This claim has had profound influence, suggesting that stable outcomes of strategic interactions can be mathematically assured. Viewed in this light, equilibrium appears to be a normative benchmark: if rational players understand the game and each others rationality, they ought to settle on equilibrium strategies. Equilibria can also be viewed as a predictive tool, useful for understanding how rational agents will likely behave in ideal conditions. 

Nash Equilibrium's prominence does not mean it is without its pitfalls. Empirical and experimental work has cast doubt on its real-world realizability. Players operating in the real world often rely upon heuristics rather than identifying and calculating the equilibrium of complex games (Simon 1957). There is a myriad of factors that may contribute to discrepancy between theory and practice. Here are couple worth highlighting:

1. Bounded Rationality: Humans, and current computational agents, lack the vast  cognitive resources often assumed by theory. Moreover, equilibrium in nontrivial games can be computationally hard to find (Papadimitriou 2001). Players may be unable to perform the complex iterative calculations that ensure equilibrium is reached, such as in the instance of p-beauty contest games (Camerer 2003). This may be particularly true in instances of limited time. 
2. Evidence Against Strict Equilibrium Play: Controlled experiments have shown that stable but non-equilibrium outcomes can exist in which players hover around certain regions of the strategy space. After prolonged learning or adaptation, players may converge on a precise equilibrium but this is not guaranteed (Fudenberg & Levine 1998). 
3. Players may not all be equally or entirely rational. A plethora of papers discuss findings based upon this notion, some famous ones being *Nudge* (Thaler 2008), *Fast and Slow* (Kahneman's 2011), and *Predictably Irrational* (Ariely's 2008).

While Nash Equilibrium has great use in theoretical models, it is too unrealizable to serve as a normative or predictive tool in real world strategic games. 

### Nearness to Equilibrium: Accounting for Limited Usability

To account for the practical limitations of Nash Equilibrium, approximate equilibrium and local stability concepts have been used (Daskalakis & Goldberg & Papadimitriou 2008, Fudenberg & Levine 1998). An $\epsilon$-Nash Equilibrium is a strategy profile *s* such that no player can gain more than $\epsilon$ in payoff by unilaterally deviating from their strategy in *s*. The notion of $\epsilon$-Nash Equilibrium relaxes the strict equilibrium condition by allowing that no player can positively deviate by more than $\epsilon$. $\epsilon$-Nash Equilibrium acknowledges that players may achieve stable "good enough" solutions as opposed to perfectly optimized ones. However, this brings up the question: how could we formally reason about how close a strategy profile is to equilibrium?

Let us introduce a distance equation for formally reasoning a strategy profile's closeness to equilibrium. Strategy profiles are points in a metric space, enabling us to measure "nearness to equilibrium". By defining a distance function *d($\cdot$ , $\cdot$)* over the set of strategy profiles, we can quantify how far a given strategy profile is from an exact equilibrium. We do this by subtracting the corresponding values of the points of our player's chosen strategy profile, *s$_1$* from our player's closest equilibrium strategy profile, s${_1}{^`}$*. 

Suppose each player's strategy profile is represented by a *p*-dimensional vector *x$_i$* where *x$_i$ = (x${_i}{_1}$ , x${_i}{_2}$, .... , x${_i}{_p}$)* and *p* represents the size of player *i*'s strategy profile. Each player also has a strategy profile that is the nearest Nash Equilibrium represented by *p*-dimensional vector *y*$_i$ where *y$_i$ = (y${_i}{_1}$ , y${_i}{_2}$, .... , y${_i}{_p}$)* and *p*, again, represents the size of player *i*'s strategy profile. 

We will then use the Euclidian distance formula to measure the distance between vector *x$_i$* and *y$_i$*: 

d$_p$(x , y) = $\sqrt{\sum_{j=1}^{p} (x_j - y_j)^2}$ 

Now suppose we have *N* players, each with chosen strategy profile *x$_i$*. A strategy profile for *N* players would then be: 

*s = (x$_1$ , x$_2$ , ... , x$_n$).*

The strategy profile of *N* players for which the outcome is the nearest Nash Equilibrium is then:

*t = (y$_1$ , y$_2$ , ... , y$_n$).*

To measure the distance between *s* and *t*, we will sum the differences between each players strategy profiles. 

d$_p$(s , t) = $\sum_{i=1}^{n}d_p(x_1,y_1)$ 

Finally, to provide a more intuitive measure, we will divide this sum by the number of players, *N*, in the game to produce an average:

$\frac{1}{N}$d$_p$(s , t)

The provided distance formula can also account for heterogenous players with dimensionally different strategy sets. The set of strategy profiles would then be a tuple of dimensionally different vectors. The key principles of: 1. Represent each players strategy in metric space, 2. Measure said distance (for our purposes, via Euclidian distance), and 3. Aggregate players distances to end up with a final measure of the difference between two strategy profiles will remain. 

Various aggregation methods would yield different distances. This paper only demonstrates the average of all players distances as it describes a holistic understanding of the strategy profile of the game. Another popular method for aggregation for the distances between strategy profiles is to only consider the player's strategy which is farthest from equilibrium, since that agent will likely be the limiting factor. To gain a deeper understanding of the set of strategy profiles played and their divergence from the equilibrium set of strategy profiles, it may be useful to utilize a plethora of various metrics.  
##### Distance Formula Example

Imagine a two player game where the only two choices for each player is A or B. Let player one adopt a mixed strategy of (.7,.3) and player two adopt a mixed strategy of (.5,.5). Lastly, assume that the Nash Equilibrium is (.5,.5). The distance the strategy profile ((.7,.3),(.5,.5)) has from the nearest Nash Equilibrium is: 

Player 1 distance:
*d$_2$(x${_1}$,y${_1}$) = $\sqrt{(.7-.5)^2+ (.3 - .5)^2}$ $\approx$ 0.283

Player 2 distance:
*d$_2$(x${_1}$,y$_1$) = $\sqrt{(.5-.5)^2+ (.5 - .5)^2}$ = 0

Total distance:
0.283 + 0 = 0.283

### Modal Operators

We can then include parameterized modal operators $\square$ and $\Diamond$. In classical, non modal logic, statements are simply true or false in a single "world".  Modal logic allows us to incorporate operators like $\square$ and $\Diamond$ to quantify over various "worlds" or "states"  (Blackburn & de Rijke & Venema 2001). In modal logic, we imagine differing possible worlds to represent the ways a world could be. 

In standard Kripke semantics for modal logic, we have:

- A set of worlds *W*.
- An individual world *w*.
- An accessibility relation *R ⊆ W × W* that determines which worlds are accessible from which other worlds.
- A valuation that assigns truth values to propositions in each world.

A statement like $\square_\phi$ is true at *w* if and only if for every accessible world, $\phi$ holds at w'. Formally:

*w $\models$ $\square_\phi$ $\iff$ $\forall$ w' $\in$ W such that (w, w') $\in$ R, w' $\models$ $\phi$*

Similarly, a statement like $\Diamond_\phi$ is true if at *w*, there exists an accessible world where $\phi$ holds at *w*'. Formally: 

*w $\models$ $\Diamond_\phi$ $\iff$ $\exists$ w' $\in$ W such that (w, w') $\in$ R and w' $\models$ $\phi$*

For our purposes, worlds represent various strategy profiles. The accessibility relation *R$_\epsilon$* is defined on the set of strategy profiles *S* by *(s, s')* $\in$  *R$_\epsilon$* $\iff$ *d(s,s') < $\epsilon$*. Therefore, our modal operators are:

- $\square_\epsilon$$\psi$ reads: $\psi$ holds in all profiles within $\epsilon$-distance of the current strategy profile
- $\Diamond_\epsilon$$\psi$ reads: $\psi$ holds in at least one strategy profile within $\epsilon$-distance of the current strategy profile

where $\psi$ represents Nash Equilibrium. 

These modal statements capture approximate stability which will allow us to classify strategy profiles as "robustly" reaching a Nash Equilibrium or "weakly" reaching Nash Equilibrium. If $\Box$$_\epsilon$$\psi$ holds, it means that the entire neighborhood around *s* maintains the desired stability which means the strategy profile robustly reaches Nash Equilibrium. Robust Nash Equilibria suggest that, even with small changes in the strategy profile, the equilibrium will persist. This could be interpreted normatively as, "Even if rational players unpredictably or mistakenly change their strategy in small ways, the equilibrium is robustly stable and will be reached."  If $\Diamond$$_\epsilon$$\psi$ holds at profile *s*, it means that there is some equilibrium within $\epsilon$ which means the strategy profile weakly reaches Nash Equilibrium. Weak Nash Equilibria appear more descriptive or predictive: over long periods of time and/or iterative processes, players are likely to converge on equilibrium.

This approach provides a structural lens through which we can understand strategic behavior as weakly or robustly stable. Under real-world conditions and limitations, players may never realize a single, exact equilibrium but they may find themselves in regions of the strategy space where no small unilateral deviation yields a significant payoff improvement. These local basins of approximate equilibrium are then logically characterized through modal operators, offering a principled method to describe, measure, and verify approximate solutions. 

##### Modal Operator Example

Building off the distance formula example, let us say $\epsilon$ is 0.3. Therefore, we can say:

- $\square_\epsilon$$\psi$ does not hold as there are strategy profiles within 0.3 distance of our current strategy profile that are not a Nash Equilibrium.
- $\Diamond_\epsilon$$\psi$ holds as there is at least one strategy profile (the strategy profile (0.5,0.5) which we determined is 0.283 away) that is a Nash Equilibrium within 0.3 of our current strategy profile. 

### Conclusion

Through a combination of metric based distance measures for approximate Nash Equilibria and introducing modal logic operators $\square$ and $\Diamond$, we are able to classify approximate Nash Equilibria as robust or weak. "Robust" equilibria emerge as normatively appealing, stable configurations that persist under small deviations, while "weak" equilibria indicate that equilibrium conditions are only locally or occasionally met. This dichotomy refines our understanding for whether a Nash Equilibrium can be viewed as realistic targets for rational agents or merely theoretical idealizations, likely only attainable over substantial periods of time.

Ultimately, such a framework moves game theory closer to the complexities of real-world decision-making, where exact equilibria are rare and approximate stability and local predictability guide strategic behavior. By introducing the aforementioned modal operators, we gain a formal language for distinguishing varying levels of robustness in Nash Equilibria. 

### References

Ariely, D. (2008). _Predictably Irrational: The Hidden Forces That Shape Our Decisions._ HarperCollins.

Blackburn, P., de Rijke, M., & Venema, Y. (2001). _Modal Logic._ Cambridge University Press.

Camerer, C. F. (2003). _Behavioral Game Theory: Experiments in Strategic Interaction._ Princeton University Press.

Daskalakis, C., Goldberg, P. W., & Papadimitriou, C. H. (2008). The complexity of computing a Nash equilibrium. _SIAM Journal on Computing_, 39(1)

Fudenberg, D., & Levine, D. K. (1998). _The Theory of Learning in Games._ MIT Press.

Kahneman, D. (2011). _Thinking, Fast and Slow._ Farrar, Straus and Giroux.

Myerson, R. B. (1999). Nash equilibrium and the history of economic theory. _Journal of Economic Literature_, 37(3)

Nash, J. F. (1950). Equilibrium points in n-person games. _Proceedings of the National Academy of Sciences_, 36(1)

Papadimitriou, C. H. (2001). Algorithms, games, and the internet. In _Proceedings of the Thirty-Third Annual ACM Symposium on Theory of Computing_. ACM.

Simon, H. A. (1957). _Models of Man: Social and Rational._ Wiley.

Thaler, R. H., & Sunstein, C. R. (2008). _Nudge: Improving Decisions about Health, Wealth, and Happiness._ Yale University Press.

Von Neumann, J., & Morgenstern, O. (1944). _Theory of Games and Economic Behavior._ Princeton University Press.

