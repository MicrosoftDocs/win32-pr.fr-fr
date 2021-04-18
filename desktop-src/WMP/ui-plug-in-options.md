---
title: Options du plug-in d’interface utilisateur
description: Options du plug-in d’interface utilisateur
ms.assetid: 3c188506-865c-4e0c-965d-1429eafd01ef
keywords:
- Plug-ins du lecteur Windows Media, options
- plug-ins, options
- plug-ins d’interface utilisateur, options
- Plug-ins d’interface utilisateur, options
- plug-ins de zone Paramètres
- plug-ins d’arrière-plan
- plug-ins de fenêtre distincts
- plug-ins de zone de métadonnées
- plug-ins de zone d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281dd0679e6a975b1c867624f2f652f2b3e6b9ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106526928"
---
# <a name="ui-plug-in-options"></a><span data-ttu-id="7b748-112">Options du plug-in d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="7b748-112">UI Plug-in Options</span></span>

<span data-ttu-id="7b748-113">L’un des cinq types de plug-in d’interface utilisateur peut avoir une page de propriétés dans laquelle l’utilisateur peut modifier des paramètres de plug-in.</span><span class="sxs-lookup"><span data-stu-id="7b748-113">Any of the five UI plug-in types can have a property page where the user can modify plug-in settings.</span></span> <span data-ttu-id="7b748-114">Cette page de propriétés peut être définie pour s’afficher automatiquement lorsqu’un plug-in est chargé pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="7b748-114">This property page can be set to display automatically when a plug-in is loaded for the first time.</span></span> <span data-ttu-id="7b748-115">Vous pouvez également y accéder à partir de l’onglet Plug-ins de la boîte de dialogue Options.</span><span class="sxs-lookup"><span data-stu-id="7b748-115">It can also be accessed from the Plug-ins tab of the Options dialog box.</span></span>

<span data-ttu-id="7b748-116">Un plug-in d’interface utilisateur peut être configuré pour être chargé automatiquement après l’installation au démarrage du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7b748-116">A UI plug-in can be set to load automatically after installation when Windows Media Player is started.</span></span> <span data-ttu-id="7b748-117">S’il n’est pas démarré automatiquement, l’utilisateur peut le charger en le sélectionnant dans la liste des **plug-ins** du menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="7b748-117">If it is not started automatically, the user can load it by selecting it from the **Plug-ins** list on the **Tools** menu.</span></span>

<span data-ttu-id="7b748-118">Un plug-in de zone d’affichage peut avoir plusieurs présélections, qui sont des vues différentes que le plug-in peut mettre à la disposition de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b748-118">A display area plug-in can have multiple presets, which are different views that the plug-in can make available to the user.</span></span> <span data-ttu-id="7b748-119">L’utilisateur peut modifier la présélection en sélectionnant une entrée différente dans la liste **visualisations et vues** du menu **affichage** , ou en utilisant les boutons fléchés situés en bas du volet de **diffusion en cours** juste au-dessus du message d’État et des contrôles de transport.</span><span class="sxs-lookup"><span data-stu-id="7b748-119">The user can change the preset by selecting a different entry from the **Visualizations and Views** list on the **View** menu, or by using the arrow buttons provided at the bottom of the **Now Playing** pane just above the status message and transport controls.</span></span>

<span data-ttu-id="7b748-120">Les plug-ins d’interface utilisateur de fenêtre et d’arrière-plan peuvent être programmés pour accepter un élément multimédia ou une sélection que l’utilisateur lui envoie.</span><span class="sxs-lookup"><span data-stu-id="7b748-120">Background and separate window UI plug-ins can be programmed to accept a media item or playlist that the user sends to it.</span></span> <span data-ttu-id="7b748-121">Si un plug-in prend en charge cette fonctionnalité, son nom s’affiche dans la liste **Envoyer vers** disponible dans le menu contextuel du contrôle de sélection ou de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="7b748-121">If a plug-in supports this feature, its name will appear on the **Send to** list available from the shortcut menu of the playlist control or the library.</span></span>

<span data-ttu-id="7b748-122">Un plug-in d’interface utilisateur peut être programmé pour intercepter les raccourcis clavier lorsqu’il a le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="7b748-122">A UI plug-in can be programmed to intercept keyboard shortcuts when it has the keyboard focus.</span></span> <span data-ttu-id="7b748-123">Le focus clavier est nécessaire pour éviter les conflits lorsque plusieurs plug-ins d’interface utilisateur qui interceptent le même raccourci clavier sont chargés.</span><span class="sxs-lookup"><span data-stu-id="7b748-123">Keyboard focus is required to prevent conflicts when multiple UI plug-ins that intercept the same keyboard shortcut are loaded.</span></span> <span data-ttu-id="7b748-124">Bien que cela empêche les conflits, elle peut également entraîner des confusions pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="7b748-124">Although this prevents conflicts, it can also cause confusion to end users.</span></span> <span data-ttu-id="7b748-125">Pour cette raison, l’utilisation de raccourcis clavier avec les plug-ins de l’interface utilisateur n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="7b748-125">For this reason, the use of keyboard shortcuts with UI plug-ins is not recommended.</span></span> <span data-ttu-id="7b748-126">Toutefois, lorsqu’ils sont utilisés, ils ne doivent pas intercepter les raccourcis clavier utilisés par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7b748-126">When they are used, however, they should not intercept any keyboard shortcuts that are used by Windows Media Player.</span></span> <span data-ttu-id="7b748-127">Pour obtenir la liste complète des raccourcis clavier utilisés par le lecteur, consultez l’aide du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7b748-127">For a complete list of keyboard shortcuts used by the Player, see Windows Media Player Help.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b748-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b748-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b748-129">**Vue d’ensemble du plug-in d’interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="7b748-129">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




