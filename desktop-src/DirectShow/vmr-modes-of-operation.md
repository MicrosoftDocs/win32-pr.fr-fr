---
description: Modes de fonctionnement VMR
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Modes de fonctionnement VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524520"
---
# <a name="vmr-modes-of-operation"></a><span data-ttu-id="1a188-103">Modes de fonctionnement VMR</span><span class="sxs-lookup"><span data-stu-id="1a188-103">VMR Modes of Operation</span></span>

<span data-ttu-id="1a188-104">L’architecture du composant VMR permet aux applications de les configurer de différentes manières, en fonction de la façon dont le rendu doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="1a188-104">The component architecture of the VMR enables applications to configure it in various ways, depending on how rendering is to be performed.</span></span> <span data-ttu-id="1a188-105">Le tableau suivant présente les trois modes de présentation et les deux modes de mixage, ainsi que les composants qui sont présents pour chaque configuration.</span><span class="sxs-lookup"><span data-stu-id="1a188-105">The following table shows the three presentation modes and the two mixing modes, and the components that are present for each configuration.</span></span>



| <span data-ttu-id="1a188-106">Mode</span><span class="sxs-lookup"><span data-stu-id="1a188-106">Mode</span></span>       | <span data-ttu-id="1a188-107">Flux unique</span><span class="sxs-lookup"><span data-stu-id="1a188-107">Single Stream</span></span>                                                                     | <span data-ttu-id="1a188-108">Plusieurs flux (mode de mixage)</span><span class="sxs-lookup"><span data-stu-id="1a188-108">Multiple Streams (Mixing Mode)</span></span>                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a188-109">Fenêtrées</span><span class="sxs-lookup"><span data-stu-id="1a188-109">Windowed</span></span>   | <span data-ttu-id="1a188-110">Allocator-unité de synchronisation presenterCore</span><span class="sxs-lookup"><span data-stu-id="1a188-110">Allocator-presenterCore Synchronization Unit</span></span><br/> <span data-ttu-id="1a188-111">Gestionnaire de fenêtres</span><span class="sxs-lookup"><span data-stu-id="1a188-111">Window Manager</span></span><br/> | <span data-ttu-id="1a188-112">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="1a188-112">MixerCompositor\*</span></span><br/> <span data-ttu-id="1a188-113">Allocator-présentateur</span><span class="sxs-lookup"><span data-stu-id="1a188-113">Allocator-presenter</span></span><br/> <span data-ttu-id="1a188-114">Unité de synchronisation principale</span><span class="sxs-lookup"><span data-stu-id="1a188-114">Core Synchronization Unit</span></span><br/> <span data-ttu-id="1a188-115">Gestionnaire de fenêtres</span><span class="sxs-lookup"><span data-stu-id="1a188-115">Window Manager</span></span><br/> |
| <span data-ttu-id="1a188-116">Sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="1a188-116">Windowless</span></span> | <span data-ttu-id="1a188-117">Allocator-unité de synchronisation presenterCore</span><span class="sxs-lookup"><span data-stu-id="1a188-117">Allocator-presenterCore Synchronization Unit</span></span><br/>                           | <span data-ttu-id="1a188-118">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="1a188-118">MixerCompositor\*</span></span><br/> <span data-ttu-id="1a188-119">Allocator-présentateur</span><span class="sxs-lookup"><span data-stu-id="1a188-119">Allocator-presenter</span></span><br/> <span data-ttu-id="1a188-120">Unité de synchronisation principale</span><span class="sxs-lookup"><span data-stu-id="1a188-120">Core Synchronization Unit</span></span><br/>                           |
| <span data-ttu-id="1a188-121">Rendu</span><span class="sxs-lookup"><span data-stu-id="1a188-121">Renderless</span></span> | <span data-ttu-id="1a188-122">Allocator-Presenter (fourni par l’application) unité de synchronisation principale</span><span class="sxs-lookup"><span data-stu-id="1a188-122">Allocator-presenter (provided by application)Core Synchronization Unit</span></span><br/> | <span data-ttu-id="1a188-123">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="1a188-123">MixerCompositor\*</span></span><br/> <span data-ttu-id="1a188-124">Allocator-Presenter (fourni par l’application)</span><span class="sxs-lookup"><span data-stu-id="1a188-124">Allocator-presenter (provided by application)</span></span><br/> <span data-ttu-id="1a188-125">Unité de synchronisation principale</span><span class="sxs-lookup"><span data-stu-id="1a188-125">Core Synchronization Unit</span></span><br/> |



 

<span data-ttu-id="1a188-126">\* Indique que l’application a la possibilité de fournir un composant personnalisé ou d’utiliser le composant par défaut.</span><span class="sxs-lookup"><span data-stu-id="1a188-126">\* Indicates that the application has the option to provide a custom component or use the default component.</span></span>

<span data-ttu-id="1a188-127">Dans toutes les configurations, le point principal à retenir lorsque vous créez des graphiques de filtre avec VMR est que vous devez configurer VMR avant de le connecter.</span><span class="sxs-lookup"><span data-stu-id="1a188-127">In all configurations, the main point to remember when you create filter graphs with the VMR is that you must configure the VMR before you connect it.</span></span>

<span data-ttu-id="1a188-128">Pour toutes les configurations, les codes confidentiels ne peuvent pas être ajoutés ou supprimés de manière dynamique une fois que VMR est connecté au filtre en amont, mais ils peuvent être connectés et déconnectés.</span><span class="sxs-lookup"><span data-stu-id="1a188-128">For all configurations, pins cannot be dynamically added or removed after the VMR is connected to the upstream filter, but they can be connected and disconnected.</span></span> <span data-ttu-id="1a188-129">Si l’application ne peut pas savoir combien de codes confidentiels seront nécessaires, elle doit configurer VMR pour le nombre maximal qui peut être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1a188-129">If the application is unsure how many pins will be needed, it should configure the VMR for the maximum number that might be needed.</span></span> <span data-ttu-id="1a188-130">La présence de broches d’entrée inutilisées sur le filtre ne dégrade pas les performances de rendu.</span><span class="sxs-lookup"><span data-stu-id="1a188-130">The presence of unused input pins on the filter does not degrade rendering performance.</span></span> <span data-ttu-id="1a188-131">Contrairement à l’ancien mélangeur de superposition, VMR n’a pas de broche de sortie, car il ne nécessite pas de filtre distinct pour la gestion des fenêtres.</span><span class="sxs-lookup"><span data-stu-id="1a188-131">Unlike the old Overlay Mixer, the VMR has no output pin because it does not require a separate filter for window management.</span></span>

<span data-ttu-id="1a188-132">Les sections suivantes décrivent comment configurer VMR pour un mode donné :</span><span class="sxs-lookup"><span data-stu-id="1a188-132">The following sections describe how to configure the VMR for a given mode:</span></span>

-   [<span data-ttu-id="1a188-133">Mode avec fenêtres VMR (compatibilité)</span><span class="sxs-lookup"><span data-stu-id="1a188-133">VMR Windowed (Compatibility) Mode</span></span>](vmr-windowed--compatibility--mode.md)
-   [<span data-ttu-id="1a188-134">Mode sans fenêtre VMR</span><span class="sxs-lookup"><span data-stu-id="1a188-134">VMR Windowless Mode</span></span>](vmr-windowless-mode.md)
-   [<span data-ttu-id="1a188-135">VMR avec plusieurs flux (mode de mixage)</span><span class="sxs-lookup"><span data-stu-id="1a188-135">VMR with Multiple Streams (Mixing Mode)</span></span>](vmr-with-multiple-streams--mixing-mode.md)
-   [<span data-ttu-id="1a188-136">Mode de mixage YUV</span><span class="sxs-lookup"><span data-stu-id="1a188-136">YUV Mixing Mode</span></span>](yuv-mixing-mode.md)
-   [<span data-ttu-id="1a188-137">Positionnement et déplacement de rectangles vidéo dans l’espace de composition</span><span class="sxs-lookup"><span data-stu-id="1a188-137">Positioning and Moving Video Rectangles in Composition Space</span></span>](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [<span data-ttu-id="1a188-138">Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)</span><span class="sxs-lookup"><span data-stu-id="1a188-138">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [<span data-ttu-id="1a188-139">Mode exclusif DirectDraw</span><span class="sxs-lookup"><span data-stu-id="1a188-139">DirectDraw Exclusive Mode</span></span>](directdraw-exclusive-mode.md)

 

 




