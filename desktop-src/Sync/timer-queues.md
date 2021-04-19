---
description: La fonction CreateTimerQueue crée une file d’attente pour les minuteurs.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Files d’attente du minuteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518713"
---
# <a name="timer-queues"></a>Files d’attente du minuteur

La fonction [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) crée une file d’attente pour les minuteurs. Les minuteries de cette file d’attente, appelées *minuteries de file d’attente du minuteur*, sont des objets légers qui vous permettent de spécifier une fonction de rappel à appeler lorsque l’heure d’échéance spécifiée arrive. L’opération d’attente est effectuée par un thread dans le [pool de threads](../procthread/thread-pooling.md).

Pour ajouter un minuteur à la file d’attente, appelez la fonction [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) . Pour mettre à jour un minuteur de file d’attente de minuterie, appelez la fonction [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) . Vous pouvez spécifier une fonction de rappel à exécuter par un thread de travail à partir du pool de threads lorsque le minuteur expire.

Pour annuler un minuteur en attente, appelez la fonction [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) . Lorsque vous avez terminé avec la file d’attente des minuteries, appelez la fonction [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) pour supprimer la file d’attente du minuteur. Les minuteries en attente dans la file d’attente sont annulées et supprimées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des files d’attente du minuteur](using-timer-queues.md)
</dt> </dl>

 

 
