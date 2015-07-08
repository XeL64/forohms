# forohms
Forum (sens littéral/place_public du terme) public libre insubmersible incontrôlable

## Concept (si pas déjà existant) :
ui/interface multilangues (esperanto + autres)
forum like
blog like
reddit like
stackoverflow like

sphère public seulement, rien de privé (voir possibilité whisp/mp pour le privé)

## Gestion utilisateur :
Pas d'admin
2 profiles utilisateurs : profile sans inscription (rw faible poids pas d'apartenance communauté) & profile inscrit (rw poids double + appartenance communauté(s))
communauté(s)/groupe(s) dans la communauté globale (induit poids sur les votes, double/indice au sein d'une communauté)
sous appartenance : x2/incide n+1 poids
ex : 
non inscrit : poids 1 partout
inscrit : poids 2 partout
inscrit et appartenance communauté : poids 2 partout, poids 4 dans sa(ses) communauté(s)
inscrit et appartenance communauté public + communauté "privé": poids 2 partout, poids 4 dans sa communauté, poids 8 dans sa communauté privé (seule la comunauté privé l'est, le contenu est public : tout est lisible).

## Notion communauté public/privé:
grandes catégories (à déterminer par les inscrits) : communauté public (vote pour passer communauté privé à public)
création d'une communauté privé au sein de public : rubrique à pinpin : communauté privé.
exemple 1:
universe => earth => france : communauté public
création utilisateur inscrit : Paris (communauté privé)
% inscrits communauté france : vote communauté public Paris.

héritage "inverse"  exemple 2 :
universe => earth => france : communauté public
création utilisateur inscrit : Paris (communauté privé)
création utilisateur inscrit sous communauté privé Paris : 
communauté mon association/restaurant/passion/what ever lambda privé
% inscrits communauté france : vote communauté public lambda : lambda + Paris sous communauté public

adhésion communauté lambda : auto adhésion communauté(s) parente(s)

## Contenu :
tout est lisible : pas de suppression (masquage avec possibilité de relecture, gestion particulière pour le spam à déterminer)

## Automatisme : 
éviter le spam (concaténisation des spams pour réduire leur visibilité + vote communauté pour sortir un spam)

## Technique :
hébergement (à creuser ou pas) :
tahoe-LAFS (même contenu partout, point d'entrée gateway différent)
propagation / réplication / synchronisation (à vérifier : spec tahoe-LAFS)

type DB (à déterminer) :
Cassandra
ZODB

web app => pointeur arbo vers gateway tahoe-LAFS
explorateur de communauté : point d'entrée : navigation parents/enfants
exemple :
forohms.com : help
point d'entrée : forohms.com/universe : 
nav :
up : help
down : forohms.com/earth
lambda.com : help
point d'entrée : forohms.com/universe/earth/france/paris/lambda (=) lambda.com/lambda
nav :
up : paris
down : none

réflexion à poursuivre...
