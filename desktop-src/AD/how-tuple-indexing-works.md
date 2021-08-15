---
title: Fonctionnement de l’indexation des tuples
description: Les index de tuple sont utilisés pour optimiser les recherches qui ont 0 ou plusieurs chaînes de recherche médiane et 0 ou 1 chaînes de recherche finale. Elles peuvent également être utilisées pour optimiser les recherches d’une chaîne de recherche initiale si aucun index ordinaire n’est disponible sur cet attribut.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- indexation des tuples
- Recherche Active Directory Active Directory, optimisation
- Active Directory, l’optimisation de la recherche Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9d15bad8de15e4f559123d2d3cb3b6b9ec6446328e6ed4c4c52cf18355d634
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188032"
---
# <a name="how-tuple-indexing-works"></a>Fonctionnement de l’indexation des tuples

Les index de tuple sont utilisés pour optimiser les recherches qui ont 0 ou plusieurs [chaînes de recherche médiane](search-string-types.md) et 0 ou 1 chaînes de recherche finale. Elles peuvent également être utilisées pour optimiser les recherches d’une chaîne de recherche initiale si aucun index ordinaire n’est disponible sur cet attribut.

Vous pouvez activer l’indexation des tuples pour un attribut en définissant le bit 5, qui correspond à la valeur 32, dans l’attribut [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) . Cet attribut est défini dans l’objet de schéma qui représente l’attribut qui a besoin de l’index de Tuple. L’impact sur les performances de l’activation de l’indexation des tuples est que toute valeur de chaîne définie pour cet attribut sera développée en un grand nombre de fragments dans l’index de Tuple. Lorsqu’un attribut est développé, il consomme une plus grande quantité d’espace disque dans le fichier de l’arborescence d’informations d’annuaire et est également mis à jour plus lentement.

Les index de tuple sont conçus pour accélérer les recherches dans le formulaire `*string*` . L’accélération peut être considérable, car cette forme de recherche ne peut pas être optimisée d’une autre façon, et dans sa forme non optimisée, elle force le serveur Active Directory à parcourir chaque objet dans l’étendue de la recherche pour exécuter la requête. Par conséquent, une recherche de base recherche simplement un objet, qui utiliseraient moins de ressources, une recherche d’enfants immédiates rechercherait uniquement les enfants d’un objet (qui pourrait utiliser moins de ressources ou plus de ressources en fonction de la taille du conteneur), et une recherche de sous-arborescence parcourra l’ensemble de la sous-arborescence sous l’objet de base, ce qui nécessiterait généralement beaucoup de ressources et sera très lente en raison de la

Les index de tuple fonctionnent en scindant une chaîne en *tuples*. Par exemple, la chaîne « Active Directory » est décomposée dans les tuples suivants :

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> Le répertoire s’arrêtera à 32767 caractères lors du développement d’une chaîne pour l’indexation des tuples.

 

Un index de tuple contient une entrée pour chacun de ces tuples. Par conséquent, si un utilisateur recherche `*cto*` , le serveur de Active Directory recherche toutes les correspondances pour « directeur de la configuration » dans l’index et, dans ce cas, retrouve un pointeur vers l’enregistrement qui avait un attribut (Tuple indexé) avec la valeur « Directory ».

Si la chaîne `*cto*` de recherche intégrée (dans l’exemple précédent) est suffisamment spécifique, la recherche est très efficace, car elle réduit considérablement le nombre d’objets que le serveur Active Directory doit inspecter pour exécuter la requête.

 

 