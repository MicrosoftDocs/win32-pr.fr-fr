---
title: Quand répondre au message de WM_GETOBJECT
description: Si une application prend en charge Microsoft Active Accessibility ou UI Automation pour un élément d’interface utilisateur, l’application ne doit pas répondre au message WM de la fonction \_ GETOBJECT avant que l’objet qui représente l’élément d’interface utilisateur soit entièrement initialisé, ou une fois que l’application a commencé à se fermer.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cfa8d6604a13e84ffa89bf1fcf93d5d13e66e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463562"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a><span data-ttu-id="bb906-103">Quand répondre au message WM de \_ GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="bb906-103">When to Respond to the WM\_GETOBJECT Message</span></span>

<span data-ttu-id="bb906-104">Si une application prend en charge Microsoft Active Accessibility ou UI Automation pour un élément d’interface utilisateur, l’application ne doit pas répondre au message WM de la fonction [**\_ GETOBJECT**](wm-getobject.md) avant que l’objet qui représente l’élément d’interface utilisateur soit entièrement initialisé, ou une fois que l’application a commencé à se fermer.</span><span class="sxs-lookup"><span data-stu-id="bb906-104">If an application supports Microsoft Active Accessibility or UI Automation for a UI element, the application must not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message before the object that represents the UI element is fully initialized, or after the application has begun to close.</span></span> <span data-ttu-id="bb906-105">Quand une application crée une nouvelle fenêtre, le système déclenche l' [**objet d’événement \_ \_ Create**](event-constants.md) WinEvent pour notifier les clients avant d’envoyer le message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) à la procédure de fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="bb906-105">When an application creates a new window, the system raises the [**EVENT\_OBJECT\_CREATE**](event-constants.md) WinEvent to notify clients before sending the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to the application's window procedure.</span></span> <span data-ttu-id="bb906-106">Étant donné que de nombreuses applications utilisent la **\_ création de WM** pour démarrer le processus d’initialisation, toute implémentation d’accessibilité d’un élément d’interface utilisateur ne répond pas au message WM de la fonction [**\_ GETOBJECT**](wm-getobject.md) tant que l’application n’a pas terminé de traiter le message **WM \_ Create** .</span><span class="sxs-lookup"><span data-stu-id="bb906-106">Because many applications use **WM\_CREATE** to start the initialization process, any accessibility implementation of a UI element does not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message until after the application has finished processing the **WM\_CREATE** message.</span></span>

 

 