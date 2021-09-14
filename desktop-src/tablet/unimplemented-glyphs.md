---
description: La liste suivante répertorie les glyphes de mouvements que Microsoft envisage de prendre en charge à l’avenir dans le cadre du module de reconnaissance de mouvement Microsoft.
ms.assetid: 4d504140-ff48-4a07-9bf7-a36913e44426
title: Glyphes non implémentés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d479c6f3b486706b9e8d063ae2bc46daf5a0a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296011"
---
# <a name="unimplemented-glyphs"></a>Glyphes non implémentés

La liste suivante répertorie les glyphes de mouvements que Microsoft envisage de prendre en charge à l’avenir dans le cadre du module de *reconnaissance de mouvement Microsoft*. Le travail est en cours pour s’assurer que la précision de la reconnaissance pour ces glyphes est élevée (pour éviter une activation accidentelle) et qu’ils correspondent aux opérations appropriées.

Pour garantir la cohérence des *mouvements* utilisés pour les *actions* courantes entre les applications, vous devez respecter les suggestions suivantes :

-   L' *action* est le comportement sémantique suggéré associé au geste.
-   Pour les mouvements étiquetés comme indiqué dans le tableau suivant, il est *recommandé de ne* pas modifier le comportement de sémantique suggéré. Si une application n’a pas besoin du comportement sémantique spécifié, il est recommandé de ne pas réutiliser le geste pour une autre action ou sémantique.
-   N’hésitez pas à associer des comportements sémantiques pertinents à tous les autres gestes. Ces mouvements sont étiquetés comme étant *spécifiques à l’application*. Pour les gestes qui présentent un comportement sémantique suggéré, il est recommandé d’utiliser le geste pour la sémantique suggérée si la fonctionnalité correspondante existe dans votre application.
-   Le point réactif d’un mouvement est un point distinctif dans la géométrie du mouvement. Le point réactif peut être utilisé pour déterminer où le mouvement a été effectué. L’API gestes permet de déterminer le point réactif pour un mouvement donné. Toutefois, tous les mouvements n’ont pas un point chaud spécifique. Pour ceux qui n’ont pas de point de connexion distinctif spécifique, le point de départ est signalé comme point chaud.

> [!Note]  
> Certains des mouvements ont un point névralgique distinctif qui se trouve juste être le point de départ. Ils sont distingués dans la table.

 



| Nom du geste                      | Action                                         | Fixe                           | Point réactif                                                           |
|-----------------------------------|------------------------------------------------|---------------------------------|---------------------------------------------------------------------|
| Infini<br/>               | Basculer vers et hors du mode de mouvement<br/> | Fixe<br/>                | Point de départ<br/>                                           |
| Croix<br/>                  | DELETE<br/>                              | Spécifique à l’application<br/> | Intersection des traits<br/>                              |
| Marque de paragraphe<br/>         | Nouveau paragraphe<br/>                       | Fixe<br/>                | Point de départ<br/>                                           |
| Section<br/>                | Nouvelle section<br/>                         | Fixe<br/>                | Point de départ<br/>                                           |
| Sélectionnées<br/>                 | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Intersections<br/>           | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Repère<br/>               | Gras<br/>                                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Échange<br/>                   | contenu Exchange<br/>                    | Spécifique à l’application<br/> | Milieu du trait de haut<br/>                                  |
| Openup<br/>                 | Ouvrir un espace entre les mots<br/>         | Spécifique à l’application<br/> | Milieu du trait de soutropie<br/>                                |
| Gros plan<br/>                | Fermer l’espace supplémentaire<br/>                | Spécifique à l’application<br/> | Centre de l’espace vertical entre les deux parenthèses<br/> |
| Rectangle<br/>              | Sélectionne le contenu délimité<br/>            | Fixe<br/>                | Point de départ<br/>                                           |
| Entourer-cliquer<br/>             | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Taper<br/>                                                      |
| Cercle-cercle<br/>          | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Cercle-Croix<br/>           | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Cercle-ligne-vertical<br/>   | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Cercle-ligne-horizontal<br/> | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Double flèche vers le haut<br/>        | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Double flèche vers le bas<br/>      | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Double flèche vers la gauche<br/>      | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Double flèche droite<br/>     | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Flèche haut-gauche<br/>          | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Haut-Flèche droite<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Flèche bas-gauche<br/>        | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Bas-flèche droite<br/>       | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Flèche gauche vers le haut<br/>          | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                               |
| Flèche gauche-bas<br/>        | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Flèche droite vers le haut<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Flèche vers le bas<br/>       | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Sommet de la tête de flèche<br/>                                   |
| Diagonale-leftup<br/>        | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Diagonale-rightup<br/>       | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Diagonale-leftdown<br/>      | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Diagonale-rightdown<br/>     | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-A<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-B<br/>         | Gras<br/>                                | Fixe<br/>                | Point de départ<br/>                                           |
| Lettre latine-C<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-D<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-E<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-F<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-G<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-H<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-I<br/>         | Italique<br/>                              | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-J<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-K<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-L<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-M<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-N<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-O<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-P<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-Q<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-R<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-S<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-T<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-U<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-V<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-W<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-X<br/>         | Couper<br/>                                 | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-Y<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Lettre latine-Z<br/>         | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Chiffre-0<br/>                | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Chiffre-1<br/>                | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Chiffre-2<br/>                | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Chiffre-3<br/>                | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Chiffre-4<br/>                | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Chiffre-5<br/>                | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Chiffre-6<br/>                | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Chiffre-7<br/>                | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Chiffre-8<br/>                | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Chiffre-9<br/>                | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Point d'interrogation<br/>          | Aide<br/>                                | Fixe<br/>                | Centrer le long de la hauteur de la courbe<br/>                     |
| Limitée<br/>                  | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Investi<br/>                 | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Astérisque<br/>               | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Center<br/>                                                   |
| Plus<br/>                   | Coller<br/>                               | Fixe<br/>                | Intersection des traits<br/>                              |
| Double-haut<br/>              | Faire défiler vers le haut<br/>                           | Fixe<br/>                | Point de départ<br/>                                           |
| Double-point<br/>            | Faire défiler vers le bas<br/>                         | Fixe<br/>                | Point de départ<br/>                                           |
| Double-gauche<br/>            | Faire défiler vers la gauche<br/>                         | Fixe<br/>                | Point de départ<br/>                                           |
| Double-droite<br/>           | Faire défiler vers la droite<br/>                        | Fixe<br/>                | Point de départ<br/>                                           |
| Triple<br/>              | Page précédente<br/>                             | Fixe<br/>                | Point de départ<br/>                                           |
| Tripler<br/>            | Page suivante<br/>                           | Fixe<br/>                | Point de départ<br/>                                           |
| Triple gauche<br/>            | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Triple droite<br/>           | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Point de départ<br/>                                           |
| Crochet sur<br/>           | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Midpoint<br/>                                                 |
| Crochet-inférieur à<br/>          | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Midpoint<br/>                                                 |
| Crochet gauche<br/>           | Début de la sélection<br/>                  | Fixe<br/>                | Midpoint<br/>                                                 |
| Crochet droit<br/>          | Fin de la sélection<br/>                    | Fixe<br/>                | Midpoint<br/>                                                 |
| Accolade-au-dessus<br/>             | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Midpoint<br/>                                                 |
| Accolade-sous<br/>            | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Midpoint<br/>                                                 |
| Accolade-gauche<br/>             | Début de la sélection discontinue<br/>    | Fixe<br/>                | Midpoint<br/>                                                 |
| Accolade droite<br/>            | Fin de la sélection discontinue<br/>      | Fixe<br/>                | Midpoint<br/>                                                 |
| Robinet triple<br/>             | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Le point de départ distingue le point chaud<br/>               |
| Quadruple pression<br/>          | Spécifique à l’application<br/>                | Spécifique à l’application<br/> | Le point de départ distingue le point chaud<br/>               |



 

 

 




