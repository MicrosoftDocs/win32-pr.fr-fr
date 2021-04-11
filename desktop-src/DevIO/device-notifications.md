---
description: Le système diffuse un ensemble d’événements de changement d’appareil par défaut à l’ensemble des applications et services.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Notifications de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caeee8ba50a62a3bc393172347be09d1ac58085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111178"
---
# <a name="device-notifications"></a><span data-ttu-id="a64b5-103">Notifications de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a64b5-103">Device Notifications</span></span>

<span data-ttu-id="a64b5-104">Le système diffuse un ensemble d’événements de changement d’appareil par défaut à l’ensemble des applications et services.</span><span class="sxs-lookup"><span data-stu-id="a64b5-104">The system broadcasts a set of default device change events to all applications and services.</span></span> <span data-ttu-id="a64b5-105">Vous n’avez pas besoin de vous inscrire pour recevoir ces événements par défaut.</span><span class="sxs-lookup"><span data-stu-id="a64b5-105">You do not need to register to receive these default events.</span></span> <span data-ttu-id="a64b5-106">Pour plus d’informations, consultez la section Notes dans [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="a64b5-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details.</span></span> <span data-ttu-id="a64b5-107">Pour spécifier d’autres événements que votre application ou service doit recevoir, utilisez la fonction **RegisterDeviceNotification** .</span><span class="sxs-lookup"><span data-stu-id="a64b5-107">To specify other events your application or service should receive, use the **RegisterDeviceNotification** function.</span></span>

<span data-ttu-id="a64b5-108">Lorsqu’une application ou un service appelle [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), elle spécifie également la fenêtre qui recevra les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="a64b5-108">When an application or service calls [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), it also specifies the window that will receive the notification events.</span></span> <span data-ttu-id="a64b5-109">Les services peuvent spécifier un handle d’état de service au lieu d’un handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a64b5-109">Services can specify a service status handle instead of a window handle.</span></span> <span data-ttu-id="a64b5-110">Si un service spécifie son descripteur d’État du service, son gestionnaire de contrôle des services recevra les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="a64b5-110">If a service specifies its service status handle, its service control handler will receive the notification events.</span></span> <span data-ttu-id="a64b5-111">Pour plus d’informations, consultez [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="a64b5-111">For more information, see [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="a64b5-112">Veillez à gérer Plug-and-Play événements d’appareil aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="a64b5-112">Be sure to handle Plug and Play device events as quickly as possible.</span></span> <span data-ttu-id="a64b5-113">Dans le cas contraire, le système risque de ne plus répondre.</span><span class="sxs-lookup"><span data-stu-id="a64b5-113">Otherwise, the system may become unresponsive.</span></span> <span data-ttu-id="a64b5-114">Si votre gestionnaire d’événements doit effectuer une opération qui peut bloquer l’exécution (par exemple, les e/s), il est préférable de démarrer un autre thread pour effectuer l’opération de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a64b5-114">If your event handler is to perform an operation that may block execution (such as I/O), it is best to start another thread to perform the operation asynchronously.</span></span>

<span data-ttu-id="a64b5-115">Les descripteurs de notification de périphérique retournés par [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) doivent être fermés en appelant la fonction [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) lorsqu’ils ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="a64b5-115">Device notification handles returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) must be closed by calling the [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) function when they are no longer needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a64b5-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a64b5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a64b5-117">Inscription aux notifications de l’appareil</span><span class="sxs-lookup"><span data-stu-id="a64b5-117">Registering for device notification</span></span>](registering-for-device-notification.md)
</dt> </dl>

 

 
