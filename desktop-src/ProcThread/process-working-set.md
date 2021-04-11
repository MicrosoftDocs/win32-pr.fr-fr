---
description: La plage de travail d’un programme est une collection de ces pages dans son espace d’adressage virtuel qui ont été récemment référencées.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Traiter la plage de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900b5d8a19c756a9087a9b2c006259857691dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202849"
---
# <a name="process-working-set"></a>Traiter la plage de travail

La *plage de travail* d’un programme est une collection de ces pages dans son espace d’adressage virtuel qui ont été récemment référencées. Il comprend des données partagées et privées. Les données partagées incluent des pages qui contiennent toutes les instructions exécutées par votre application, y compris celles qui figurent dans vos dll et les DLL système. À mesure que la taille de la plage de travail augmente, la demande de mémoire augmente.

Un processus est associé à une taille de jeu de travail minimale et à une taille de jeu de travail maximale. Chaque fois que vous appelez [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), il réserve la taille minimale du jeu de travail pour le processus. Le gestionnaire de mémoire virtuelle tente de conserver suffisamment de mémoire pour la plage de travail minimale résidant lorsque le processus est actif, mais ne conserve pas plus de la taille maximale.

Pour obtenir les tailles minimale et maximale requises de la plage de travail de votre application, appelez la fonction [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) .

Le système définit les tailles de la plage de travail par défaut. Vous pouvez également modifier les tailles de la plage de travail à l’aide de la fonction [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) . La définition de ces valeurs n’est pas une garantie que la mémoire sera réservée ou résidera. Soyez prudent lorsque vous demandez une taille de jeu de travail minimale ou maximale, car cela peut nuire aux performances du système.

Pour obtenir la taille actuelle ou maximale de la plage de travail de votre processus, utilisez la fonction [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations sur les performances de la mémoire](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))
</dt> <dt>

[Plage de travail](../memory/working-set.md)
</dt> </dl>

 

 
