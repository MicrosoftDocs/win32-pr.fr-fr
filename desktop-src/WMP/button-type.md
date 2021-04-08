---
title: Type de bouton
description: Type de bouton
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Windows Media Player Mobile Skins, types de boutons
- apparences, types de bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, types
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839566"
---
# <a name="button-type"></a><span data-ttu-id="3e7e7-107">Type de bouton</span><span class="sxs-lookup"><span data-stu-id="3e7e7-107">Button Type</span></span>

<span data-ttu-id="3e7e7-108">Les boutons se présentent sous deux types généraux : emplacement et région.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-108">Buttons come in two general types: location and region.</span></span> <span data-ttu-id="3e7e7-109">Chaque type général a trois types spécifiques, en effectuant six types de boutons.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-109">Each general type has three specific types, making six button types in all.</span></span>

> [!Note]  
> <span data-ttu-id="3e7e7-110">Les types de boutons sont déconseillés dans les habillages pour Windows Media Player 10 mobile ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-110">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="3e7e7-111">Types de boutons d’emplacement</span><span class="sxs-lookup"><span data-stu-id="3e7e7-111">Location Button Types</span></span>

<span data-ttu-id="3e7e7-112">Les boutons d’emplacement utilisent des coordonnées pour définir leurs emplacements par rapport à l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-112">Location buttons use coordinates to define their locations relative to the background.</span></span> <span data-ttu-id="3e7e7-113">Le tableau suivant indique les valeurs qui sont valides pour les types de bouton d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-113">The following table shows the values that are valid for location button types.</span></span> <span data-ttu-id="3e7e7-114">Vous n’avez pas besoin de définir des valeurs pour les types que vous n’utiliserez pas dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-114">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="3e7e7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e7e7-115">Value</span></span>  | <span data-ttu-id="3e7e7-116">Description</span><span class="sxs-lookup"><span data-stu-id="3e7e7-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7e7-117">Envoi de données (push)</span><span class="sxs-lookup"><span data-stu-id="3e7e7-117">Push</span></span>   | <span data-ttu-id="3e7e7-118">Définit un bouton qui déclenche un événement une seule fois.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-118">Defines a button that triggers an event once.</span></span> <span data-ttu-id="3e7e7-119">Le bouton doit être envoyé à chaque fois pour déclencher d’autres événements.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-119">The button must be pushed each time to trigger further events.</span></span> <span data-ttu-id="3e7e7-120">Par exemple, un bouton se déplace vers l’élément suivant dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-120">An example would be a button that moves to the next item in the playlist.</span></span> <span data-ttu-id="3e7e7-121">L’emplacement du bouton est défini par ses coordonnées.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-121">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3e7e7-122">Bascule</span><span class="sxs-lookup"><span data-stu-id="3e7e7-122">Toggle</span></span> | <span data-ttu-id="3e7e7-123">Définit un bouton qui déclenche un événement qui modifie un État.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-123">Defines a button that triggers an event that changes a state.</span></span> <span data-ttu-id="3e7e7-124">L’état reste jusqu’à ce que le bouton fasse l’objet d’un push.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-124">The state remains until the button is pushed again.</span></span> <span data-ttu-id="3e7e7-125">Par exemple, un bouton qui mélange la playlist.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-125">An example is a button that shuffles the playlist.</span></span> <span data-ttu-id="3e7e7-126">Une fois que la sélection est dans un état aléatoire, elle reste aléatoire jusqu’à ce que le bouton soit de nouveau envoyé.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-126">Once the playlist is in a shuffled state, it will remain shuffled until the button is pushed again.</span></span> <span data-ttu-id="3e7e7-127">L’emplacement du bouton est défini par ses coordonnées.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-127">The location of the button is defined by its coordinates.</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3e7e7-128">2Push</span><span class="sxs-lookup"><span data-stu-id="3e7e7-128">2Push</span></span>  | <span data-ttu-id="3e7e7-129">Définit un bouton qui déclenche un événement, puis passe à un État qui est prêt à déclencher un événement différent.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-129">Defines a button that triggers an event, and then changes to a state that is ready to trigger a different event.</span></span> <span data-ttu-id="3e7e7-130">Les deux États sont activés chaque fois que le bouton est poussé.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-130">The two states are toggled every time the button is pushed.</span></span> <span data-ttu-id="3e7e7-131">Par exemple, un bouton qui utilise la fonction **PlayPause** pour basculer entre la diffusion et la suspension de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-131">An example is a button that uses the **PlayPause** function to toggle between playing and pausing the current media item.</span></span> <span data-ttu-id="3e7e7-132">Lorsque le bouton est poussé la première fois, l’état de lecture principal est déclenché et une image secondaire est affichée pour indiquer qu’un événement de **Pause** peut être déclenché.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-132">When the button is pushed the first time, the primary Play state is triggered and a secondary image is displayed to indicate that a **Pause** event can be triggered.</span></span> <span data-ttu-id="3e7e7-133">Lorsque le bouton est envoyé à nouveau, l’État pause est déclenché et l’image d’origine est affichée pour indiquer qu’un événement de **lecture** peut être déclenché.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-133">When the button is pushed again, the Pause state is triggered and the original image is displayed to indicate that a **Play** event can be triggered.</span></span> <span data-ttu-id="3e7e7-134">L’emplacement du bouton est défini par ses coordonnées.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-134">The location of the button is defined by its coordinates.</span></span> |



 

<span data-ttu-id="3e7e7-135">Types de boutons de région</span><span class="sxs-lookup"><span data-stu-id="3e7e7-135">Region Button Types</span></span>

<span data-ttu-id="3e7e7-136">Les boutons de région utilisent des zones de couleur dans l’image de la région pour définir où les robinets seront traités pour un bouton particulier.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-136">Region buttons use color areas in the Region image to define where taps will be processed for a particular button.</span></span> <span data-ttu-id="3e7e7-137">Le tableau suivant indique les valeurs qui sont valides pour les types de bouton de région.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-137">The following table shows the values that are valid for region button types.</span></span> <span data-ttu-id="3e7e7-138">Vous n’avez pas besoin de définir des valeurs pour les types que vous n’utiliserez pas dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-138">You do not need to define values for types you will not be using in your skin.</span></span>



| <span data-ttu-id="3e7e7-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e7e7-139">Value</span></span>     | <span data-ttu-id="3e7e7-140">Description</span><span class="sxs-lookup"><span data-stu-id="3e7e7-140">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7e7-141">PushHit</span><span class="sxs-lookup"><span data-stu-id="3e7e7-141">PushHit</span></span>   | <span data-ttu-id="3e7e7-142">Semblable à la valeur du bouton de commande, à la différence près que la zone d’accès du bouton est définie par la valeur de couleur dans l’image de la région.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-142">Similar to the Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>   |
| <span data-ttu-id="3e7e7-143">ToggleHit</span><span class="sxs-lookup"><span data-stu-id="3e7e7-143">ToggleHit</span></span> | <span data-ttu-id="3e7e7-144">Semblable à la valeur du bouton bascule, à la différence près que la zone d’accès du bouton est définie par la valeur de couleur dans l’image de la région.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-144">Similar to the Toggle button value except that the hit area of the button is defined by the color value in the Region image.</span></span> |
| <span data-ttu-id="3e7e7-145">2PushHit</span><span class="sxs-lookup"><span data-stu-id="3e7e7-145">2PushHit</span></span>  | <span data-ttu-id="3e7e7-146">Semblable à la valeur du bouton 2Push, à ceci près que la zone d’accès du bouton est définie par la valeur de couleur dans l’image de la région.</span><span class="sxs-lookup"><span data-stu-id="3e7e7-146">Similar to the 2Push button value except that the hit area of the button is defined by the color value in the Region image.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="3e7e7-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e7e7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e7e7-148">**Boutons**</span><span class="sxs-lookup"><span data-stu-id="3e7e7-148">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




