---
title: Gestionnaire de fenêtrage
description: Gestionnaire de fenêtrage
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fca8550134ba0c1cdafe0bd5c349061ef900a9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103897"
---
# <a name="the-desktop-window-manager"></a><span data-ttu-id="c6829-103">Gestionnaire de fenêtrage</span><span class="sxs-lookup"><span data-stu-id="c6829-103">The Desktop Window Manager</span></span>

<span data-ttu-id="c6829-104">Avant Windows Vista, un programme Windows serait directement dessiné à l’écran.</span><span class="sxs-lookup"><span data-stu-id="c6829-104">Before Windows Vista, a Windows program would draw directly to the screen.</span></span> <span data-ttu-id="c6829-105">En d’autres termes, le programme écrit directement dans la mémoire tampon indiquée par la carte vidéo.</span><span class="sxs-lookup"><span data-stu-id="c6829-105">In other words, the program would write directly to the memory buffer shown by the video card.</span></span> <span data-ttu-id="c6829-106">Cette approche peut provoquer des artefacts visuels si une fenêtre ne se repeint pas correctement.</span><span class="sxs-lookup"><span data-stu-id="c6829-106">This approach can cause visual artifacts if a window does not repaint itself correctly.</span></span> <span data-ttu-id="c6829-107">Par exemple, si l’utilisateur fait glisser une fenêtre sur une autre fenêtre, et que la fenêtre située en dessous ne se redessine pas suffisamment rapidement, la fenêtre supérieure peut sortir d’une piste :</span><span class="sxs-lookup"><span data-stu-id="c6829-107">For example, if the user drags one window over another window, and the window underneath does not repaint itself quickly enough, the top-most window can leave a trail:</span></span>

![capture d’écran qui montre les artefacts de redessin.](images/graphics04.png)

<span data-ttu-id="c6829-109">La trace est due au fait que Windows peigne à la même zone de mémoire.</span><span class="sxs-lookup"><span data-stu-id="c6829-109">The trail is caused because both windows paint to the same area of memory.</span></span> <span data-ttu-id="c6829-110">Lorsque vous faites glisser la fenêtre de niveau supérieur, la fenêtre située en dessous doit être redessinée.</span><span class="sxs-lookup"><span data-stu-id="c6829-110">As the top-most window is dragged, the window below it must be repainted.</span></span> <span data-ttu-id="c6829-111">Si le redessin est trop lent, cela provoque l’affichage des artefacts dans l’image précédente.</span><span class="sxs-lookup"><span data-stu-id="c6829-111">If the repainting is too slow, it causes the artifacts shown in the previous image.</span></span>

<span data-ttu-id="c6829-112">Windows Vista a modifié fondamentalement la manière dont les fenêtres sont dessinées, en introduisant le Gestionnaire de fenêtrage (DWM).</span><span class="sxs-lookup"><span data-stu-id="c6829-112">Windows Vista fundamentally changed how windows are drawn, by introducing the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="c6829-113">Lorsque le DWM est activé, une fenêtre ne dessine plus directement dans la mémoire tampon d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c6829-113">When the DWM is enabled, a window no longer draws directly to the display buffer.</span></span> <span data-ttu-id="c6829-114">Au lieu de cela, chaque fenêtre dessine dans une mémoire tampon hors écran, également appelée *surface hors écran*.</span><span class="sxs-lookup"><span data-stu-id="c6829-114">Instead, each window draws to an offscreen memory buffer, also called an *offscreen surface*.</span></span> <span data-ttu-id="c6829-115">Le DWM compose ensuite ces surfaces à l’écran.</span><span class="sxs-lookup"><span data-stu-id="c6829-115">The DWM then composites these surfaces to the screen.</span></span>

![diagramme qui montre comment le DWM composite le bureau.](images/graphics05.png)

<span data-ttu-id="c6829-117">Le DWM offre plusieurs avantages par rapport à l’ancienne architecture graphique.</span><span class="sxs-lookup"><span data-stu-id="c6829-117">The DWM provides several advantages over the old graphics architecture.</span></span>

-   <span data-ttu-id="c6829-118">Moins de messages de redessin.</span><span class="sxs-lookup"><span data-stu-id="c6829-118">Fewer repaint messages.</span></span> <span data-ttu-id="c6829-119">Quand une fenêtre est obstruée par une autre fenêtre, la fenêtre masquée n’a pas besoin de se repeindre.</span><span class="sxs-lookup"><span data-stu-id="c6829-119">When a window is obstructed by another window, the obstructed window does not need to repaint itself.</span></span>
-   <span data-ttu-id="c6829-120">Des artefacts réduits.</span><span class="sxs-lookup"><span data-stu-id="c6829-120">Reduced artifacts.</span></span> <span data-ttu-id="c6829-121">Auparavant, le fait de faire glisser une fenêtre pouvait créer des artefacts visuels, comme décrit.</span><span class="sxs-lookup"><span data-stu-id="c6829-121">Previously, dragging a window could create visual artifacts, as described.</span></span>
-   <span data-ttu-id="c6829-122">Effets visuels.</span><span class="sxs-lookup"><span data-stu-id="c6829-122">Visual effects.</span></span> <span data-ttu-id="c6829-123">Étant donné que le DWM est en mesure de comcréer l’écran, il peut restituer des zones translucides et floues de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c6829-123">Because the DWM is in charge of compositing the screen, it can render translucent and blurred areas of the window.</span></span>
-   <span data-ttu-id="c6829-124">Mise à l’échelle automatique pour la haute résolution.</span><span class="sxs-lookup"><span data-stu-id="c6829-124">Automatic scaling for high DPI.</span></span> <span data-ttu-id="c6829-125">Même si la mise à l’échelle n’est pas la méthode idéale pour gérer les résolutions élevées, il s’agit d’un secours viable pour les applications plus anciennes qui n’ont pas été conçues pour des paramètres haute résolution.</span><span class="sxs-lookup"><span data-stu-id="c6829-125">Although scaling is not the ideal way to handle high DPI, it is a viable fallback for older applications that were not designed for high DPI settings.</span></span> <span data-ttu-id="c6829-126">(Nous allons revenir à cette rubrique plus tard, dans la section [dpi et Device-Independent pixels](dpi-and-device-independent-pixels.md).)</span><span class="sxs-lookup"><span data-stu-id="c6829-126">(We will return to this topic later, in the section [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).)</span></span>
-   <span data-ttu-id="c6829-127">Autres affichages.</span><span class="sxs-lookup"><span data-stu-id="c6829-127">Alternative views.</span></span> <span data-ttu-id="c6829-128">Le DWM peut utiliser les surfaces hors écran de différentes façons intéressantes.</span><span class="sxs-lookup"><span data-stu-id="c6829-128">The DWM can use the offscreen surfaces in various interesting ways.</span></span> <span data-ttu-id="c6829-129">Par exemple, le DWM est la technologie sous-jacente de Windows Flip 3D, des miniatures et des transitions animées.</span><span class="sxs-lookup"><span data-stu-id="c6829-129">For example, the DWM is the technology behind Windows Flip 3D, thumbnails, and animated transitions.</span></span>

<span data-ttu-id="c6829-130">Notez, cependant, qu’il n’est pas garanti que le DWM soit activé.</span><span class="sxs-lookup"><span data-stu-id="c6829-130">Note, however, that the DWM is not guaranteed to be enabled.</span></span> <span data-ttu-id="c6829-131">La carte graphique ne prend peut-être pas en charge la configuration système requise pour DWM et les utilisateurs peuvent désactiver le DWM via le panneau de configuration **Propriétés système** .</span><span class="sxs-lookup"><span data-stu-id="c6829-131">The graphics card might not support the DWM system requirements, and users can disable the DWM through the **System Properties** control panel.</span></span> <span data-ttu-id="c6829-132">Cela signifie que votre programme ne doit pas reposer sur le comportement de redessin du DWM.</span><span class="sxs-lookup"><span data-stu-id="c6829-132">That means your program should not rely on the repainting behavior of the DWM.</span></span> <span data-ttu-id="c6829-133">Testez votre programme avec DWM désactivé pour vous assurer qu’il se repeint correctement.</span><span class="sxs-lookup"><span data-stu-id="c6829-133">Test your program with DWM disabled to make sure that it repaints correctly.</span></span>

## <a name="next"></a><span data-ttu-id="c6829-134">Suivant</span><span class="sxs-lookup"><span data-stu-id="c6829-134">Next</span></span>

[<span data-ttu-id="c6829-135">Mode de conservation et mode immédiat</span><span class="sxs-lookup"><span data-stu-id="c6829-135">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)

 

 




