---
description: 'Vous pouvez utiliser un collecteur d’encres (InkCollector, InkOverlay ou InkPicture) pour accéder directement à la reconnaissance de mouvement Microsoft par défaut. Pour utiliser un collecteur d’encres pour accéder au module de reconnaissance de mouvement : définissez la propriété CollectionMode du collecteur d’encre en mode InkAndGesture ou en mode GestureOnly. inkOverlay. CollectionMode = CollectionMode. GestureOnly ; Choisissez le geste que vous souhaitez prendre en charge. inkOverlay. SetGestureStatus (ApplicationGesture. AllGestures, true); implémentez un gestionnaire d’événements qui reçoit des notifications de mouvement. Dans le gestionnaire d’événements, vous devez implémenter l’action correspondant à chaque événement reçu. Remarque le mode mixte ne prend en charge que les gestes à trait simple. Le mode geste prend en charge les gestes à plusieurs traits. inkOverlay. geste + = New InkCollectorGestureEventHandler ( \_ mouvement inkOverlay); en mode InkAndGesture, chaque trait individuel est envoyé au module de reconnaissance de mouvement Microsoft. S’il est reconnu comme un geste que vous avez activé, une notification d’événement est envoyée. Si l’application accepte la notification d’événement, le trait est effacé. Si l’application n’accepte pas la notification ou si le trait n’est pas reconnu comme un mouvement, le trait est stocké dans l’objet Ink. En mode GestureOnly, les traits sont délimités par des délais d’attente avant et après les traits. Les traits collectés dans le délai d’expiration sont envoyés au module de reconnaissance. Si les traits sont reconnus comme un geste que vous avez activé, une notification d’événement est envoyée. L’application peut accepter ou refuser l’événement, ce qui a pour effet d’appliquer l’action correspondante. En mode de mouvement uniquement, les traits ne sont jamais enregistrés dans l’objet Ink.'
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Utilisation du module de reconnaissance de mouvement Microsoft uniquement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80504e8b32c0b9596936bb4f07d029cd4ea8ddbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862490"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a><span data-ttu-id="dfda1-113">Utilisation du module de reconnaissance de mouvement Microsoft uniquement</span><span class="sxs-lookup"><span data-stu-id="dfda1-113">Using the Microsoft Gesture Recognizer Only</span></span>

<span data-ttu-id="dfda1-114">Vous pouvez utiliser un collecteur d’encres ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)ou [InkPicture](inkpicture-control-reference.md)) pour accéder directement à la reconnaissance de mouvement Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="dfda1-114">You can use an ink collector ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), or [InkPicture](inkpicture-control-reference.md)) to access the default Microsoft gesture recognizer directly.</span></span>

<span data-ttu-id="dfda1-115">Pour utiliser un collecteur d’encres pour accéder au module de reconnaissance de mouvement :</span><span class="sxs-lookup"><span data-stu-id="dfda1-115">To use an ink collector to access the gesture recognizer:</span></span>

-   <span data-ttu-id="dfda1-116">Définissez la propriété [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) du collecteur d’encre en mode **InkAndGesture** ou en mode **GestureOnly** .</span><span class="sxs-lookup"><span data-stu-id="dfda1-116">Set the [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) property of the ink collector to either **InkAndGesture** mode or **GestureOnly** mode.</span></span>

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   <span data-ttu-id="dfda1-117">Choisissez le geste que vous souhaitez prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="dfda1-117">Choose the gesture that you want to support.</span></span>

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   <span data-ttu-id="dfda1-118">Implémentez un gestionnaire d’événements qui reçoit des notifications de mouvement.</span><span class="sxs-lookup"><span data-stu-id="dfda1-118">Implement an event handler that receives gesture notifications.</span></span> <span data-ttu-id="dfda1-119">Dans le gestionnaire d’événements, vous devez implémenter l’action correspondant à chaque événement reçu.</span><span class="sxs-lookup"><span data-stu-id="dfda1-119">In the event handler, you need to implement the action corresponding to each event received.</span></span>
    > [!Note]  
    > <span data-ttu-id="dfda1-120">Le mode mixte ne prend en charge que les gestes à trait simple.</span><span class="sxs-lookup"><span data-stu-id="dfda1-120">Mixed mode supports only single-stroke gestures.</span></span> <span data-ttu-id="dfda1-121">Le mode geste prend en charge les gestes à plusieurs traits.</span><span class="sxs-lookup"><span data-stu-id="dfda1-121">Gesture mode supports multiple stroke gestures.</span></span>

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

<span data-ttu-id="dfda1-122">En mode **InkAndGesture** , chaque trait individuel est envoyé au module de reconnaissance de mouvement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dfda1-122">In **InkAndGesture** mode, each individual stroke is sent to the Microsoft gesture recognizer.</span></span> <span data-ttu-id="dfda1-123">S’il est reconnu comme un geste que vous avez activé, une notification d’événement est envoyée.</span><span class="sxs-lookup"><span data-stu-id="dfda1-123">If it is recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="dfda1-124">Si l’application accepte la notification d’événement, le trait est effacé.</span><span class="sxs-lookup"><span data-stu-id="dfda1-124">If the application accepts the event notification, the stroke is erased.</span></span> <span data-ttu-id="dfda1-125">Si l’application n’accepte pas la notification ou si le trait n’est pas reconnu comme un mouvement, le trait est stocké dans l’objet [**Ink**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="dfda1-125">If the application does not accept the notification or if the stroke is not recognized to be a gesture, the stroke is stored in the [**Ink**](inkdisp-class.md) object.</span></span>

<span data-ttu-id="dfda1-126">En mode **GestureOnly** , les traits sont délimités par des délais d’attente avant et après les traits.</span><span class="sxs-lookup"><span data-stu-id="dfda1-126">In **GestureOnly** mode, the strokes are delimited by timeouts before and after the strokes.</span></span> <span data-ttu-id="dfda1-127">Les traits collectés dans le délai d’expiration sont envoyés au module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="dfda1-127">The strokes collected within the timeout are sent to the recognizer.</span></span> <span data-ttu-id="dfda1-128">Si les traits sont reconnus comme un geste que vous avez activé, une notification d’événement est envoyée.</span><span class="sxs-lookup"><span data-stu-id="dfda1-128">If the strokes are recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="dfda1-129">L’application peut accepter ou refuser l’événement, ce qui a pour effet d’appliquer l’action correspondante.</span><span class="sxs-lookup"><span data-stu-id="dfda1-129">The application may accept or reject the event, effecting the corresponding action or not.</span></span> <span data-ttu-id="dfda1-130">En mode de mouvement uniquement, les traits ne sont jamais enregistrés dans l’objet [**Ink**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="dfda1-130">In gesture-only mode, the strokes are never saved in the [**Ink**](inkdisp-class.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfda1-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dfda1-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dfda1-132">[Microsoft. Ink. InkCollector. CollectionMode](/previous-versions/ms836497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="dfda1-132">[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="dfda1-133">[Microsoft. Ink. InkOverlay. CollectionMode](/previous-versions/ms833092(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="dfda1-133">[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="dfda1-134">[Microsoft. Ink. InkPicture. CollectionMode](/previous-versions/ms582182(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="dfda1-134">[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))</span></span>
</dt> </dl>

 

 
