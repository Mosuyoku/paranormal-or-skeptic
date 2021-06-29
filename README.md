Skeptic vs paranormal subreddits
================================

Classify a reddit as either from Skeptic subreddit or one of the
"paranormal" subreddits (Paranormal, UFOs, TheTruthIsHere, Ghosts,
,Glitch-in-the-Matrix, conspiracytheories).

Output label is the probability of a paranormal subreddit.

Sources
-------

Data taken from <https://archive.org/details/2015_reddit_comments_corpus>.


## Cel projektu
Przewidzenie czy dany post na reddicie pochodzi ze „sceptycznych” subredditów, czy z „paranormalnych” subredditów.

## Dane
Dane pochodzą z wyzwania „Skeptic vs paranormal subreddits” na platformie gonito.net (link: https://gonito.net/challenge/paranormal-or-skeptic.
Zbiór jest podzielony na 289579 przykładów uczących oraz 5272 przykładów testowych.

## Modele
W projekcie porównano działanie 3 modeli:
* Regresja liniowa.
* Regresja logistyczna korzystająca z solvera lbfgs.
* Klasyfikator SGD.

## Ewaluacja
Do ewaluacji wykorzystano metryki accuracy, precision, recall i F1-score. Wyniki ewaluacji przedstawia poniższa tabelka:

Model | Accuracy | Precision | Recall | F1-score
| :---: | :---: | :---: | :---: | :---: |
Regresja liniowa  | 0.7083 | 0.6513 | 0.3783 | 0.4786
Regresja logistyczna  | 0.7123 | 0.6382 | 0.4319 | 0.5152
Klasyfikator SGD  | 0.7191 | 0.6224 | 0.5247 | 0.5694

## Wnioski
Najlepsze rezultaty uzyskał Klasyfikator SGD. Warto zauważyć, że Recall malał wraz ze wzrostem pozostałych metryk. Stąd też w przypadku regresji liniowej Precision było największe, mimo najsłabszych pozostałych wyników, a w przypadku SGD Precision było najniższe, mimo najlepszych wyników (szczególnie Recall i F1).
