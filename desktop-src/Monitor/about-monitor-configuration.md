---
title: À propos de la configuration de l’analyse
description: À propos de la configuration de l’analyse
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- moniteur, à propos de
- moniteur, étalonnage des couleurs
- moniteur, réglage de la zone d’affichage du moniteur
- surveiller, enregistrer les paramètres de l’analyse
- surveiller, restaurer les paramètres d’analyse
- moniteur, fonctionnalités du fournisseur
- étalonnage des couleurs
- réglage de la zone d’affichage du moniteur
- enregistrement des paramètres de l’analyse
- restauration des paramètres d’analyse
- fonctionnalités du fournisseur
- configuration de l’analyse, étalonnage des couleurs
- configuration de l’analyse, à propos de
- surveiller la configuration, ajuster la zone d’affichage du moniteur
- surveiller la configuration, enregistrer les paramètres de l’analyse
- surveiller la configuration, restaurer les paramètres d’analyse
- configuration de l’analyse, fonctionnalités du fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d8e2f3d463bc84acaf8b48f493f5a0118976ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507178"
---
# <a name="about-monitor-configuration"></a><span data-ttu-id="5a8b9-120">À propos de la configuration de l’analyse</span><span class="sxs-lookup"><span data-stu-id="5a8b9-120">About Monitor Configuration</span></span>

<span data-ttu-id="5a8b9-121">Les fonctions de configuration de l’analyse sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a8b9-121">Uses for the monitor configuration functions include:</span></span>

-   <span data-ttu-id="5a8b9-122">Étalonnage des couleurs.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-122">Color calibration.</span></span> <span data-ttu-id="5a8b9-123">Une analyse correctement étalonnée reproduit correctement les couleurs.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-123">A properly calibrated monitor reproduces colors correctly.</span></span> <span data-ttu-id="5a8b9-124">En règle générale, une application d’étalonnage des couleurs affiche un modèle de test et dispose de contrôles pour modifier un paramètre d’analyse.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-124">Typically, a color calibration application displays a test pattern and has controls to change a monitor setting.</span></span> <span data-ttu-id="5a8b9-125">L’utilisateur modifie le paramètre jusqu’à ce qu’une condition soit remplie et répète ce processus pour chaque paramètre de l’analyse jusqu’à ce que l’analyseur soit étalonné.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-125">The user changes the setting until a condition is met, and repeats this process for each monitor setting until the monitor is calibrated.</span></span>
-   <span data-ttu-id="5a8b9-126">Ajustement de la zone d’affichage du moniteur.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-126">Adjusting the monitor's display area.</span></span> <span data-ttu-id="5a8b9-127">Les fonctions de configuration de l’analyse peuvent être utilisées pour modifier la taille et la position de la zone d’affichage d’un moniteur.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-127">The monitor configuration functions can be used to change the size and position of a monitor's display area.</span></span> <span data-ttu-id="5a8b9-128">Par exemple, lorsqu’un moniteur LCD est connecté à un ordinateur à l’aide d’un connecteur analogique, la meilleure qualité d’image est obtenue lorsqu’il existe un mappage un-à-un entre les pixels de la mémoire tampon de trame de la carte graphique et les pixels sur l’écran LCD.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-128">For example, when an LCD monitor is connected to a computer by using an analog connector, the best image quality is obtained when there is a one-to-one mapping between pixels in the graphics card's frame buffer and pixels on the LCD monitor.</span></span>
-   <span data-ttu-id="5a8b9-129">Enregistrement et restauration des paramètres d’analyse.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-129">Saving and restoring monitor settings.</span></span> <span data-ttu-id="5a8b9-130">Certains utilisateurs ont besoin de plusieurs ensembles de paramètres d’analyse, car différents scénarios nécessitent différents paramètres d’analyse.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-130">Some users need multiple sets of monitor settings, because different scenarios require different monitor settings.</span></span> <span data-ttu-id="5a8b9-131">Par exemple, les paramètres de surveillance optimaux pour les applications de bureau ne sont pas optimaux pour regarder la télévision.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-131">For example, monitor settings that are optimal for desktop applications are not optimal for watching television.</span></span>
-   <span data-ttu-id="5a8b9-132">Utilisation des fonctionnalités d’analyse spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-132">Using vendor-specific monitor features.</span></span> <span data-ttu-id="5a8b9-133">À l’aide des fonctions de configuration de l’analyse, les fabricants peuvent créer des applications qui utilisent les fonctionnalités spécifiques au fournisseur du moniteur.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-133">Using the monitor configuration functions, manufacturers can create applications that use the vendor-specific features of the monitor.</span></span>

<span data-ttu-id="5a8b9-134">Les fonctions de configuration de l’analyse sont divisées en fonctions de haut niveau et de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-134">The monitor configuration functions are divided into high-level and low-level functions.</span></span> <span data-ttu-id="5a8b9-135">Les fonctions de haut niveau sont plus faciles à utiliser que les fonctions de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-135">The high-level functions are easier to use than the low-level functions.</span></span> <span data-ttu-id="5a8b9-136">Pour utiliser les fonctions de haut niveau, vous n’avez rien à savoir sur l’interface de commande DDC/CI.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-136">To use the high-level functions, you do not need to know anything about the Display Data Channel Command Interface (DDC/CI).</span></span> <span data-ttu-id="5a8b9-137">Toutefois, les fonctions de haut niveau ne vous donnent pas accès aux fonctionnalités spécifiques au fournisseur du moniteur.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-137">However, the high-level functions do not give you access to vendor-specific features of the monitor.</span></span>

<span data-ttu-id="5a8b9-138">Les fonctions de bas niveau sont un wrapper léger autour des commandes DDC/CI.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-138">The low-level functions are a thin wrapper around the DDC/CI commands.</span></span> <span data-ttu-id="5a8b9-139">Pour utiliser les fonctions de bas niveau, vous devez être familiarisé avec la norme DDC/CI et avec la norme du jeu de commandes de contrôle du moniteur VESA (MCCS).</span><span class="sxs-lookup"><span data-stu-id="5a8b9-139">To use the low-level functions, you must be familiar with the DDC/CI standard and also with the VESA Monitor Control Command Set (MCCS) standard.</span></span> <span data-ttu-id="5a8b9-140">En général, vous devez utiliser les fonctions de haut niveau, sauf si vous avez besoin d’utiliser des fonctionnalités qui sont uniquement disponibles dans les fonctions de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-140">Generally, you should use the high-level functions unless you need to use features that are available only in the low-level functions.</span></span>

<span data-ttu-id="5a8b9-141">Les fonctions de configuration de l’analyse de haut niveau sont conçues de façon à ce qu’une application ne puisse pas mettre un moniteur dans un état inutilisable.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-141">The high-level monitor configuration functions are designed so that an application cannot put a monitor into an unusable state.</span></span> <span data-ttu-id="5a8b9-142">Les fonctions de bas niveau peuvent être utilisées pour envoyer des codes VCP à l’analyse.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-142">The low-level functions can be used to send VCP codes to the monitor.</span></span> <span data-ttu-id="5a8b9-143">Toutefois, sachez que certains codes VCP peuvent désactiver des fonctionnalités importantes ou placer l’analyse dans un État où l’utilisateur ne peut pas voir l’image d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5a8b9-143">However, be aware that some VCP codes can disable important functionality or put the monitor into a state where the user cannot see the display image.</span></span> <span data-ttu-id="5a8b9-144">Pour plus d’informations, consultez la norme du jeu de commandes de contrôle du moniteur VESA (MCCS).</span><span class="sxs-lookup"><span data-stu-id="5a8b9-144">For more information, see the VESA Monitor Control Command Set (MCCS) standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a8b9-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a8b9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a8b9-146">Configuration de l’analyse</span><span class="sxs-lookup"><span data-stu-id="5a8b9-146">Monitor Configuration</span></span>](monitor-configuration.md)
</dt> </dl>

 

 




