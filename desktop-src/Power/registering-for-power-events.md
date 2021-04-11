---
description: Les applications peuvent mieux adapter leur comportement à l’état d’alimentation actuel de l’ordinateur en s’inscrivant pour les événements d’alimentation.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Inscription pour les événements d’alimentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da084592414d1c58ab4ab43dd2b5c35f028552b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202861"
---
# <a name="registering-for-power-events"></a><span data-ttu-id="cde09-103">Inscription pour les événements d’alimentation</span><span class="sxs-lookup"><span data-stu-id="cde09-103">Registering for Power Events</span></span>

<span data-ttu-id="cde09-104">Les applications peuvent mieux adapter leur comportement à l’état d’alimentation actuel de l’ordinateur en s’inscrivant pour les événements d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="cde09-104">Applications can better adapt their behavior to the current power state of the computer by registering for power events.</span></span> <span data-ttu-id="cde09-105">Une application doit s’inscrire à chaque événement de changement d’alimentation qui peut avoir un impact sur son comportement.</span><span class="sxs-lookup"><span data-stu-id="cde09-105">An application should register for each power change event that might impact its behavior.</span></span>

<span data-ttu-id="cde09-106">Une application ou un service utilise la fonction [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) pour s’inscrire aux notifications.</span><span class="sxs-lookup"><span data-stu-id="cde09-106">An application or service uses the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function to register for notifications.</span></span> <span data-ttu-id="cde09-107">Lorsque le paramètre d’alimentation correspondant change, le système envoie des notifications comme suit :</span><span class="sxs-lookup"><span data-stu-id="cde09-107">When the corresponding power setting changes, the system sends notifications as follows:</span></span>

-   <span data-ttu-id="cde09-108">Une application reçoit un [**message WM \_ POWERBROADCAST**](wm-powerbroadcast.md) avec un *wParam* de [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) et un *lParam* qui pointe vers une structure de [**\_ paramètre POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="cde09-108">An application receives a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message with a *wParam* of [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) and an *lParam* that points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>
-   <span data-ttu-id="cde09-109">Un service reçoit un appel à la fonction de rappel [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) qu’il a inscrit en appelant la fonction [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) .</span><span class="sxs-lookup"><span data-stu-id="cde09-109">A service receives a call to the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) callback function it registered by calling the [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function.</span></span> <span data-ttu-id="cde09-110">Le paramètre *lpEventData* envoyé à la fonction de rappel *HandlerEx* pointe vers une structure de [**\_ paramètre POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="cde09-110">The *lpEventData* parameter sent to the *HandlerEx* callback function points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

<span data-ttu-id="cde09-111">Dans la structure de [**\_ paramètre POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) , le membre **PowerSetting** contient le GUID qui identifie la notification et le membre de **données** contient la nouvelle valeur du paramètre d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="cde09-111">In the [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure, the **PowerSetting** member contains the GUID that identifies the notification and the **Data** member contains the new value of the power setting.</span></span>

<span data-ttu-id="cde09-112">Pour obtenir la liste des GUID des paramètres d’alimentation pour les notifications les plus utiles pour les applications, consultez [**GUID des paramètres d’alimentation**](power-setting-guids.md).</span><span class="sxs-lookup"><span data-stu-id="cde09-112">For a list of power setting GUIDs for notifications that are most useful to applications, see [**Power Setting GUIDs**](power-setting-guids.md).</span></span>

 

 
