---
title: Vue d’ensemble du plug-in d’interface utilisateur
description: Vue d’ensemble du plug-in d’interface utilisateur
ms.assetid: 8c4feb56-31c0-4f69-98dd-3c203941bb4c
keywords:
- Lecteur Windows Media, plug-ins
- Lecteur Windows Media, plug-ins d’interface utilisateur
- Plug-ins du lecteur Windows Media, interface utilisateur
- plug-ins, interface utilisateur
- plug-ins d’interface utilisateur, à propos de
- Plug-ins d’interface utilisateur, à propos de
- plug-ins d’interface utilisateur, types
- Plug-ins d’interface utilisateur, types
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5228c9ab7ff97c9f0d03b1b8d1320d303b178e56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309534"
---
# <a name="ui-plug-in-overview"></a><span data-ttu-id="641e1-111">Vue d’ensemble du plug-in d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="641e1-111">UI Plug-in Overview</span></span>

<span data-ttu-id="641e1-112">Les plug-ins d’interface utilisateur peuvent être installés, désinstallés et configurés à l’aide de l’onglet Plug-ins de la boîte de dialogue Options du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="641e1-112">UI plug-ins can be installed, uninstalled, and configured using the Plug-ins tab of the Options dialog in Windows Media Player.</span></span>

<span data-ttu-id="641e1-113">Il existe cinq types de plug-ins d’interface utilisateur pris en charge par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="641e1-113">There are five types of UI plug-ins supported by Windows Media Player.</span></span> <span data-ttu-id="641e1-114">Trois de ces types correspondent à différentes zones du volet de **lecture** en cours du mode complet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="641e1-114">Three of these types correspond to different areas of the **Now Playing** pane of the full mode of the player.</span></span> <span data-ttu-id="641e1-115">Les deux autres types sont pour les plug-ins qui s’affichent dans une fenêtre distincte et pour les plug-ins qui n’ont pas d’affichage (à l’exception d’une page de propriétés).</span><span class="sxs-lookup"><span data-stu-id="641e1-115">The other two types are for plug-ins that display in a separate window and for plug-ins that have no display (except perhaps a property page).</span></span>

<span data-ttu-id="641e1-116">Les plug-ins d’interface utilisateur sont déchargés lorsqu’ils sont fermés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="641e1-116">UI plug-ins are unloaded when they are closed or disabled.</span></span> <span data-ttu-id="641e1-117">Les plug-ins d’interface utilisateur qui s’affichent dans le volet en **cours** de création sont également déchargés lorsque l’utilisateur choisit un autre plug-in du même type ou bascule en dehors du volet de **diffusion en cours** .</span><span class="sxs-lookup"><span data-stu-id="641e1-117">UI plug-ins that appear in the **Now Playing** pane are also unloaded when the user chooses another plug-in of the same type or switches out of the **Now Playing** pane.</span></span> <span data-ttu-id="641e1-118">Lorsque l’utilisateur bascule en mode apparence, tous les plug-ins restent chargés, mais ils ne sont pas affichés.</span><span class="sxs-lookup"><span data-stu-id="641e1-118">When the user switches to skin mode, all plug-ins remain loaded, but are not displayed.</span></span> <span data-ttu-id="641e1-119">Si des plug-ins de fenêtre ou d’arrière-plan distincts sont en cours d’exécution au moment de la fermeture du lecteur Windows Media, ils seront automatiquement rechargés au prochain démarrage du lecteur.</span><span class="sxs-lookup"><span data-stu-id="641e1-119">If separate window or background plug-ins are running when Windows Media Player is closed, they will be automatically reloaded the next time the player is started.</span></span>

<span data-ttu-id="641e1-120">Les sections suivantes fournissent des informations générales sur les plug-ins de l’interface utilisateur du lecteur Windows Media :</span><span class="sxs-lookup"><span data-stu-id="641e1-120">The following sections provide general information about Windows Media Player UI plug-ins:</span></span>

-   [<span data-ttu-id="641e1-121">Plug-ins de zone d’affichage (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="641e1-121">Display Area Plug-ins (deprecated)</span></span>](display-area-plug-ins--deprecated.md)
-   [<span data-ttu-id="641e1-122">Plug-ins de zone Paramètres</span><span class="sxs-lookup"><span data-stu-id="641e1-122">Settings Area Plug-ins</span></span>](settings-area-plug-ins.md)
-   [<span data-ttu-id="641e1-123">Plug-ins de zone de métadonnées (déconseillés)</span><span class="sxs-lookup"><span data-stu-id="641e1-123">Metadata Area Plug-ins (deprecated)</span></span>](metadata-area-plug-ins--deprecated.md)
-   [<span data-ttu-id="641e1-124">Plug-ins de fenêtre distincts</span><span class="sxs-lookup"><span data-stu-id="641e1-124">Separate Window Plug-ins</span></span>](separate-window-plug-ins.md)
-   [<span data-ttu-id="641e1-125">Plug-ins d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="641e1-125">Background Plug-ins</span></span>](background-plug-ins.md)
-   [<span data-ttu-id="641e1-126">Options du plug-in d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="641e1-126">UI Plug-in Options</span></span>](ui-plug-in-options.md)
-   [<span data-ttu-id="641e1-127">Affichage des interfaces utilisateur modales</span><span class="sxs-lookup"><span data-stu-id="641e1-127">Displaying Modal User Interfaces</span></span>](displaying-modal-user-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="641e1-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="641e1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="641e1-129">**À propos des plug-ins d’interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="641e1-129">**About User Interface Plug-ins**</span></span>](about-user-interface-plug-ins.md)
</dt> </dl>

 

 




