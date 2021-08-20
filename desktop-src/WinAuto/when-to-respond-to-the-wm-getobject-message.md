---
title: Quand répondre au message de WM_GETOBJECT
description: Si une application prend en charge Microsoft Active Accessibility ou UI Automation pour un élément d’interface utilisateur, l’application ne doit pas répondre au message WM de la fonction \_ GETOBJECT avant que l’objet qui représente l’élément d’interface utilisateur soit entièrement initialisé, ou une fois que l’application a commencé à se fermer.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdb12edde21b7906fdda91d1bc5d46e453696214b93a331e26034527e163a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114614"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a>Quand répondre au message WM de \_ GETOBJECT

Si une application prend en charge Microsoft Active Accessibility ou UI Automation pour un élément d’interface utilisateur, l’application ne doit pas répondre au message WM de la fonction [**\_ GETOBJECT**](wm-getobject.md) avant que l’objet qui représente l’élément d’interface utilisateur soit entièrement initialisé, ou une fois que l’application a commencé à se fermer. Quand une application crée une nouvelle fenêtre, le système déclenche l' [**objet d’événement \_ \_ Create**](event-constants.md) WinEvent pour notifier les clients avant d’envoyer le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) à la procédure de fenêtre de l’application. Étant donné que de nombreuses applications utilisent la **\_ création de WM** pour démarrer le processus d’initialisation, toute implémentation d’accessibilité d’un élément d’interface utilisateur ne répond pas au message WM de la fonction [**\_ GETOBJECT**](wm-getobject.md) tant que l’application n’a pas terminé de traiter le message **WM \_ Create** .

 

 