---
description: Le système diffuse un message à toutes les applications et pilotes installables à chaque fois qu’un événement de gestion de l’alimentation se produit.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: Messages WM_POWERBROADCAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518678"
---
# <a name="wm_powerbroadcast-messages"></a><span data-ttu-id="9a406-103">\_Messages WM POWERBROADCAST</span><span class="sxs-lookup"><span data-stu-id="9a406-103">WM\_POWERBROADCAST Messages</span></span>

<span data-ttu-id="9a406-104">Le système diffuse un message à toutes les applications et pilotes installables à chaque fois qu’un événement de gestion de l’alimentation se produit.</span><span class="sxs-lookup"><span data-stu-id="9a406-104">The system broadcasts a message to all applications and installable drivers whenever a power management event occurs.</span></span> <span data-ttu-id="9a406-105">Le système diffuse ces événements par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) , en définissant le paramètre *wParam* sur l’événement de gestion de l’alimentation approprié.</span><span class="sxs-lookup"><span data-stu-id="9a406-105">The system broadcasts these events through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message, setting the *wParam* parameter to the appropriate power management event.</span></span> <span data-ttu-id="9a406-106">Par exemple, l’événement [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) indique une modification de l’état de l’alimentation du système.</span><span class="sxs-lookup"><span data-stu-id="9a406-106">For example, the [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) event indicates a system power status change.</span></span> <span data-ttu-id="9a406-107">Vous devez vous assurer que votre application répond correctement au message **WM \_ POWERBROADCAST** .</span><span class="sxs-lookup"><span data-stu-id="9a406-107">You must ensure that your application responds properly to the **WM\_POWERBROADCAST** message.</span></span>

<span data-ttu-id="9a406-108">Le système diffuse un événement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) immédiatement avant la suspension de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9a406-108">The system broadcasts a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event immediately before suspending operation.</span></span> <span data-ttu-id="9a406-109">Cela donne aux applications et aux pilotes une dernière chance de se préparer pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="9a406-109">This gives applications and drivers one last chance to prepare for the event.</span></span> <span data-ttu-id="9a406-110">Dans de nombreux cas, le système diffuse ces messages sans demander l’autorisation de le faire.</span><span class="sxs-lookup"><span data-stu-id="9a406-110">In many cases, the system broadcasts these messages without requesting permission to do so.</span></span> <span data-ttu-id="9a406-111">Cela se produit, par exemple, si une application force la suspension avec la fonction [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .</span><span class="sxs-lookup"><span data-stu-id="9a406-111">This happens, for example, if an application forces suspension with the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

<span data-ttu-id="9a406-112">Le système diffuse l’événement [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) ou [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) lors de la restauration de l’opération système.</span><span class="sxs-lookup"><span data-stu-id="9a406-112">The system broadcasts the [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) or [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event when system operation has been restored.</span></span> <span data-ttu-id="9a406-113">Si une application a reçu un événement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) avant la suspension de l’ordinateur, elle recevra l' \_ événement PBT APMRESUMESUSPEND.</span><span class="sxs-lookup"><span data-stu-id="9a406-113">If an application received a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended, it will receive the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="9a406-114">Dans le cas contraire, il recevra l' \_ événement PBT APMRESUMECRITICAL.</span><span class="sxs-lookup"><span data-stu-id="9a406-114">Otherwise, it will receive the PBT\_APMRESUMECRITICAL event.</span></span>

<span data-ttu-id="9a406-115">Le système envoie un événement [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) aux applications qui sont inscrites pour l’événement spécifique à l’aide de [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span><span class="sxs-lookup"><span data-stu-id="9a406-115">The system sends a [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) event to applications that have registered for the specific event using [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span></span> <span data-ttu-id="9a406-116">Pour plus d’informations, consultez [inscription pour les événements d’alimentation](registering-for-power-events.md).</span><span class="sxs-lookup"><span data-stu-id="9a406-116">For more information, see [Registering for Power Events](registering-for-power-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a406-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a406-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a406-118">À propos de la gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="9a406-118">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



