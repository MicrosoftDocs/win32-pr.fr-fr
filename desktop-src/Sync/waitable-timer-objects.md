---
description: Un objet de minuteur qui peut être attendu est un objet de synchronisation dont l’État est défini sur signalé lorsque l’heure d’échéance spécifiée arrive.
ms.assetid: 5d39ada0-ea31-40d7-b075-aeb657ee508c
title: Objets Timer waitables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9597617705fcd78bb71f63e33a475e3bca78e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095794"
---
# <a name="waitable-timer-objects"></a>Objets Timer waitables

Un *objet de minuteur* qui peut être attendu est un objet de synchronisation dont l’État est défini sur signalé lorsque l’heure d’échéance spécifiée arrive. Il existe deux types de minuteurs qui peuvent être créés : Manuel-réinitialisation et synchronisation. Un minuteur de l’un des deux types peut également être un minuteur périodique.



| Object                | Description                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| réinitialisation manuelle du minuteur    | Minuterie dont l’état reste signalé jusqu’à ce que [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) soit appelé pour établir une nouvelle heure d’échéance.                                                                          |
| minuteur de synchronisation | Minuterie dont l’état reste signalé jusqu’à ce qu’un thread termine une opération d’attente sur l’objet de minuteur.                                                                                                     |
| minuteur périodique        | Minuterie réactivée à chaque expiration de la période spécifiée, jusqu’à ce que la minuterie soit réinitialisée ou annulée. Un minuteur périodique est soit un minuteur de réinitialisation manuelle périodique, soit un minuteur de synchronisation périodique. |



 

> [!Note]  
> Lorsqu’un minuteur est signalé, le processeur doit s’exécuter pour traiter les instructions associées. Les minuteries périodiques de fréquence élevée maintiennent le processeur continuellement occupé, ce qui empêche le système de rester dans un [État d’alimentation](../power/system-power-states.md) inférieur pendant une durée significative. Cela peut avoir un impact négatif sur la durée de vie de la batterie de l’ordinateur portable et les scénarios qui dépendent de la gestion de l’alimentation, tels que les grands centres de centres. Pour une plus grande efficacité énergétique, envisagez d’utiliser des notifications basées sur les événements plutôt que des notifications temporelles dans votre application. Si un minuteur est nécessaire, utilisez une minuterie signalée une seule fois plutôt qu’une minuterie périodique, ou définissez l’intervalle sur une valeur supérieure à une seconde.

 

Un thread utilise la fonction [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) ou [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) pour créer un objet Timer. Le thread de création spécifie si la minuterie est un minuteur de réinitialisation manuelle ou un minuteur de synchronisation. Le thread de création peut spécifier un nom pour l’objet de minuteur. Les threads d’autres processus peuvent ouvrir un handle vers une minuterie existante en spécifiant son nom dans un appel à la fonction [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) . Tout thread avec un handle d’objet Timer peut utiliser l’une des [fonctions Wait](wait-functions.md) pour attendre que l’état du minuteur soit défini comme signalé.

-   Le thread appelle la fonction [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) pour activer la minuterie. Notez l’utilisation des paramètres suivants pour **SetWaitableTimer**:
-   Utilisez le paramètre *lpDueTime* pour spécifier l’heure à laquelle la minuterie doit être définie sur l’état signalé. Lorsqu’un minuteur de réinitialisation manuelle est défini sur l’état signalé, il reste dans cet État jusqu’à ce que [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) établisse une nouvelle heure d’échéance. Quand un minuteur de synchronisation est défini sur l’état signalé, il reste dans cet État jusqu’à ce qu’un thread termine une opération d’attente sur l’objet de minuteur.
-   Utilisez le paramètre *lPeriod* de la fonction [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) pour spécifier la période du minuteur. Si la période n’est pas égale à zéro, la minuterie est un minuteur périodique. elle est réactivée à chaque expiration de la période, jusqu’à ce que la minuterie soit réinitialisée ou annulée. Si la période est égale à zéro, le minuteur n’est pas un minuteur périodique ; elle est signalée une seule fois, puis désactivée.

Un thread peut utiliser la fonction [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) pour définir le minuteur sur l’état inactif. Pour réinitialiser la minuterie, appelez [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Lorsque vous avez terminé avec l’objet de minuteur, appelez [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) pour fermer le handle de l’objet de minuteur.

Le comportement d’un minuteur peut être résumé comme suit :

-   Lorsqu’un minuteur est défini, il est annulé s’il était déjà actif, l’état du minuteur n’est pas signalé et le minuteur est placé dans la file d’attente du minuteur du noyau.
-   Lorsqu’un minuteur expire, la minuterie est définie sur l’état signalé. Si la minuterie a une routine de saisie semi-automatique, elle est mise en file d’attente vers le thread qui a défini la minuterie. La routine de saisie semi-automatique reste dans la file d’attente d' [appels de procédure asynchrone](asynchronous-procedure-calls.md) (APC) du thread jusqu’à ce que le thread entre dans un état d’attente averti. À ce moment-là, l’APC est distribué et la routine de saisie semi-automatique est appelée. Si la minuterie est périodique, elle est replacée dans la file d’attente du minuteur du noyau.
-   Lorsqu’une minuterie est annulée, elle est supprimée de la file d’attente du minuteur du noyau si elle était en attente. Si le minuteur a expiré et qu’un APC est toujours mis en file d’attente sur le thread qui a défini la minuterie, l’APC est supprimé de la file d’attente APC du thread. L’état signalé de la minuterie n’est pas affecté.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appels de procédure asynchrone](asynchronous-procedure-calls.md)
</dt> <dt>

[Utilisation d’objets Timer Waitables](using-waitable-timer-objects.md)
</dt> </dl>

 

 
