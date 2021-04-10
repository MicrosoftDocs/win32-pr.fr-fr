---
title: Initialisation de la page
description: Initialisation de la page
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Windows Media Player Online stores, initialisation des pages
- magasins en ligne, initialiser des pages
- type 2 magasins en ligne, initialisation des pages
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
- initialisation des pages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197076"
---
# <a name="initializing-the-page"></a><span data-ttu-id="28d5e-113">Initialisation de la page</span><span class="sxs-lookup"><span data-stu-id="28d5e-113">Initializing the Page</span></span>

<span data-ttu-id="28d5e-114">Lors du chargement de la page Web, la fonction **init** s’exécute.</span><span class="sxs-lookup"><span data-stu-id="28d5e-114">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="28d5e-115">Ce code extrait tout d’abord toutes les données stockées dans une session précédente.</span><span class="sxs-lookup"><span data-stu-id="28d5e-115">This code first retrieves any data stored in a previous session.</span></span> <span data-ttu-id="28d5e-116">Pour plus d’informations, consultez [mise à jour des informations de session](maintaining-session-information.md).</span><span class="sxs-lookup"><span data-stu-id="28d5e-116">For details, see [Maintaining Session Information](maintaining-session-information.md).</span></span> <span data-ttu-id="28d5e-117">Il crée ensuite l’objet **downloadmanager** et le stocke dans la variable globale nommée g \_ oManager.</span><span class="sxs-lookup"><span data-stu-id="28d5e-117">It then creates the **DownloadManager** object and stores it in the global variable named g\_oManager.</span></span>


```C++
g_oManager = external.DownloadManager;

```



<span data-ttu-id="28d5e-118">Ensuite, la fonction connecte l’événement **OnColorChange** à la fonction nommée **OnAppColor** , puis appelle la fonction directement pour initialiser la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="28d5e-118">Next, the function connects the **OnColorChange** event to the function named **OnAppColor** and then calls the function directly to initialize the background color.</span></span> <span data-ttu-id="28d5e-119">Consultez [la page correspondance des couleurs du lecteur Windows Media](matching-the-windows-media-player-colors.md).</span><span class="sxs-lookup"><span data-stu-id="28d5e-119">See [Matching the Windows Media Player Colors](matching-the-windows-media-player-colors.md).</span></span>

<span data-ttu-id="28d5e-120">Enfin, la fonction démarre un minuteur avec un intervalle d’une seconde et initialise les zones de liste qui affichent les collections téléchargées en attente et les éléments téléchargés.</span><span class="sxs-lookup"><span data-stu-id="28d5e-120">Finally, the function starts a timer with a one-second interval and initializes the list boxes that display the pending download collections and download items.</span></span> <span data-ttu-id="28d5e-121">Cela est important, car il peut y avoir des sessions en cours la dernière fois que le magasin en ligne est fermé et que ces informations doivent être de nouveau affichées.</span><span class="sxs-lookup"><span data-stu-id="28d5e-121">This is important because there may have been sessions in progress the last time the online store closed and this information needs to be displayed again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28d5e-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28d5e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28d5e-123">**Utilisation du gestionnaire de téléchargement**</span><span class="sxs-lookup"><span data-stu-id="28d5e-123">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




