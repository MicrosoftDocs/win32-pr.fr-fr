---
title: Entrée MouseWheel pour Windows 8.1
description: Entrée MouseWheel pour Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839694"
---
# <a name="mousewheel-input-for-windows-81"></a><span data-ttu-id="18c8a-103">Entrée MouseWheel pour Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="18c8a-103">Mousewheel input for Windows 8.1</span></span>

## <a name="platform"></a><span data-ttu-id="18c8a-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="18c8a-104">Platform</span></span>

<dl> <span data-ttu-id="18c8a-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="18c8a-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="18c8a-106">Serveurs-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="18c8a-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="18c8a-107">Description</span><span class="sxs-lookup"><span data-stu-id="18c8a-107">Description</span></span>

<span data-ttu-id="18c8a-108">Dans Windows 8.1, les événements MouseWheel ne sont plus fournis en fonction du focus clavier, comme dans les versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="18c8a-108">In Windows 8.1, mousewheel events are no longer delivered based on keyboard focus as in previous versions of Windows.</span></span> <span data-ttu-id="18c8a-109">Dans Windows 8.1, si la souris pointe sur une application du Windows Store, MouseWheel sera remis à cette application ; Toutefois, à des fins de compatibilité, si la souris pointe sur une application de bureau, MouseWheel continuera à être remis en fonction du focus clavier.</span><span class="sxs-lookup"><span data-stu-id="18c8a-109">In Windows 8.1, if the mouse is hovering over a store app, mousewheel will be delivered to that app; for compatibility purposes, however, if the mouse is hovering over a desktop app, mousewheel will continue to be delivered based on keyboard focus.</span></span>

## <a name="manifestations"></a><span data-ttu-id="18c8a-110">Manifestations</span><span class="sxs-lookup"><span data-stu-id="18c8a-110">Manifestations</span></span>

<span data-ttu-id="18c8a-111">Lorsque la souris pointe sur les applications du Windows Store, MouseWheel fait défiler tout le contenu applicable sans que l’utilisateur ne soit obligé de cliquer sur l’application du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="18c8a-111">When the mouse is hovering over Store apps, mousewheel will scroll any applicable content without the user having to click on the Store app.</span></span> <span data-ttu-id="18c8a-112">Cela s’applique également à l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="18c8a-112">This also applies to the start screen.</span></span> <span data-ttu-id="18c8a-113">Cela permet de faire défiler par MouseWheel une interaction plus simple dans Windows 8.1 que dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="18c8a-113">This makes scrolling by mousewheel a simpler interaction in Windows 8.1 than in Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="18c8a-114">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="18c8a-114">Mitigation</span></span>

<span data-ttu-id="18c8a-115">La plupart du temps, cette modification ne doit pas avoir d’impact sur les applications existantes.</span><span class="sxs-lookup"><span data-stu-id="18c8a-115">For the most part this change should have no impact on existing apps.</span></span> <span data-ttu-id="18c8a-116">Si une application du Windows Store écoutait des événements MouseWheel uniquement après avoir inscrit un événement de clic de souris, cette application n’est pas susceptible de répondre à MouseWheel tant que l’utilisateur ne l’a pas activement cliqué.</span><span class="sxs-lookup"><span data-stu-id="18c8a-116">If a Store app listened for mousewheel events only after it has registered a mouse click event, that app would not be likely to respond to mousewheel until the user actively clicked it.</span></span> <span data-ttu-id="18c8a-117">Par conséquent, l’inconvénient le plus probable est simplement qu’une application continue à fonctionner comme dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="18c8a-117">Consequently, the most likely downside here is simply that an app continues to operate just as it did in Windows 8.</span></span> <span data-ttu-id="18c8a-118">Pour les applications de bureau, le focus clavier ne donne plus à l’application un monopole sur l’entrée MouseWheel, mais cela n’entraîne pas non plus l’interruption de ces applications.</span><span class="sxs-lookup"><span data-stu-id="18c8a-118">For desktop apps, having keyboard focus no longer gives the app a monopoly over mousewheel input, but this also does not in any way break those apps.</span></span> <span data-ttu-id="18c8a-119">Par conséquent, aucune atténuation à bref terme n’est requise.</span><span class="sxs-lookup"><span data-stu-id="18c8a-119">So no short-term mitigations are required.</span></span>

## <a name="solution"></a><span data-ttu-id="18c8a-120">Solution</span><span class="sxs-lookup"><span data-stu-id="18c8a-120">Solution</span></span>

<span data-ttu-id="18c8a-121">Les développeurs d’applications du Store doivent s’attendre à recevoir des événements MouseWheel sans événement de clic de souris précurseur.</span><span class="sxs-lookup"><span data-stu-id="18c8a-121">Store app developers should expect to receive mousewheel events without a precursor mouse click event.</span></span> <span data-ttu-id="18c8a-122">Ils ne doivent pas, par exemple, écouter les événements MouseWheel uniquement après l’inscription d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="18c8a-122">They should not, for example, listen for mousewheel events only after registering a mouse click.</span></span> <span data-ttu-id="18c8a-123">De même, les applications de bureau ne doivent pas essayer de capturer les événements MouseWheel (par exemple, en définissant un raccordement de bas niveau) lorsqu’ils ont le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="18c8a-123">Similarly, desktop applications should not try to capture mousewheel events (for example, by setting a low-level hook) when they have keyboard focus.</span></span>

## <a name="tests"></a><span data-ttu-id="18c8a-124">Tests</span><span class="sxs-lookup"><span data-stu-id="18c8a-124">Tests</span></span>

<span data-ttu-id="18c8a-125">Les développeurs d’applications du Store doivent effectuer des tests sur Windows 8.1 pour vérifier que toutes les fonctionnalités de défilement fonctionnent chaque fois que la souris pointe sur l’application.</span><span class="sxs-lookup"><span data-stu-id="18c8a-125">Store app developers should test on Windows 8.1 to verify that all scrolling functionality works whenever the mouse is hovering over the app.</span></span> <span data-ttu-id="18c8a-126">Les développeurs d’applications de bureau doivent effectuer des tests sur Windows 8.1 pour vérifier qu’ils ne capturent pas d’événements MouseWheel (conformément aux instructions ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="18c8a-126">Desktop app developers should test on Windows 8.1 to verify that they are not capturing mousewheel events (per guidance above.)</span></span>

 

 




