---
title: Copie de descripteurs
description: Les méthodes ID3D12Device CopyDescriptors et ID3D12Device CopyDescriptorsSimple de l’interface de l’appareil utilisent le processeur pour copier immédiatement les descripteurs.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404351"
---
# <a name="copying-descriptors"></a>Copie de descripteurs

Les méthodes [**ID3D12Device :: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) et [**ID3D12Device :: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) sur l’interface de l’appareil utilisent le processeur pour copier immédiatement les descripteurs. Ils peuvent être appelés thread libre, à condition que plusieurs threads sur le processeur ou le GPU n’effectuent pas d’écriture potentiellement conflictuelle.

## <a name="copying-descriptors-immediately-cpu-timeline"></a>Copie immédiate des descripteurs (chronologie de l’UC)

Le nombre de descripteurs de code source (à copier à partir de), spécifié sous la forme d’un ensemble de plages de descripteur, doit être égal au nombre de descripteurs de destination (à copier), spécifié sous la forme d’un ensemble distinct de plages de descripteurs. Dans le cas contraire, les plages source et de destination ne doivent pas être alignées. Par exemple, un ensemble de descripteurs éparpillés peut être copié vers une destination contiguë, vice versa, ou dans une combinaison.

Plusieurs tas de descripteurs peuvent être impliqués dans l’opération de copie, à la fois en tant que source et destination. L’utilisation de handles de descripteur en tant que paramètres signifie que les méthodes de copie ne s’intéressent pas aux tas figurant dans un descripteur donné. il s’agit uniquement de la mémoire.

Les types de tas de descripteur copiés à partir de et à doivent correspondre, donc les méthodes prennent un type de tas de descripteur unique comme entrée. Le pilote doit connaître le type de segment de mémoire de tous les descripteurs dans l’opération de copie donnée. il sait donc quelle taille de données est impliquée dans l’opération de copie. Le pilote peut également avoir besoin d’effectuer une copie personnalisée si un type de tas de descripteur donné le justifie, un détail d’implémentation. Notez que les handles de descripteur eux-mêmes n’identifient pas le type auquel ils pointent. par conséquent, un paramètre supplémentaire est requis pour l’opération de copie.

Une autre API pour [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) est fournie dans le cas simple de la copie d’une plage unique de descripteurs d’un emplacement à un autre – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).

Pour ces méthodes de copie du descripteur basé sur un appareil (chronologie), les descripteurs de source doivent provenir d’un tas de descripteur visible sans nuanceur. Les descripteurs de destination peuvent se trouver dans n’importe quel tas de descripteur visible par l’UC (nuanceur visible ou non).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Descripteurs](descriptors.md)
</dt> </dl>

 

 




