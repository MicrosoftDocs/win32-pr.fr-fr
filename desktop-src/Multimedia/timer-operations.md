---
title: Opérations d’événement de minuterie
description: Opérations d’événement de minuterie
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- minuteries multimédias, événements
- minuteries, événements
- timeSetEvent fonction)
- timeKillEvent fonction)
- démarrage des événements du minuteur
- événements à une seule minuterie
- événements de minuteur périodiques
- annulation des événements du minuteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724797"
---
# <a name="timer-event-operations"></a><span data-ttu-id="e45e6-111">Opérations d’événement de minuterie</span><span class="sxs-lookup"><span data-stu-id="e45e6-111">Timer Event Operations</span></span>

<span data-ttu-id="e45e6-112">Une fois que vous avez établi la résolution de l’horloge de votre application, vous pouvez démarrer des événements de minuteur à l’aide de la fonction [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e45e6-112">After you have established your application's timer resolution, you can start timer events by using the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function.</span></span> <span data-ttu-id="e45e6-113">Cette fonction retourne un identificateur de minuterie qui peut être utilisé pour arrêter ou identifier des événements de minuterie.</span><span class="sxs-lookup"><span data-stu-id="e45e6-113">This function returns a timer identifier that can be used to stop or identify timer events.</span></span> <span data-ttu-id="e45e6-114">L’un des paramètres de la fonction est l’adresse d’une fonction de rappel [**TimeProc**](/previous-versions//dd757631(v=vs.85)) qui est appelée lorsque l’événement du minuteur se produit.</span><span class="sxs-lookup"><span data-stu-id="e45e6-114">One of the function's parameters is the address of a [**TimeProc**](/previous-versions//dd757631(v=vs.85)) callback function that is called when the timer event takes place.</span></span>

<span data-ttu-id="e45e6-115">Il existe deux types d’événements de minuterie : *unique* et *périodique*.</span><span class="sxs-lookup"><span data-stu-id="e45e6-115">There are two types of timer events: *single* and *periodic*.</span></span> <span data-ttu-id="e45e6-116">Un événement de minuterie unique se produit une fois, après un nombre spécifié de millisecondes.</span><span class="sxs-lookup"><span data-stu-id="e45e6-116">A single timer event occurs once, after a specified number of milliseconds.</span></span> <span data-ttu-id="e45e6-117">Un événement de minuteur périodique se produit chaque fois qu’un nombre de millisecondes spécifié est écoulé.</span><span class="sxs-lookup"><span data-stu-id="e45e6-117">A periodic timer event occurs every time a specified number of milliseconds elapses.</span></span> <span data-ttu-id="e45e6-118">L’intervalle entre les événements périodiques est appelé un *délai d’événement*.</span><span class="sxs-lookup"><span data-stu-id="e45e6-118">The interval between periodic events is called an *event delay*.</span></span> <span data-ttu-id="e45e6-119">Les événements de minuterie périodiques avec un délai d’événement de 10 millisecondes ou moins consomment une partie significative des ressources du processeur.</span><span class="sxs-lookup"><span data-stu-id="e45e6-119">Periodic timer events with an event delay of 10 milliseconds or less consume a significant portion of CPU resources.</span></span>

<span data-ttu-id="e45e6-120">La relation entre la résolution d’un événement de minuterie et la longueur du délai d’événements est importante dans les événements de minuterie.</span><span class="sxs-lookup"><span data-stu-id="e45e6-120">The relationship between the resolution of a timer event and the length of the event delay is important in timer events.</span></span> <span data-ttu-id="e45e6-121">Par exemple, si vous spécifiez une résolution de 5 et un délai d’événements de 100, les services de minuteur notifient la fonction de rappel après un intervalle compris entre 95 et 105 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="e45e6-121">For example, if you specify a resolution of 5 and an event delay of 100, the timer services notify the callback function after an interval ranging from 95 to 105 milliseconds.</span></span>

<span data-ttu-id="e45e6-122">Vous pouvez annuler un événement de minuteur actif à tout moment à l’aide de la fonction [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e45e6-122">You can cancel an active timer event at any time by using the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function.</span></span> <span data-ttu-id="e45e6-123">Veillez à annuler les minuteurs en suspens avant de libérer la mémoire contenant la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="e45e6-123">Be sure to cancel any outstanding timers before freeing the memory containing the callback function.</span></span>

> [!Note]  
> <span data-ttu-id="e45e6-124">Le minuteur multimédia s’exécute dans son propre thread.</span><span class="sxs-lookup"><span data-stu-id="e45e6-124">The multimedia timer runs in its own thread.</span></span>

 

 

 