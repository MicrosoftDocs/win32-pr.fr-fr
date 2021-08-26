---
description: Chaque thread a une priorité dynamique.
ms.assetid: bcc6cec7-2d85-4810-98d0-7d99486f4924
title: Augmentations de priorité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe04bcd1df27c2456a06d35d83b894243c9871b3799f04bdc3c3df190ef251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032019"
---
# <a name="priority-boosts"></a>Augmentations de priorité

Chaque thread a une *priorité dynamique*. Il s’agit de la priorité utilisée par le planificateur pour déterminer le thread à exécuter. Initialement, la priorité dynamique d’un thread est identique à sa priorité de base. Le système peut augmenter et diminuer la priorité dynamique pour s’assurer qu’il est réactif et qu’aucun thread n’est privé pour le temps processeur. Le système n’augmente pas la priorité des threads avec un niveau de priorité de base compris entre 16 et 31. Seuls les threads dont la priorité de base est comprise entre 0 et 15 reçoivent une priorité dynamique.

Le système améliore la priorité dynamique d’un thread pour améliorer sa réactivité comme suit.

-   Lorsqu’un processus qui utilise la \_ \_ classe de priorité normale est placé au premier plan, le planificateur augmente la classe de priorité du processus associé à la fenêtre de premier plan, afin qu’il soit supérieur ou égal à la classe de priorité des processus en arrière-plan. La classe Priority revient à sa valeur d’origine lorsque le processus n’est plus au premier plan.
-   Quand une fenêtre reçoit une entrée, par exemple des messages de minuteur, des messages de souris ou une entrée au clavier, le planificateur augmente la priorité du thread qui possède la fenêtre.
-   Lorsque les conditions d’attente d’un thread bloqué sont satisfaites, le planificateur augmente la priorité du thread. Par exemple, lorsqu’une opération d’attente associée aux e/s de disque ou de clavier est terminée, le thread reçoit une augmentation de priorité.

    Vous pouvez désactiver la fonctionnalité de renforcement de priorité en appelant la fonction [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost) ou [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost) . Pour déterminer si cette fonctionnalité a été désactivée, appelez la fonction [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost) ou [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost) .

Après avoir déclenché la priorité dynamique d’un thread, le planificateur réduit cette priorité d’un niveau chaque fois que le thread termine une tranche de temps, jusqu’à ce que le thread repasse à sa priorité de base. La priorité dynamique d’un thread n’est jamais inférieure à sa priorité de base.

 

 
