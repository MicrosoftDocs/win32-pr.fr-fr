---
title: Architecture du gestionnaire de téléchargement
description: Architecture du gestionnaire de téléchargement
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
- architecture du gestionnaire de téléchargement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671906"
---
# <a name="download-manager-architecture"></a><span data-ttu-id="2adc7-110">Architecture du gestionnaire de téléchargement</span><span class="sxs-lookup"><span data-stu-id="2adc7-110">Download Manager Architecture</span></span>

<span data-ttu-id="2adc7-111">Le gestionnaire de téléchargement du lecteur Windows Media utilise la technologie COM.</span><span class="sxs-lookup"><span data-stu-id="2adc7-111">The Windows Media Player Download Manager uses COM technology.</span></span> <span data-ttu-id="2adc7-112">La fonctionnalité est divisée en un ensemble d’interfaces de programmation ; vous pouvez écrire du code de programmation qui utilise ces interfaces à l’aide de Microsoft JScript ou C++.</span><span class="sxs-lookup"><span data-stu-id="2adc7-112">The functionality is distilled into a set of programming interfaces; you can write programming code that uses these interfaces by using Microsoft JScript or C++.</span></span>

<span data-ttu-id="2adc7-113">Les langages de script utilisent le concept d’objets pour diviser les fonctionnalités de programmation.</span><span class="sxs-lookup"><span data-stu-id="2adc7-113">The scripting languages use the concept of objects to divide programming functionality.</span></span> <span data-ttu-id="2adc7-114">Le modèle objet **downloadmanager** utilise plusieurs objets pour diviser les méthodes et les propriétés en une organisation logique qui regroupe les fonctions sémantiquement associées.</span><span class="sxs-lookup"><span data-stu-id="2adc7-114">The **DownloadManager** object model uses several objects to divide the methods and properties into a logical organization that groups semantically related functions together.</span></span> <span data-ttu-id="2adc7-115">Les sections suivantes contiennent des informations sur les objets du gestionnaire de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2adc7-115">The following sections contain information about the Download Manager objects.</span></span>



| <span data-ttu-id="2adc7-116">Section</span><span class="sxs-lookup"><span data-stu-id="2adc7-116">Section</span></span>                                                                     | <span data-ttu-id="2adc7-117">Description</span><span class="sxs-lookup"><span data-stu-id="2adc7-117">Description</span></span>                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2adc7-118">À propos de l’objet DownloadManager</span><span class="sxs-lookup"><span data-stu-id="2adc7-118">About the DownloadManager Object</span></span>](#about-the-downloadmanager-object)       | <span data-ttu-id="2adc7-119">L’objet **downloadmanager** représente l’objet racine du gestionnaire de téléchargement du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2adc7-119">The **DownloadManager** object represents the root object for the Windows Media Player Download Manager.</span></span> |
| [<span data-ttu-id="2adc7-120">À propos de l’objet DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="2adc7-120">About the DownloadCollection Object</span></span>](#about-the-downloadcollection-object) | <span data-ttu-id="2adc7-121">L’objet **DownloadCollection** représente une collection d’éléments de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2adc7-121">The **DownloadCollection** object represents a collection of download items.</span></span>                             |
| [<span data-ttu-id="2adc7-122">À propos de l’objet DownloadItem</span><span class="sxs-lookup"><span data-stu-id="2adc7-122">About the DownloadItem Object</span></span>](#about-the-downloaditem-object)             | <span data-ttu-id="2adc7-123">L’objet **DownloadItem** représente une demande de téléchargement individuelle.</span><span class="sxs-lookup"><span data-stu-id="2adc7-123">The **DownloadItem** object represents an individual download request.</span></span>                                   |



 

## <a name="about-the-downloadmanager-object"></a><span data-ttu-id="2adc7-124">À propos de l’objet DownloadManager</span><span class="sxs-lookup"><span data-stu-id="2adc7-124">About the DownloadManager Object</span></span>

<span data-ttu-id="2adc7-125">**Downloadmanager** est l’objet racine du gestionnaire de téléchargement du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2adc7-125">**DownloadManager** is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="2adc7-126">Tous les autres objets sont accessibles par le biais de cet objet.</span><span class="sxs-lookup"><span data-stu-id="2adc7-126">All other objects are accessed through this object.</span></span> <span data-ttu-id="2adc7-127">Pour accéder à l’objet **downloadmanager** , utilisez la syntaxe JScript suivante :</span><span class="sxs-lookup"><span data-stu-id="2adc7-127">To gain access to the **DownloadManager** object, use the following JScript syntax:</span></span>


```C++
var DownloadManager = external.DownloadManager;
```



<span data-ttu-id="2adc7-128">Cela crée une instance de l’objet **downloadmanager** , qui peut ensuite être utilisée pour récupérer les objets enfants.</span><span class="sxs-lookup"><span data-stu-id="2adc7-128">This creates an instance of the **DownloadManager** object, which can then be used to retrieve the child objects.</span></span> <span data-ttu-id="2adc7-129">Par exemple, la syntaxe suivante récupère le premier élément de la collection de téléchargements portant le numéro d’ID 253675 :</span><span class="sxs-lookup"><span data-stu-id="2adc7-129">For example, the following syntax retrieves the first item from the download collection that has id number 253675:</span></span>


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a><span data-ttu-id="2adc7-130">À propos de l’objet DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="2adc7-130">About the DownloadCollection Object</span></span>

<span data-ttu-id="2adc7-131">L’objet **DownloadCollection** représente une collection de fichiers à télécharger.</span><span class="sxs-lookup"><span data-stu-id="2adc7-131">The **DownloadCollection** object represents a collection of files to be downloaded.</span></span> <span data-ttu-id="2adc7-132">Vous pouvez utiliser cet objet pour déterminer le nombre de téléchargements dans la collection, supprimer des éléments de la collection, récupérer un élément de téléchargement spécifique et démarrer un nouveau téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2adc7-132">You can use this object to determine how many downloads are in the collection, remove items from the collection, retrieve a specific download item, and to start a new download.</span></span> <span data-ttu-id="2adc7-133">Le démarrage d’un nouveau téléchargement ajoute automatiquement le téléchargement à la collection.</span><span class="sxs-lookup"><span data-stu-id="2adc7-133">Starting a new download automatically adds the download to the collection.</span></span>

## <a name="about-the-downloaditem-object"></a><span data-ttu-id="2adc7-134">À propos de l’objet DownloadItem</span><span class="sxs-lookup"><span data-stu-id="2adc7-134">About the DownloadItem Object</span></span>

<span data-ttu-id="2adc7-135">L’objet **DownloadItem** représente un téléchargement individuel.</span><span class="sxs-lookup"><span data-stu-id="2adc7-135">The **DownloadItem** object represents an individual download.</span></span> <span data-ttu-id="2adc7-136">Les éléments de téléchargement existent toujours dans le cadre d’une collection de téléchargements.</span><span class="sxs-lookup"><span data-stu-id="2adc7-136">Download items always exist as part of a download collection.</span></span> <span data-ttu-id="2adc7-137">Utilisez cet objet pour récupérer des informations sur l’élément de téléchargement et pour suspendre, reprendre ou annuler le téléchargement en cours.</span><span class="sxs-lookup"><span data-stu-id="2adc7-137">Use this object to retrieve information about the download item and to pause, resume, or cancel the download in progress.</span></span>

<span data-ttu-id="2adc7-138">Lorsque vous annulez un téléchargement, l’élément de téléchargement reste en place dans sa collection de téléchargements.</span><span class="sxs-lookup"><span data-stu-id="2adc7-138">When you cancel a download, the download item remains in place in its download collection.</span></span> <span data-ttu-id="2adc7-139">Dans ce cas, **downloadCollection**. **downloadState** récupère la valeur 4, ce qui signifie que l’opération a été annulée.</span><span class="sxs-lookup"><span data-stu-id="2adc7-139">In this case, **downloadCollection**.**downloadState** retrieves a value of 4, meaning canceled.</span></span>

<span data-ttu-id="2adc7-140">Vous pouvez utiliser **downloadItem**. **progression** pour informer l’utilisateur de la quantité de fichier qui a été transférée ou de la quantité restant à télécharger.</span><span class="sxs-lookup"><span data-stu-id="2adc7-140">You can use **downloadItem**.**progress** to inform the user about how much of the file has been transferred or how much remains to be downloaded.</span></span> <span data-ttu-id="2adc7-141">Vous pouvez utiliser cette valeur pour estimer également le temps restant.</span><span class="sxs-lookup"><span data-stu-id="2adc7-141">You might use this value to estimate the time remaining as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2adc7-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2adc7-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2adc7-143">**Gestionnaire de téléchargement**</span><span class="sxs-lookup"><span data-stu-id="2adc7-143">**Download Manager**</span></span>](download-manager.md)
</dt> </dl>

 

 




