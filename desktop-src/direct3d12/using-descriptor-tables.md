---
title: Utilisation de tables de descripteurs
description: Les tables de descripteurs, chacune identifiant une plage dans un tas de descripteur, sont liées aux emplacements définis par la signature racine actuelle dans une liste de commandes.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104614"
---
# <a name="using-descriptor-tables"></a>Utilisation de tables de descripteurs

Les tables de descripteurs, chacune identifiant une plage dans un tas de descripteur, sont liées aux emplacements définis par la signature racine actuelle dans une liste de commandes.

-   [Indexation des tables de descripteurs](#indexing-descriptor-tables)
-   [Rubriques connexes](#related-topics)

Les nuanceurs peuvent localiser les ressources référencées par les descripteurs qui composent la table du descripteur. D’autres liaisons de ressources-tampons d’index, tampons de vertex, mémoires tampons de sortie de flux, cibles de rendu et stencil de profondeur sont effectués directement sur une liste de commandes plutôt que via des descripteurs. Pour récapituler :

Les références de ressources suivantes peuvent partager les mêmes table de descripteur et tas :

-   Affichages des ressources de nuanceur
-   Vues d’accès non ordonnées
-   Vues de mémoire tampon constantes

Les références de ressources suivantes doivent être dans leur propre tas de descripteur :

-   Échantillonneurs

Les ressources suivantes ne sont pas placées dans les tables de descripteurs ou les segments de mémoire, mais sont directement liées à l’aide de listes de commandes :

-   Mémoires tampons d’index
-   Mémoires tampons de vertex
-   Mémoires tampons de sortie de flux
-   Cibles de rendu
-   Vues du stencil de profondeur

## <a name="indexing-descriptor-tables"></a>Indexation des tables de descripteurs

Les nuanceurs ne peuvent pas indexer dynamiquement entre les limites des tables de descripteurs à partir d’un site d’appel donné dans le nuanceur. Toutefois, la sélection d’un descripteur au sein d’une table de descripteur peut être indexée dynamiquement dans le code du nuanceur dans des plages du même type de descripteur (telles que l’indexation dans une région contiguë de SRVs).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tables de descripteurs](descriptor-tables.md)
</dt> </dl>

 

 




