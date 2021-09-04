---
title: Vue d’ensemble de la liaison de ressources
description: Les clés pour la compréhension de la liaison de ressources dans DirectX 12 sont les concepts des descripteurs, des tables de descripteurs, des tas de descripteurs et des signatures racines.
ms.assetid: 92E100CA-822D-46B1-BD37-FF57C3FB703D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657e380c58182fee8ad2c82f3af0c6fdd5ffec76
ms.sourcegitcommit: 8a211d404470a6a2790733ed2894cfaf92bddd70
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2021
ms.locfileid: "123464102"
---
# <a name="resource-binding-overview"></a>Vue d’ensemble de la liaison de ressources

Les clés pour la compréhension de la liaison de ressources dans DirectX 12 sont les concepts des descripteurs, des tables de descripteurs, des tas de descripteurs et des signatures racines.

## <a name="resources-and-the-graphics-pipeline"></a>Ressources et pipeline graphique

Les ressources de nuanceur (telles que les textures, les tables constantes, les images, les mémoires tampons, etc.) ne sont pas directement liées au pipeline de nuanceur. au lieu de cela, ils sont référencés via un *descripteur*. Un descripteur est un petit objet qui contient des informations sur une ressource.

Les descripteurs sont regroupés en *tables* de descripteurs de formulaire. Chaque table de descripteur stocke des informations sur une plage de types de ressources. Il existe de nombreux types de ressources. Les ressources les plus courantes sont les suivantes :

-   Vues de mémoire tampon constante (CBVs)
-   Vues d’accès non ordonnées (UAVs)
-   Vues des ressources de nuanceur (SRVs)
-   Échantillonneurs

Les descripteurs SRV, UAV et CBVs peuvent être combinés dans la même table de descripteurs.

Les pipelines graphiques et de calcul accèdent aux ressources en faisant référence aux tables de descripteurs par index.

Les tables de descripteurs sont stockées dans un *tas de descripteur*. Dans l’idéal, les tas de descripteurs contiennent tous les descripteurs (dans les tables de descripteurs) pour un ou plusieurs frames à restituer. Toutes les ressources sont stockées dans des tas en mode utilisateur.

Un autre concept est celui d’une *signature racine*. La signature racine est une convention de liaison, définie par l’application, qui est utilisée par les nuanceurs pour localiser les ressources auxquelles elle doit accéder. La signature racine peut stocker les éléments suivants :

-   Indexe les tables de descripteur dans un tas de descripteur, où la disposition de la table de descripteur a été prédéfinie.
-   Les constantes, afin que les applications puissent lier des constantes définies par l’utilisateur (appelées *constantes racine*) directement aux nuanceurs sans avoir à passer par des descripteurs et des tables de descripteur.
-   Un très petit nombre de descripteurs directement à l’intérieur de la signature racine, comme une vue de mémoire tampon constante (CBV) qui change par dessin, ce qui évite à l’application d’avoir à placer ces descripteurs dans un tas de descripteur.

En d’autres termes, la signature racine fournit des optimisations de performances appropriées pour les petites quantités de données qui changent par dessin.

La conception Direct3D 12 pour la liaison la sépare des autres tâches, telles que la gestion de la mémoire, la gestion de la durée de vie des objets, le suivi de l’État et la synchronisation de la mémoire (reportez-vous aux [différences dans le modèle de liaison de Direct3D 11](binding-model.md)). La liaison Direct3D 12 est conçue pour une surcharge faible et est optimisée pour les appels d’API qui sont effectués le plus fréquemment. Il est également évolutif sur un matériel de bas en bout à haut niveau, et évolutif à partir d’une version plus ancienne (pipeline Direct3D 11 plus linéaire) vers les approches plus récentes (plus parallèles) de la programmation du moteur graphique.

## <a name="resource-types-and-views"></a>Types et vues de ressources

Les types de ressources sont les mêmes que Direct3D 11, à savoir :

-   Texture1D et Texture1DArray
-   Texture2D et Texture2DArray, Texture2DMS, Texture2DMSArray
-   Texture3D
-   Mémoires tampons (typées, structurées et brutes)

Les vues de ressources sont similaires, mais légèrement différentes de celles de Direct3D 11, les vues de mémoire tampon de vertex et d’index ont été ajoutées.

-   Affichage des mémoires tampons de constantes (CBV)
-   Vue d’accès non triée (UAV)
-   Affichage des ressources de nuanceur (SRV)
-   Échantillonneurs
-   Affichage de la cible de rendu (RTV)
-   Vue du stencil de profondeur (DSV)
-   Vue de la mémoire tampon d’index (IBV)
-   Vue de la mémoire tampon de vertex (VBV)
-   Vue de sortie de flux (SOV)

Seules les quatre premières de ces vues sont réellement visibles pour les nuanceurs, reportez-vous aux [tas du descripteur visible du nuanceur](shader-visible-descriptor-heaps.md) et aux [tas de descripteurs visibles non nuanceur](non-shader-visible-descriptor-heaps.md).

## <a name="resource-binding-flow-of-control"></a>Flow-of-Control de la liaison de ressources

En se concentrant uniquement sur les signatures racines, les descripteurs racine, les constantes racine, les tables de descripteurs et les tas de descripteurs, le déroulement de la logique de rendu d’une application doit être similaire à ce qui suit :

-   Créez un ou plusieurs objets de signature racine, un pour chaque configuration de liaison différente dont une application a besoin.
-   Créez des nuanceurs et un état de pipeline avec les objets de signature racine avec lesquels ils seront utilisés.
-   Créez un ou plusieurs tas de descripteurs (ou, le cas échéant) qui contiendront tous les descripteurs SRV, UAV et CBV pour chaque trame de rendu.
-   Initialiser le ou les tas (s) de descripteur avec des descripteurs dans la mesure du possible pour les jeux de descripteurs qui seront réutilisés dans plusieurs frames.
-   Pour chaque frame à rendre :
    -   Pour chaque liste de commandes :
        -   Définissez la signature racine actuelle à utiliser (et modifiez-la si nécessaire pendant le rendu, ce qui est rarement requis).
        -   Mettez à jour les constantes et/ou les descripteurs de signature racine de la signature racine pour la nouvelle vue (par exemple, les projections de type World/View).
        -   Pour chaque élément à dessiner :
            -   Définissez tous les nouveaux descripteurs dans les tas de descripteurs en fonction des besoins pour le rendu par objet. Pour les tas de descripteurs visibles par le nuanceur, l’application doit veiller à utiliser un espace de tas de descripteur qui n’est pas déjà référencé par un rendu pouvant être en cours d’utilisation, par exemple pour allouer de manière linéaire l’espace via le tas du descripteur pendant le rendu.
            -   Mettez à jour la signature racine avec des pointeurs vers les régions requises des tas de descripteurs. Par exemple, une table de descripteur peut pointer vers certains descripteurs statiques (immuables) initialisés précédemment, tandis qu’une autre table de descripteurs peut pointer vers certains descripteurs dynamiques configurés pour le rendu actuel.
            -   Mettez à jour les constantes et/ou les descripteurs de signature racine de la signature racine pour le rendu par élément.
            -   Définissez l’état du pipeline pour l’élément à dessiner (uniquement si la modification est nécessaire), compatible avec la signature racine actuellement liée.
            -   Dessin
        -   Répéter (élément suivant)
    -   Répéter (liste de commandes suivante)
    -   Une fois que le GPU a terminé avec une mémoire qui n’est plus utilisée, il peut être libéré. Les références aux descripteurs qu’il contient n’ont pas besoin d’être supprimées si un rendu supplémentaire qui utilise ces descripteurs n’est pas envoyé. Ainsi, le rendu suivant peut pointer vers d’autres zones dans des tas de descripteurs, ou les descripteurs obsolètes peuvent être remplacés par des descripteurs valides pour réutiliser l’espace du tas du descripteur.
-   Répéter (Frame suivant)

Notez que les autres types de descripteurs, les vues de la cible de rendu (RTVs), les vues de stencil de profondeur (DSV), les vues de tampon d’index (IBVs), les vues de mémoire tampon de vertex (VBVs) et les vues d’objets de nuanceur (SOV) sont gérés différemment. Le pilote gère le contrôle de version de l’ensemble des descripteurs liés pour chaque dessin au cours de l’enregistrement de la liste de commandes (de la même façon que les liaisons de signature racine sont gérées par le matériel/pilote). Cela diffère du contenu des tas de descripteurs visibles par le nuanceur, pour lesquels l’application doit être allouée manuellement via le tas, car elle référence des descripteurs différents entre les dessins. Le contrôle de version du contenu de segment de mémoire visible par Shader est laissé à l’application, car il permet aux applications d’effectuer des opérations telles que la réutilisation de descripteurs qui ne changent pas, ou l’utilisation de grands ensembles statiques de descripteurs et l’utilisation d’une combinaison de techniques pour différents descripteurs. Le matériel n’est pas conçu pour gérer ce type de flexibilité pour les autres types de descripteurs (RTV, DSV, IBV, VBV, SOV).

## <a name="suballocation"></a>Sous-allocation

Dans Direct3D 12, l’application dispose d’un contrôle de bas niveau sur la gestion de la mémoire. Dans les versions antérieures de Direct3D, y compris Direct3D 11, il y aurait une allocation par ressource. Dans Direct3D 12, l’application peut utiliser l’API pour allouer un grand bloc de mémoire, ce qui est plus important que n’importe quel objet unique. Une fois cette opération effectuée, l’application peut créer des descripteurs pour pointer vers les sections de ce bloc de mémoire volumineux. Ce processus consiste à décider de l’endroit où (les plus petits blocs à l’intérieur du grand bloc) sont connus sous le nom de sous- *allocation*. L’activation de l’application pour cela peut entraîner des gains d’utilisation efficace du calcul et de la mémoire. Par exemple, le changement de nom des ressources est rendu obsolète. Au lieu de cela, les applications peuvent utiliser des délimiteurs pour déterminer quand une ressource particulière est utilisée et lorsqu’elle ne l’est pas par des délimitations sur les exécutions de la liste de commandes où la liste de commandes requiert l’utilisation de cette ressource particulière.

## <a name="freeing-resources"></a>Libération des ressources

Avant de pouvoir libérer de la mémoire qui a été liée au pipeline, le GPU doit en avoir terminé.

L’attente du rendu des frames est probablement la manière la plus grossière de s’assurer que le GPU est terminé. À un niveau de granularité plus fin, vous pouvez utiliser à nouveau des délimiteurs : quand une commande est enregistrée dans une liste de commandes dont vous souhaitez effectuer le suivi, insérer une clôture immédiatement après celle-ci. Ensuite, vous pouvez effectuer diverses opérations de synchronisation avec la clôture. Vous soumettez un nouveau travail (listes de commandes) qui attend la fin d’une clôture spécifiée sur le GPU, ce qui indique que tout est terminé, ou vous pouvez demander qu’un événement de processeur soit déclenché lorsque la clôture est passée (que l’application peut attendre avec un thread en veille). Dans Direct3D 11, il s’agissait de `EnqueueSetEvent` ().

## <a name="related-topics"></a>Rubriques connexes

* [Liaison de ressource](resource-binding.md)
