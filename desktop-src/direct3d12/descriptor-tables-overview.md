---
title: Vue d’ensemble des tables de descripteurs
description: Chaque table de descripteur stocke des descripteurs d’un ou plusieurs types-SRVs, UAVe, CBVs et échantillonneurs. Une table de descripteurs n’est pas une allocation de mémoire ; Il s’agit simplement d’un décalage et d’une longueur dans un tas de descripteur.
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3edae00c37a451aa0fb71355a1dea5860de4398f
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813109"
---
# <a name="descriptor-tables-overview"></a>Vue d’ensemble des tables de descripteurs

Chaque table de descripteur stocke des descripteurs d’un ou plusieurs types &mdash; SRVs, UAVe, CBVS et échantillonneurs. Une table de descripteurs n’est pas une allocation de mémoire ; Il s’agit simplement d’un décalage et d’une longueur dans un tas de descripteur.

## <a name="referencing-descriptor-tables"></a>Référencement des tables de descripteurs

Le pipeline Graphics, via la signature racine, permet d’accéder aux ressources en référençant les tables de descripteurs par index.

Une table de descripteurs est en fait simplement une sous-plage d’un tas de descripteur. Les tas de descripteurs représentent l’allocation de mémoire sous-jacente pour une collection de descripteurs. Étant donné que l’allocation de mémoire est une propriété de création d’un tas de descripteur, la définition d’une table de descripteurs à partir d’un est garantie d’être aussi coûteuse que l’identification d’une région dans le segment du matériel. Les tables de descripteurs n’ont pas besoin d’être créées ou détruites au niveau de l’API. elles sont simplement identifiées pour les pilotes en tant que décalage et taille hors d’un segment de mémoire à chaque fois qu’elles sont référencées.

Il est tout à fait possible pour une application de définir des tables de descripteurs très volumineuses quand ses nuanceurs souhaitent pouvoir effectuer une sélection à partir d’un vaste ensemble de descripteurs disponibles (souvent en référençant les textures) à la volée (peut-être pilotée par des données matérielles).

La signature racine fait référence à l’entrée de la table du descripteur avec une référence au tas, à l’emplacement de départ de la table (offset à partir du début du tas) et à la longueur (en entrées) de la table. L’image ci-dessous montre ces concepts : les pointeurs de table de descripteur de la signature racine et les descripteurs dans le tas de descripteur qui référencent la texture complète ou les données de mémoire tampon dans un segment de mémoire (dans le cas d’une texture, le tas par défaut).

![tables de descripteurs](images/descriptor-table.png)

## <a name="related-topics"></a>Rubriques connexes

* [Tables de descripteurs](descriptor-tables.md)
