---
title: Limites de signature racine
description: La signature racine est un grand patrimoine et il existe des limites et des coûts stricts à prendre en compte.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104136"
---
# <a name="root-signature-limits"></a>Limites de signature racine

La signature racine est un grand patrimoine et il existe des limites et des coûts stricts à prendre en compte.

-   [Limites et coûts de la mémoire](#memory-limits-and-costs)
-   [Coûts de performances](#performance-costs)
-   [Échantillonneurs statiques](#static-samplers)
-   [Rubriques connexes](#related-topics)

## <a name="memory-limits-and-costs"></a>Limites et coûts de la mémoire

La taille maximale d’une signature racine est de 64 DWORDs.

Cette taille maximale est choisie pour empêcher un abus de la signature racine comme un moyen de stocker des données en bloc. Chaque entrée dans la signature racine a un coût pour cette limite DWORD de 64 :

-   Tables de descripteur coût 1 DWORD chacune.
-   Les constantes racine cost 1 DWORD sont chacune, car il s’agit de valeurs 32 bits.
-   Les descripteurs racine (adresses virtuelles du GPU 64 bits) coûtent 2 DWORD.

Les échantillonneurs statiques n’ont aucun coût dans la taille de la signature racine.

## <a name="performance-costs"></a>Coûts de performances

Le coût des performances (en termes de niveaux d’indirection) est égal à zéro pour une constante racine, 1 à un descripteur racine et 2 pour une table de descripteurs. Si une signature racine est volumineuse et déborde de la mémoire la plus rapide dans une mémoire légèrement plus lente (qui peut se produire sur du matériel), ajoutez 1 au coût des performances pour les éléments de dépassement à la fin de la signature racine.

Un dépassement de capacité peut se produire sur du matériel qui peut avoir, par exemple, une taille fixe de 16 DWORDs pour l’espace d’argument racine. Cette limite peut être plus réduite d’une unité si l’assembleur d’entrée est utilisé. Dans ce cas, la mémoire est légèrement plus lente si la signature racine est trop grande pour la mémoire native de 15 ou 16 DWORD. Dans un autre matériel, il n’existe pas de mémoire d’arguments racine Native fixe (la situation de dépassement de capacité ne se produit donc jamais).

Pour tout le matériel, si un argument racine change, le pilote doit conserver une version de tous les arguments racine (contrairement à d’autres stockages, tels que les tas de descripteurs et les ressources de mémoire tampon, qui ne sont pas gérées par le pilote). Dans le matériel qu’une situation de dépassement de capacité se produit, seule la version native ou de dépassement de capacité doit être gérée, selon l’endroit où la modification s’est produite. La quantité de contrôle de version doit évidemment être conservée au minimum nécessaire.

En règle générale, tenez compte des recommandations suivantes :

-   Utilisez une petite signature racine en fonction des besoins, bien que l’équilibre avec la flexibilité d’une signature racine plus grande.
-   Réorganisez les paramètres dans une grande signature racine afin que les paramètres les plus susceptibles d’être modifiés souvent, ou si une faible latence d’accès pour un paramètre donné soit importante, se produisent en premier.
-   Si vous le faites, utilisez des constantes racine ou des vues de mémoire tampon constantes racine pour placer des vues de mémoire tampon constantes dans un tas de descripteur.

## <a name="static-samplers"></a>Échantillonneurs statiques

Les échantillonneurs statiques (exemples dans lesquels l’État est entièrement défini et immuable) font partie des signatures racines, mais ne sont pas pris en compte dans la limite DWORD de 64. Si un échantillonneur peut être défini comme static, il n’est pas nécessaire que l’échantillonneur fasse partie d’un tas de descripteur.

Il n’y a aucun coût de performance pour l’utilisation d’échantillonneurs statiques, et une signature racine peut contenir une combinaison d’échantillonneurs statiques (stockés dans la signature racine ou dans un espace réservé sur un matériel) et d’échantillonneurs dynamiques (stockés dans un tas de descripteur d’échantillonneur). Les échantillonneurs d’un tas de descripteur peuvent être attribués et indexés dynamiquement, ce qui ne peut pas être le signe d’échantillonneurs statiques.

Les échantillonneurs statiques peuvent être écrits dans le cadre de la signature racine dans les nuanceurs HLSL (reportez-vous à [spécification des signatures racines en HLSL](specifying-root-signatures-in-hlsl.md)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Signatures racines](root-signatures.md)
</dt> </dl>

 

 




