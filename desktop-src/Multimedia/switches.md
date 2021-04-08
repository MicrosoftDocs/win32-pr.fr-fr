---
title: Commutateurs
description: Commutateurs
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- mixages audio, contrôles
- mixages audio, commutateurs
- mélangeurs, contrôles
- mélangeurs, commutateurs
- basculer les contrôles
- Structure MIXERCONTROLDETAILS_BOOLEAN
- Contrôle booléen
- contrôle Button
- contrôle activé/désactivé
- contrôle mono
- contrôle du volume
- contrôle étendu stéréo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842170"
---
# <a name="switches"></a><span data-ttu-id="d93f8-115">Commutateurs</span><span class="sxs-lookup"><span data-stu-id="d93f8-115">Switches</span></span>

<span data-ttu-id="d93f8-116">Les contrôles de commutateur sont des commutateurs à deux États.</span><span class="sxs-lookup"><span data-stu-id="d93f8-116">The switch controls are two-state switches.</span></span> <span data-ttu-id="d93f8-117">Ces contrôles utilisent la [**structure \_ booléenne MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) pour récupérer et définir des propriétés de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d93f8-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="d93f8-118">Le tableau suivant décrit les types de commutateurs.</span><span class="sxs-lookup"><span data-stu-id="d93f8-118">The following table describes the types of switches.</span></span>



| <span data-ttu-id="d93f8-119">Contrôler</span><span class="sxs-lookup"><span data-stu-id="d93f8-119">Control</span></span>         | <span data-ttu-id="d93f8-120">Description</span><span class="sxs-lookup"><span data-stu-id="d93f8-120">Description</span></span>                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d93f8-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="d93f8-121">Boolean</span></span>         | <span data-ttu-id="d93f8-122">Commutateur générique.</span><span class="sxs-lookup"><span data-stu-id="d93f8-122">The generic switch.</span></span> <span data-ttu-id="d93f8-123">Elle peut avoir la valeur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="d93f8-123">It can be set to **TRUE** or **FALSE**.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="d93f8-124">Bouton</span><span class="sxs-lookup"><span data-stu-id="d93f8-124">Button</span></span>          | <span data-ttu-id="d93f8-125">Affectez la valeur **true** à tous les boutons que le pilote doit gérer comme s’ils avaient été enfoncés.</span><span class="sxs-lookup"><span data-stu-id="d93f8-125">Set to **TRUE** for all buttons that the driver should handle as though they had been pressed.</span></span> <span data-ttu-id="d93f8-126">Si la valeur est **false**, aucune action n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="d93f8-126">If the value is **FALSE**, no action is taken.</span></span>                                                                                         |
| <span data-ttu-id="d93f8-127">Actif/inactif</span><span class="sxs-lookup"><span data-stu-id="d93f8-127">On/Off</span></span>          | <span data-ttu-id="d93f8-128">Autre commutateur qui est représenté par un graphique autre que celui utilisé pour le commutateur booléen.</span><span class="sxs-lookup"><span data-stu-id="d93f8-128">An alternative switch that is represented by a graphic other than the one used for the Boolean switch.</span></span> <span data-ttu-id="d93f8-129">Elle peut avoir la valeur ON ou OFF.</span><span class="sxs-lookup"><span data-stu-id="d93f8-129">It can be set to ON or OFF.</span></span>                                                                                                    |
| <span data-ttu-id="d93f8-130">Désactiver le son</span><span class="sxs-lookup"><span data-stu-id="d93f8-130">Mute</span></span>            | <span data-ttu-id="d93f8-131">Désactive une ligne audio (en supprimant le flux de données de la ligne) ou autorise la lecture des données audio.</span><span class="sxs-lookup"><span data-stu-id="d93f8-131">Mutes an audio line (suppressing the data flow of the line) or allows the audio data to play.</span></span> <span data-ttu-id="d93f8-132">Ce commutateur est fréquemment utilisé pour contrôler les lignes qui alimentent le mélangeur.</span><span class="sxs-lookup"><span data-stu-id="d93f8-132">This switch is frequently used to help control the lines feeding into the mixer.</span></span>                                                        |
| <span data-ttu-id="d93f8-133">Mono</span><span class="sxs-lookup"><span data-stu-id="d93f8-133">Mono</span></span>            | <span data-ttu-id="d93f8-134">Bascule entre la sortie mono et stéréo pour une ligne audio stéréo.</span><span class="sxs-lookup"><span data-stu-id="d93f8-134">Switches between mono and stereo output for a stereo audio line.</span></span> <span data-ttu-id="d93f8-135">Désactivez cette option pour lire les données stéréo en tant que canaux distincts.</span><span class="sxs-lookup"><span data-stu-id="d93f8-135">Set to OFF to play stereo data as separate channels.</span></span> <span data-ttu-id="d93f8-136">Affectez la valeur ON pour combiner des données des deux canaux en une ligne audio mono.</span><span class="sxs-lookup"><span data-stu-id="d93f8-136">Set to ON to combine data from both channels into a mono audio line.</span></span>                                            |
| <span data-ttu-id="d93f8-137">Niveau sonore</span><span class="sxs-lookup"><span data-stu-id="d93f8-137">Loudness</span></span>        | <span data-ttu-id="d93f8-138">Amplifie les basses de faible volume pour une ligne audio.</span><span class="sxs-lookup"><span data-stu-id="d93f8-138">Boosts low-volume bass for an audio line.</span></span> <span data-ttu-id="d93f8-139">Affectez la valeur ON pour augmenter les basses de faible volume.</span><span class="sxs-lookup"><span data-stu-id="d93f8-139">Set to ON to boost low-volume bass.</span></span> <span data-ttu-id="d93f8-140">Désactivez cette option pour définir les niveaux de volume sur normal.</span><span class="sxs-lookup"><span data-stu-id="d93f8-140">Set to OFF to set volume levels to normal.</span></span> <span data-ttu-id="d93f8-141">La quantité d’augmentation est spécifique au matériel.</span><span class="sxs-lookup"><span data-stu-id="d93f8-141">The amount of boost is hardware specific.</span></span> <span data-ttu-id="d93f8-142">Pour plus d’informations, consultez la documentation de votre appareil de mixage.</span><span class="sxs-lookup"><span data-stu-id="d93f8-142">For more information, see the documentation for your mixer device.</span></span> |
| <span data-ttu-id="d93f8-143">Stéréo améliorée</span><span class="sxs-lookup"><span data-stu-id="d93f8-143">Stereo Enhanced</span></span> | <span data-ttu-id="d93f8-144">Augmente la séparation stéréo.</span><span class="sxs-lookup"><span data-stu-id="d93f8-144">Increases stereo separation.</span></span> <span data-ttu-id="d93f8-145">Affectez la valeur ON pour augmenter la séparation stéréo.</span><span class="sxs-lookup"><span data-stu-id="d93f8-145">Set to ON to increase stereo separation.</span></span> <span data-ttu-id="d93f8-146">Désactivez la valeur OFF pour aucune amélioration.</span><span class="sxs-lookup"><span data-stu-id="d93f8-146">Set to OFF for no enhancement.</span></span>                                                                                                                                  |



 

 

 