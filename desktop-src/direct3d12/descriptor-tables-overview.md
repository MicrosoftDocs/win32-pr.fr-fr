---
title: Vue d’ensemble des tables de descripteurs
description: Chaque table de descripteur stocke des descripteurs d’un ou plusieurs types-SRVs, UAVe, CBVs et échantillonneurs. Une table de descripteurs n’est pas une allocation de mémoire ; Il s’agit simplement d’un décalage et d’une longueur dans un tas de descripteur.
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105145"
---
# <a name="descriptor-tables-overview"></a>Vue d’ensemble des tables de descripteurs

Chaque table de descripteur stocke des descripteurs d’un ou plusieurs types-SRVs, UAVe, CBVs et échantillonneurs. Une table de descripteurs n’est pas une allocation de mémoire ; Il s’agit simplement d’un décalage et d’une longueur dans un tas de descripteur.

-   [Référencement des tables de descripteurs](#referencing-descriptor-tables)
-   [Rubriques connexes](#related-topics)

## <a name="referencing-descriptor-tables"></a>Référencement des tables de descripteurs

Le pipeline Graphics, via la signature racine, permet d’accéder aux ressources en référençant les tables de descripteurs par index.

Une table de descripteurs est en fait simplement une sous-plage d’un tas de descripteur. Les tas de descripteurs représentent l’allocation de mémoire sous-jacente pour une collection de descripteurs. Étant donné que l’allocation de mémoire est une propriété de création d’un tas de descripteur, la définition d’une table de descripteurs à partir d’un est garantie d’être aussi coûteuse que l’identification d’une région dans le segment du matériel. Les tables de descripteurs n’ont pas besoin d’être créées ou détruites au niveau de l’API. elles sont simplement identifiées pour les pilotes en tant que décalage et taille hors d’un segment de mémoire à chaque fois qu’elles sont référencées.

Il est tout à fait possible pour une application de définir des tables de descripteurs très volumineuses quand ses nuanceurs souhaitent pouvoir effectuer une sélection à partir d’un vaste ensemble de descripteurs disponibles (souvent en référençant les textures) à la volée (peut-être pilotée par des données matérielles).

La signature racine fait référence à l’entrée de la table du descripteur avec une référence au tas, à l’emplacement de départ de la table (offset à partir du début du tas) et à la longueur (en entrées) de la table. L’image ci-dessous montre ces concepts : les pointeurs de table de descripteur de la signature racine et les descripteurs dans le tas de descripteur qui référencent la texture complète ou les données de mémoire tampon dans un tas de chargement.

![tables de descripteurs](images/descriptor-table.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tables de descripteurs](descriptor-tables.md)
</dt> </dl>

 

 




