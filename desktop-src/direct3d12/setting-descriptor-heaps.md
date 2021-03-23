---
title: Définition et remplissage des tas de descripteurs
description: Les types de tas de descripteur qui peuvent être définis sur une liste de commandes sont ceux qui contiennent des descripteurs pour lesquels les tables de descripteurs peuvent être utilisées (au plus une de chacune à la fois).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/03/2019
ms.locfileid: "104548525"
---
# <a name="setting-and-populating-descriptor-heaps"></a>Définition et remplissage des tas de descripteurs

Les types de tas de descripteur qui peuvent être définis sur une liste de commandes sont ceux qui contiennent des descripteurs pour lesquels les tables de descripteurs peuvent être utilisées (au plus une de chacune à la fois).

-   [Définition des tas de descripteurs](#setting-and-populating-descriptor-heaps)
-   [Remplissage des tas de descripteurs](#populating-descriptor-heaps)
-   [Rubriques connexes](#related-topics)

## <a name="setting-descriptor-heaps"></a>Définition des tas de descripteurs

Les types de tas de descripteurs pouvant être définis sur une liste de commandes sont :

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

Les tas définis dans la liste de commandes doivent également avoir été créés en tant que nuanceur visible. Il existe trois types de liste de commandes : DIRECT, BUNDLE et Compute.

Une fois qu’un tas de descripteur est défini sur une liste de commandes, les appels suivants qui définissent des tables de descripteurs font référence au tas de descripteur actuel. L’état de la table du descripteur n’est pas défini au début d’une liste de commandes et les tas de descripteurs sont modifiés dans une liste de commandes. Le fait de définir le même tas de descripteur de façon redondante n’entraîne pas la définition des paramètres de table de descripteur.

Dans un bundle, en revanche, les tas de descripteurs ne peuvent être définis qu’une seule fois (les appels redondants qui définissent deux fois le même tas ne génèrent pas d’erreur); dans le cas contraire, le comportement n’est pas défini. Les tas de descripteurs qui sont définis doivent correspondre à l’état quand une liste de commandes appelle le bundle. dans le cas contraire, le comportement n’est pas défini. Cela permet aux bottes d’hériter et de modifier les paramètres de table de descripteurs de la liste de commandes. Les regroupements qui ne modifient pas les tables de descripteurs (qui les héritent uniquement) n’ont pas besoin de définir un tas de descripteurs et héritent simplement de la liste de commandes appelante.

Lorsque les tas de descripteurs sont définis (à l’aide de [**ID3D12GraphicsCommandList :: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), tous les tas utilisés sont définis dans un appel unique (et tous les tas précédemment définis sont désactivés par l’appel). Au plus un segment de chaque type indiqué ci-dessus peut être défini dans l’appel.

## <a name="populating-descriptor-heaps"></a>Remplissage des tas de descripteurs

Une fois qu’une application a créé un tas de descripteur, elle peut ensuite utiliser des méthodes sur l’appareil pour générer des descripteurs directement dans le tas ou copier des descripteurs d’un emplacement à un autre.

Le contenu initial de la mémoire du tas de descripteur n’est pas défini. par conséquent, demander au GPU ou au pilote de faire référence à la mémoire non initialisée pour le rendu peut entraîner des résultats indéfinis, tels que la réinitialisation d’un appareil.

Si l’application configure un tas de descripteur pour qu’elle soit visible par le processeur, le processeur peut appeler des méthodes pour créer des descripteurs dans le tas et copier d’un emplacement à un autre (y compris entre les segments de mémoire) en mode thread immédiat et libre. Si le segment de mémoire a été configuré comme SHADER_VISIBLE, la lecture par l’UC n’est pas autorisée.



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tas de descripteurs](descriptor-heaps.md)
</dt> </dl>

 

 




