---
description: Les ressources de mémoire tampon de vertex ou de mémoire tampon managée ne peuvent pas être déclarées dynamiques en spécifiant D3DUSAGE \_ Dynamic au moment de la création.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Ressources de Application-Managed et stratégies d’allocation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516169"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a>Ressources de Application-Managed et stratégies d’allocation (Direct3D 9)

Les ressources de mémoire tampon de vertex ou de mémoire tampon managée ne peuvent pas être déclarées dynamiques en spécifiant D3DUSAGE \_ Dynamic au moment de la création. Cela nécessite une copie supplémentaire pour chaque modification apportée au contenu de la mémoire tampon de vertex. Les mémoires tampons de vertex dynamiques sont destinées au rendu de la géométrie dynamique et des données extraites à partir d’arborescences partitionnées d’espaces binaires ou d’autres structures de données de visibilité. Pour ce faire, vous devez préallouer les tampons du format souhaité. Ces ressources sont ensuite représentées pour prendre en charge les besoins d’application par un gestionnaire de ressources au sein de l’application. Le nombre total de mémoires tampons de vertex dynamiques est faible, car une application n’utilise simultanément que quelques Strides de vertex différents et parce qu’une autre mémoire tampon de vertex est requise uniquement pour les Strides uniques. Lorsque vous gérez des ressources dynamiques de cette manière, assurez-vous que les demandes à fréquence élevée sur les ressources ne diminuent pas de manière significative les performances de l’application.

Lorsque vous utilisez des ressources gérées par Direct3D et des applications, allouez des ressources gérées par l’application dans la \_ mémoire par défaut D3DPOOL avant de créer des ressources gérées par Direct3D. Cela permet au gestionnaire de mémoire de conserver un nombre précis de mémoire disponible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



