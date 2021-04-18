---
description: Les applications peuvent attendre un événement lorsque le rendu à l’écran est inutile (c’est-à-dire, alors qu’ils sont bloqués).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: En attente d’un événement lorsque le rendu est inutile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519173"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a><span data-ttu-id="1ed01-103">En attente d’un événement lorsque le rendu est inutile</span><span class="sxs-lookup"><span data-stu-id="1ed01-103">Waiting on an event when rendering is unnecessary</span></span>

<span data-ttu-id="1ed01-104">Les applications peuvent attendre un événement lorsque le rendu à l’écran est inutile (c’est-à-dire, alors qu’ils sont bloqués).</span><span class="sxs-lookup"><span data-stu-id="1ed01-104">Apps can wait on an event when rendering to the screen is unnecessary (that is, while they are occluded).</span></span> <span data-ttu-id="1ed01-105">Lorsque le Gestionnaire de fenêtrage (DWM) ou une application est bloqués, aucun rendu n’est nécessaire et le système d’exploitation peut rester dans des États d’alimentation inférieurs pendant des périodes plus longues.</span><span class="sxs-lookup"><span data-stu-id="1ed01-105">When the Desktop Window Manager (DWM) or an app is occluded, no rendering is necessary and the operating system can stay in lower power states for longer periods of time.</span></span> <span data-ttu-id="1ed01-106">Cela économise de l’énergie et augmente la durée de vie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="1ed01-106">This saves power and extends battery life.</span></span>

<span data-ttu-id="1ed01-107">Une application peut attendre un événement dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="1ed01-107">An app can wait on an event when:</span></span>

-   <span data-ttu-id="1ed01-108">Toutes les analyses sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="1ed01-108">All the monitors are off.</span></span>
-   <span data-ttu-id="1ed01-109">La session dans laquelle l’application s’exécute est déconnectée.</span><span class="sxs-lookup"><span data-stu-id="1ed01-109">The session that the app runs in is disconnected.</span></span>
-   <span data-ttu-id="1ed01-110">L’application s’exécute en mode plein écran exclusivement sur une configuration de moniteur unique.</span><span class="sxs-lookup"><span data-stu-id="1ed01-110">The app runs in full screen exclusively on a single monitor configuration.</span></span>
-   <span data-ttu-id="1ed01-111">L’application s’exécute sur un bureau autre que le bureau actif et n’est pas autorisée à effectuer un rendu sur le bureau actif.</span><span class="sxs-lookup"><span data-stu-id="1ed01-111">The app runs on a different desktop than the active desktop and does not have permission to render on the active desktop.</span></span>

<span data-ttu-id="1ed01-112">Le système d’exploitation déclenche l’événement lorsque l’application peut effectuer un rendu à nouveau.</span><span class="sxs-lookup"><span data-stu-id="1ed01-112">The operating system triggers the event when the app is able to render again.</span></span> <span data-ttu-id="1ed01-113">L’événement n’est pas effacé au cours d’une mise à niveau du pilote, ou de la procession de détection et de récupération du délai d’attente (TDR). Toutefois, il est effacé lorsque la nouvelle carte et les moniteurs deviennent actifs.</span><span class="sxs-lookup"><span data-stu-id="1ed01-113">The event is not cleared during a driver upgrade, or timeout detection and recovery (TDR) procession, however it is cleared when the new adapter and monitors become active.</span></span>

<span data-ttu-id="1ed01-114">Si vous souhaitez que votre application soit avertie des modifications de l’état d’occlusion, l’application doit s’inscrire pour ces modifications.</span><span class="sxs-lookup"><span data-stu-id="1ed01-114">If you want your app to be notified about changes of occlusion status, the app must register for these changes.</span></span> <span data-ttu-id="1ed01-115">Une application peut s’inscrire pour être avertie des modifications de l’état d’occlusion par le biais d’un message dans une fenêtre ou par le biais d’une signalisation d’événement.</span><span class="sxs-lookup"><span data-stu-id="1ed01-115">An app can register to be notified about changes of occlusion status through a message to a window or through event signaling.</span></span> <span data-ttu-id="1ed01-116">Pour s’inscrire afin de recevoir des messages de notification dans une fenêtre sur les modifications de l’état d’occlusion, une application appelle la méthode [**IDXGIFactory2 :: RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) .</span><span class="sxs-lookup"><span data-stu-id="1ed01-116">To register to receive notification messages to a window about occlusion status changes, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) method.</span></span> <span data-ttu-id="1ed01-117">Pour s’inscrire afin de recevoir la notification des modifications d’état d’occlusion via la signalisation d’événement, une application appelle la méthode [**IDXGIFactory2 :: RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) .</span><span class="sxs-lookup"><span data-stu-id="1ed01-117">To register to receive notification of occlusion status changes via event signaling, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) method.</span></span> <span data-ttu-id="1ed01-118">Les deux méthodes retournent un pointeur vers une valeur de clé que l’application peut utiliser pour annuler l’inscription de la notification.</span><span class="sxs-lookup"><span data-stu-id="1ed01-118">Both methods return a pointer to a key value that the app can use to unregister the notification.</span></span> <span data-ttu-id="1ed01-119">Pour annuler l’inscription de la notification, l’application passe cette valeur de clé à la méthode [**IDXGIFactory2 :: UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) .</span><span class="sxs-lookup"><span data-stu-id="1ed01-119">To unregister the notification, the app passes this key value to the [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ed01-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ed01-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ed01-121">Améliorations de DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="1ed01-121">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



