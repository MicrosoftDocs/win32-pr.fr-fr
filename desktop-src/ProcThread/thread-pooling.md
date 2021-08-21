---
description: Il existe de nombreuses applications qui créent des threads qui consacrent beaucoup de temps à l’état de veille en attendant qu’un événement se produise.
ms.assetid: a5e52080-35d4-47f5-9050-90889e3bf2f8
title: Regroupement des threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c581e416952e6bac14dbf12a8f87202925a5254879b7e220c7cb2d780699f9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081279"
---
# <a name="thread-pooling"></a>Regroupement des threads

Il existe de nombreuses applications qui créent des threads qui consacrent beaucoup de temps à l’état de veille en attendant qu’un événement se produise. D’autres threads peuvent entrer dans un état de veille uniquement pour être mis à jour régulièrement pour demander des informations sur l’état des modifications ou des mises à jour. Le *regroupement de threads* vous permet d’utiliser les threads plus efficacement en fournissant à votre application un pool de threads de travail qui sont gérés par le système. Au moins un thread surveille l’état de toutes les opérations d’attente en attente dans le pool de threads. Quand une opération d’attente est terminée, un thread de travail du pool de threads exécute la fonction de rappel correspondante.

Cette rubrique décrit l’API du pool de threads d’origine. l’API de pool de threads introduite dans Windows Vista est plus simple, plus fiable, offre de meilleures performances et offre davantage de flexibilité aux développeurs. Pour plus d’informations sur l’API de pool de threads actuelle, consultez [pools de threads](thread-pools.md).

Vous pouvez également mettre en file d’attente des éléments de travail qui ne sont pas associés à une opération d’attente dans le pool de threads. Pour demander qu’un élément de travail soit géré par un thread dans le pool de threads, appelez la fonction [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) . Cette fonction accepte un paramètre de la fonction qui sera appelée par le thread sélectionné dans le pool de threads. Il n’existe aucun moyen d’annuler un élément de travail après qu’il a été mis en file d’attente.

Les [minuteries de file d’attente](../sync/timer-queues.md) et les [opérations d’attente inscrites](../sync/wait-functions.md) utilisent également le pool de threads. Leurs fonctions de rappel sont mises en file d’attente dans le pool de threads. Vous pouvez également utiliser la fonction [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback) pour poster des opérations d’e/s asynchrones. À la fin de l’e/s, le rappel est exécuté par un thread de pool de threads.

Le pool de threads est créé la première fois que vous appelez [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) ou [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback), ou lorsqu’un minuteur de file d’attente de minuterie ou une opération d’attente inscrite met en file d’attente une fonction de rappel. Par défaut, le nombre de threads qui peuvent être créés dans le pool de threads est d’environ 500. Chaque thread utilise la taille de pile par défaut et s’exécute à la priorité par défaut.

Il existe deux types de threads de travail dans le pool de threads : e/s et non-e/s. Un *thread de travail d’e/s* est un thread qui attend un état d’attente averti. Les éléments de travail sont mis en file d’attente pour les threads de travail d’e/s en tant qu’appels de procédure asynchrone (APC). Vous devez mettre un élément de travail en file d’attente sur un thread de travail d’e/s s’il doit être exécuté dans un thread qui attend un état d’alerte.

Un *thread de travail non-e/s* attend sur les ports de terminaison d’e/s. L’utilisation de threads de travail non-e/s est plus efficace que l’utilisation de threads de travail d’e/s. Par conséquent, vous devez utiliser des threads de travail non-e/s chaque fois que cela est possible. Les threads de travail d’e/s et non-e/s ne se ferment pas s’il existe des demandes d’e/s asynchrones en attente. Les deux types de threads peuvent être utilisés par les éléments de travail qui initient des demandes d’achèvement d’e/s asynchrones. Toutefois, évitez de publier des demandes de fin d’exécution d’e/s asynchrones dans des threads de travail non-e/s si leur exécution peut prendre beaucoup de temps.

Pour utiliser le regroupement de threads, les éléments de travail et toutes les fonctions qu’ils appellent doivent être sécurisés par pool de threads. Une fonction sécurisée ne suppose pas que le thread qui l’exécute est un thread dédié ou persistant. En général, vous devez éviter d’utiliser le [stockage local des threads](thread-local-storage.md) ou d’effectuer un appel asynchrone qui requiert un thread persistant, tel que la fonction [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) . Toutefois, ces fonctions peuvent être appelées sur un thread dédié (créé par l’application) ou mises en file d’attente sur un thread de travail persistant (à l’aide de [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) avec l' \_ option WT EXECUTEINPERSISTENTTHREAD).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[E/s alertables](../fileio/alertable-i-o.md)
</dt> <dt>

[Appels de procédure asynchrone](../sync/asynchronous-procedure-calls.md)
</dt> <dt>

[Ports de terminaison d’e/s](../fileio/i-o-completion-ports.md)
</dt> <dt>

[Pools de threads](thread-pools.md)
</dt> </dl>

 

 
