---
title: Flow de contrôle
description: Flow de contrôle
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- visualisations, déroulement du programme
- visualisations personnalisées, déroulement du programme
- visualisations, Flow Control
- visualisations personnalisées, Flow Control
- visualisations, événements chronométrés
- visualisations personnalisées, événements chronométrés
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- visualisations, fonction RenderWindow
- visualisations personnalisées, fonction RenderWindow
- Fonction Render, déroulement du programme de visualisation
- RenderWindow fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939724"
---
# <a name="flow-of-control"></a><span data-ttu-id="beb0a-115">Flow de contrôle</span><span class="sxs-lookup"><span data-stu-id="beb0a-115">Flow of Control</span></span>

<span data-ttu-id="beb0a-116">Les données audio arrivent en permanence dans le lecteur Windows Media via un fichier ou un flux.</span><span class="sxs-lookup"><span data-stu-id="beb0a-116">Audio data comes into Windows Media Player continuously through a file or a stream.</span></span> <span data-ttu-id="beb0a-117">Ces données sont transmises à votre visualisation.</span><span class="sxs-lookup"><span data-stu-id="beb0a-117">That data is passed to your visualization.</span></span> <span data-ttu-id="beb0a-118">Vous dessinez sur une surface définie et repassez cette surface au lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="beb0a-118">You draw on a defined surface and pass that surface back to Windows Media Player.</span></span> <span data-ttu-id="beb0a-119">Cet échange se produit plusieurs fois par seconde et, pour l’utilisateur, le résultat est une animation agréable qui se déplace dans le temps jusqu’à la musique.</span><span class="sxs-lookup"><span data-stu-id="beb0a-119">This interchange happens several times a second, and to the user, the result is a pleasing animation that moves in time to the music.</span></span>

<span data-ttu-id="beb0a-120">Voici la séquence spécifique du déroulement du programme de visualisation :</span><span class="sxs-lookup"><span data-stu-id="beb0a-120">Here is the specific sequence of the visualization program flow:</span></span>

1.  <span data-ttu-id="beb0a-121">À un intervalle de temps, le lecteur Windows Media prend un instantané de l’audio qui est joué.</span><span class="sxs-lookup"><span data-stu-id="beb0a-121">At a timed interval, Windows Media Player takes a snapshot of the audio that is playing.</span></span>
2.  <span data-ttu-id="beb0a-122">Le lecteur Windows Media fournit les données de cet instantané à votre visualisation via la fonction **Render** et la fonction **RenderWindowed** .</span><span class="sxs-lookup"><span data-stu-id="beb0a-122">Windows Media Player supplies the data from that snapshot to your visualization through the **Render** function and the **RenderWindowed** function.</span></span>
3.  <span data-ttu-id="beb0a-123">Vous devez écrire du code qui s’exécutera lors de l’appel de **Render** et **RenderWindowed** .</span><span class="sxs-lookup"><span data-stu-id="beb0a-123">You must write code that will run when **Render** and **RenderWindowed** is called.</span></span> <span data-ttu-id="beb0a-124">Votre code dessine à l’aide d’un contexte de périphérique défini par le lecteur Windows Media lors du rendu sans fenêtre, ou à l’aide d’une fenêtre que vous créez lors du rendu de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="beb0a-124">Your code draws by using a device context defined by Windows Media Player when rendering windowless, or by using a window that you create when rendering windowed.</span></span>
4.  <span data-ttu-id="beb0a-125">Dans une région spécifiée par l’apparence actuelle, le lecteur Windows Media affiche ce que votre code a dessiné.</span><span class="sxs-lookup"><span data-stu-id="beb0a-125">In a region specified by the current skin, Windows Media Player displays what your code drew.</span></span>
5.  <span data-ttu-id="beb0a-126">Ce processus se répète plusieurs fois par seconde, créant ainsi des animations graphiques chronométrées à la musique.</span><span class="sxs-lookup"><span data-stu-id="beb0a-126">This process repeats several times a second, creating graphical animations that are timed to the music.</span></span> <span data-ttu-id="beb0a-127">Lorsque la musique s’arrête, la visualisation s’arrête.</span><span class="sxs-lookup"><span data-stu-id="beb0a-127">When the music stops playing, the visualization stops.</span></span>

## <a name="related-topics"></a><span data-ttu-id="beb0a-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="beb0a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beb0a-129">**Vue d’ensemble du développeur**</span><span class="sxs-lookup"><span data-stu-id="beb0a-129">**Developer Overview**</span></span>](developer-overview.md)
</dt> </dl>

 

 




