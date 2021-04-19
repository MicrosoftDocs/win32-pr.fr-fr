---
description: La fragmentation du tas est un État dans lequel la mémoire disponible est décomposée en blocs petits et non contigus.
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: Tas de fragmentation faible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad14a97fa6d95b663f63b21f0982332ba0de01e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544839"
---
# <a name="low-fragmentation-heap"></a>Tas de fragmentation faible

\[Les informations contenues dans cette rubrique s’appliquent à Windows Server 2003 et Windows XP. À compter de Windows Vista, le système utilise le tas de faible fragmentation (LFH) en fonction des besoins pour traiter les demandes d’allocation de mémoire. Les applications n’ont pas besoin d’activer le LFH pour leurs tas.\]

La fragmentation du tas est un État dans lequel la mémoire disponible est décomposée en blocs petits et non contigus. Lorsqu’un segment de mémoire est fragmenté, l’allocation de mémoire peut échouer même lorsque la mémoire disponible totale dans le tas est suffisante pour satisfaire une demande, car aucun bloc de mémoire unique n’est suffisamment grand. Le segment de fragmentation faible (LFH) permet de réduire la fragmentation du tas.

LFH n’est pas un segment de mémoire séparé. Au lieu de cela, il s’agit d’une stratégie que les applications peuvent activer pour leurs tas. Lorsque le LFH est activé, le système alloue de la mémoire dans certaines tailles prédéterminées. Quand une application demande une allocation de mémoire à partir d’un segment de mémoire sur lequel le LFH est activé, le système alloue le plus petit bloc de mémoire suffisamment grand pour contenir la taille demandée. Le système n’utilise pas le LFH pour les allocations supérieures à 16 Ko, que le LFH soit activé ou non.

Une application doit activer LFH uniquement pour le tas par défaut du processus appelant ou pour les [tas privés](heap-functions.md) créés par l’application. Pour activer LFH pour un segment de mémoire, utilisez la fonction [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) pour obtenir un handle vers le tas par défaut du processus appelant, ou utilisez le handle vers un tas privé créé par la fonction [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) . Appelez ensuite la fonction [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) avec le descripteur.

Le LFH ne peut pas être activé pour les tas créés avec un segment de mémoire **\_ non \_ Serialize** ou pour les tas créés avec une taille fixe. Le LFH ne peut pas non plus être activé si vous utilisez les outils de débogage du tas dans [outils de débogage pour Windows](/windows-hardware/drivers/debugger/) ou [Microsoft Application Verifier](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en).

Une fois que le LFH a été activé pour un segment de mémoire, il ne peut pas être désactivé.

Les applications qui tirent le meilleur parti des LFH sont des applications multithread qui allouent fréquemment de la mémoire et utilisent une variété de tailles d’allocation inférieures à 16 Ko. Toutefois, toutes les applications ne bénéficient pas de LFH. Pour évaluer les effets de l’activation des LFH dans votre application, utilisez les données de profilage des performances.

 

 
