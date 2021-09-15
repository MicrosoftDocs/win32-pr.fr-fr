---
title: Tas du descripteur visible par le nuanceur
description: Les tas de descripteurs visibles du nuanceur, sont des tas de descripteurs qui peuvent être référencés par des nuanceurs par le biais de tables de descripteurs.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518829"
---
# <a name="shader-visible-descriptor-heaps"></a>Tas du descripteur visible par le nuanceur

Les tas de descripteurs visibles du nuanceur, sont des tas de descripteurs qui peuvent être référencés par des nuanceurs par le biais de tables de descripteurs.

-   [Vue d'ensemble](#overview)
-   [Exemple](#an-example)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Les tas de descripteurs qui peuvent être référencés par des nuanceurs par le biais de tables de descripteur sont de deux types : un type de segment de mémoire, D3D12 \_ SRV \_ UAV \_ CBV \_ descripteur \_ , peut contenir des vues de ressources de nuanceur, des vues d’accès non ordonnées et des vues de mémoire tampon constantes, toutes intermélangées. Tout emplacement donné dans le tas peut être l’un des types de descripteurs listés. Un autre type de tas, D3D12 \_ descripteur \_ \_ type Heap \_ Sample, stocke uniquement des échantillonneurs, reflétant le fait que pour la majorité du matériel, les échantillonneurs sont gérés séparément de SRVs, UAVs, CBVS.

Les tas de descripteurs de ces types peuvent être demandés comme étant visibles par le nuanceur ou non lors de la création du segment de mémoire (ce dernier, non Shader visible, peut être utile pour les descripteurs intermédiaires sur le processeur). Lorsqu’un nuanceur est visible, chacun des types de tas ci-dessus peut avoir une limite de taille matérielle pour toute allocation de tas de descripteur individuelle.

Les applications peuvent créer un nombre quelconque de tas de descripteurs, et les tas de descripteurs non visibles par le nuanceur ne sont pas limités en taille. Si le tas du descripteur visible par le nuanceur qui est créé par l’application est inférieur à la limite de taille matérielle, le pilote peut choisir de sous-allouer le tas du descripteur à partir d’un tas de descripteur sous-jacent plus grand, afin que plusieurs tas de descripteurs d’API tiennent dans un tas de descripteur matériel. Cela peut être dû au fait que, pour un matériel donné, le basculement entre les tas de descripteurs de matériel pendant l’exécution nécessite une attente GPU inactive (pour s’assurer que les références GPU au tas du descripteur précédent sont terminées). Si tous les tas de descripteurs créés par une application s’intègrent aux capacités maximales du tas matériel applicables, aucune attente de ce type ne se produit lors du changement de tas du descripteur d’API pendant le rendu. Toutefois, les applications doivent autoriser le basculement du tas de descripteur actuel vers une attente d’inactivité.

Pour éviter d’être affecté par cette attente possible d’inactivité sur le commutateur du tas du descripteur, les applications peuvent tirer parti des arrêts dans le rendu, ce qui entraînerait l’inactivité du GPU pour d’autres raisons.

Le mécanisme et la sémantique permettant d’identifier les tas de descripteurs pour les nuanceurs lors de la liste de commandes/l’enregistrement groupé sont décrits dans la référence de l’API.

## <a name="an-example"></a>Exemple

L’image ci-dessous montre deux tas de descripteurs référençant deux textures 2D distinctes stockées dans deux emplacements d’un grand tas par défaut. Le tas de descripteur visible par le nuanceur est accessible par le pipeline graphique (y compris les nuanceurs) et la texture 2D est donc disponible pour le pipeline.

![tas de descripteurs visibles et non visibles](images/descriptor-heaps.png)

> [!Note]  
> Il existe souvent une limite sur le matériel GPU de la quantité de mémoire locale GPU accessible en écriture par l’UC (appelée mémoire combinée en écriture) pour les tas de descripteurs. En général, cette limite est d’environ 96 Mo pour tous les processus. Un segment de descripteur de membre 1 million, avec descripteurs 32byte, utilise 32 Mo, par exemple. Le pilote revient à la mémoire système si nécessaire, bien qu’il soit conseillé de ne pas créer un grand nombre de tas de descripteurs volumineux.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tas de descripteurs](descriptor-heaps.md)
</dt> </dl>

 

 




