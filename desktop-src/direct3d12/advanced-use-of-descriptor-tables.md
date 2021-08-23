---
title: Utilisation avancée des tables de descripteurs
description: Les sections suivantes fournissent des informations sur l’utilisation avancée des tables de descripteurs.
ms.assetid: BB0CA29C-65CB-48B1-8351-EE13CC470B54
ms.date: 05/31/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: 044c02b87591f7ad53212ce37d7549ade68308a648092a260a67c97395959c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632589"
---
# <a name="advanced-use-of-descriptor-tables"></a>Utilisation avancée des tables de descripteurs

Les sections suivantes fournissent des informations sur l’utilisation avancée des tables de descripteurs.

-   [Modification des entrées de table de descripteurs entre les appels de rendu](#changing-descriptor-table-entries-between-rendering-calls)
-   [Indexation hors limites](#out-of-bounds-indexing)
-   [Dérivés du nuanceur et indexation divergente](#shader-derivatives-and-divergent-indexing)
-   [Rubriques connexes](#related-topics)

## <a name="changing-descriptor-table-entries-between-rendering-calls"></a>Modification des entrées de table de descripteurs entre les appels de rendu

Après que les commandes qui définissent les tables de descripteur ont été soumises à une file d’attente pour exécution, l’application ne doit pas modifier à partir du processeur les portions de tas de descripteur que le GPU peut référencer jusqu’à ce que l’application sache que le GPU a fini d’utiliser les références.

L’achèvement du travail peut être déterminé à l’aide d’une limite restreinte à l’aide de limites d’API pour le suivi de la progression du GPU, ou de mécanismes plus grossiistes comme l’attente de l’envoi d’un rendu à l’affichage, quelle que soit l’application. Si une application sait que seul un sous-ensemble de la région vers lequel pointe une table de descripteur est accessible (par exemple, en raison du contrôle de Flow dans le nuanceur), les autres descripteurs non référencés sont toujours libres d’être modifiés. Si une application doit basculer entre les différents tableaux de descripteurs entre les appels de rendu, il existe plusieurs approches possibles pour l’application :

-   Contrôle de version des tables de descripteurs : créez (ou réutilisez) une table de descripteur distincte pour chaque collection unique de descripteurs qui doit être référencée par une liste de commandes. Lors de la modification et de la réutilisation de zones déjà remplies sur des tas de descripteurs, les applications doivent d’abord s’assurer que le GPU a fini d’utiliser une partie d’un tas de descripteur qui sera recyclé.
-   Indexation dynamique : les applications peuvent organiser les objets qui varient d’un dessin à l’autre (ou même faire varier dans un dessin) dans une plage d’un tas de descripteurs, définir une table de descripteurs qui couvre toutes les tables et, à partir du nuanceur, utiliser l’indexation dynamique de la table pendant l’exécution du nuanceur pour sélectionner l’objet à utiliser.
-   Placer directement les descripteurs dans la signature racine. Seul un très petit nombre de descripteurs peut être géré de cette manière, car l’espace de signature racine est limité.

L’implication de l’utilisation du contrôle de version de table de descripteurs est que la mémoire de descripteur d’un tas de descripteur doit être gravée pour chaque ensemble unique de descripteurs référencé par le pipeline Graphics pour chaque liste de commandes pouvant être exécutée, mise en file d’attente d’exécution ou enregistrée à un moment donné.

D3D12 reste responsable de la gestion du contrôle de version de l’application pour les types d’objets gérés via les tas de descripteurs et les tables de descripteurs. L’un des avantages est que les applications peuvent choisir de réutiliser le contenu des tables de descripteurs autant que possible, plutôt que de toujours définir une nouvelle version de table de descripteur pour chaque soumission de liste de commandes. La signature racine est un espace que le pilote D3D12 version automatique.

La possibilité de lier plusieurs tables de descripteurs à la signature racine (et par conséquent au pipeline) à la fois permet aux applications de regrouper et de changer des ensembles de références de descripteur à différentes fréquences, si vous le souhaitez. Par exemple, une application peut utiliser un petit nombre (peut-être un seul) de tables de descripteurs statiques volumineuses qui changent rarement, ou dans quelles régions de la mémoire du tas du descripteur sous-jacent sont remplies en fonction des besoins, avec l’utilisation de l’indexation dynamique du nuanceur pour sélectionner les textures. En même temps, l’application peut conserver une autre classe de ressources où le jeu référencé par chaque appel de dessin est basculé de l’UC à l’aide de la technique de contrôle de version de table de descripteur.

## <a name="out-of-bounds-indexing"></a>Indexation hors limites

En dehors des limites, l’indexation d’une table de descripteur à partir du nuanceur entraîne un accès à la mémoire largement non défini, y compris la possibilité de lire une mémoire arbitraire dans le processus comme s’il s’agissait d’un descripteur d’état matériel et de vivre avec la conséquence de ce que le matériel utilise. Cela peut entraîner la réinitialisation de l’appareil, mais ne se bloquera pas Windows.

## <a name="shader-derivatives-and-divergent-indexing"></a>Dérivés du nuanceur et indexation divergente

Si les appels de nuanceur de pixels qui s’exécutent dans un tampon 2x2 (pour prendre en charge les calculs dérivés), choisissez différents index de texture à échantillonner à partir d’une table de descripteur. et si la configuration et la texture de l’échantillonneur sélectionné pour un pixel donné nécessitent un calcul de LOD à partir de dérivés de coordonnées de texture, le processus de calcul LOD et d’échantillonnage de texture est effectué par le matériel indépendamment pour chaque recherche de texture dans le tampon 2x2.  ce qui aura un impact sur les performances.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tables de descripteurs](descriptor-tables.md)
</dt> </dl>

 

 




