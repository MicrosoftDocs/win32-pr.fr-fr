---
title: Objet DownloadCollection
description: Objet DownloadCollection
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Windows Media Player Online stores, objet DownloadCollection
- magasins en ligne, objet DownloadCollection
- types 2 magasins en ligne, objet DownloadCollection
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511229"
---
# <a name="downloadcollection-object"></a><span data-ttu-id="4abbf-107">Objet DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="4abbf-107">DownloadCollection Object</span></span>

> [!Note]  
> <span data-ttu-id="4abbf-108">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="4abbf-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4abbf-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4abbf-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4abbf-110">L’objet **DownloadCollection** contient des propriétés et des méthodes pour gérer des collections d’éléments de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="4abbf-110">The **DownloadCollection** object contains properties and methods to handle collections of download items.</span></span> <span data-ttu-id="4abbf-111">Il peut être utilisé par les pages Web qui sont hébergées dans le lecteur Windows Media en mode complet et qui ont accès à l’objet **externe** , tel que les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="4abbf-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as online stores.</span></span>

<span data-ttu-id="4abbf-112">L’objet **DownloadCollection** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4abbf-112">The **DownloadCollection** object supports the following properties.</span></span>



| <span data-ttu-id="4abbf-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="4abbf-113">Property</span></span>                              | <span data-ttu-id="4abbf-114">Description</span><span class="sxs-lookup"><span data-stu-id="4abbf-114">Description</span></span>                                  |
|---------------------------------------|----------------------------------------------|
| [<span data-ttu-id="4abbf-115">count</span><span class="sxs-lookup"><span data-stu-id="4abbf-115">count</span></span>](downloadcollection-count.md) | <span data-ttu-id="4abbf-116">Récupère le nombre de téléchargements en attente.</span><span class="sxs-lookup"><span data-stu-id="4abbf-116">Retrieves the number of pending downloads.</span></span>   |
| [<span data-ttu-id="4abbf-117">id</span><span class="sxs-lookup"><span data-stu-id="4abbf-117">id</span></span>](downloadcollection-id.md)       | <span data-ttu-id="4abbf-118">Récupère l’ID de la collection de téléchargements.</span><span class="sxs-lookup"><span data-stu-id="4abbf-118">Retrieves the ID of the download collection.</span></span> |



 

<span data-ttu-id="4abbf-119">L’objet **DownloadCollection** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4abbf-119">The **DownloadCollection** object supports the following methods.</span></span>



| <span data-ttu-id="4abbf-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="4abbf-120">Method</span></span>                                                | <span data-ttu-id="4abbf-121">Description</span><span class="sxs-lookup"><span data-stu-id="4abbf-121">Description</span></span>                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="4abbf-122">Effacer</span><span class="sxs-lookup"><span data-stu-id="4abbf-122">Clear</span></span>](downloadcollection-clear.md)                 | <span data-ttu-id="4abbf-123">Supprime tous les éléments d’une collection de téléchargements.</span><span class="sxs-lookup"><span data-stu-id="4abbf-123">Removes all items from a download collection.</span></span> |
| [<span data-ttu-id="4abbf-124">item</span><span class="sxs-lookup"><span data-stu-id="4abbf-124">item</span></span>](downloadcollection-item.md)                   | <span data-ttu-id="4abbf-125">Récupère un objet de téléchargement en attente.</span><span class="sxs-lookup"><span data-stu-id="4abbf-125">Retrieves a pending download object.</span></span>          |
| [<span data-ttu-id="4abbf-126">removeItem</span><span class="sxs-lookup"><span data-stu-id="4abbf-126">removeItem</span></span>](downloadcollection-removeitem.md)       | <span data-ttu-id="4abbf-127">Supprime un élément de téléchargement d’une collection.</span><span class="sxs-lookup"><span data-stu-id="4abbf-127">Removes a download item from a collection.</span></span>    |
| [<span data-ttu-id="4abbf-128">startDownload</span><span class="sxs-lookup"><span data-stu-id="4abbf-128">startDownload</span></span>](downloadcollection-startdownload.md) | <span data-ttu-id="4abbf-129">Met en file d’attente un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="4abbf-129">Queues a download.</span></span>                            |



 

<span data-ttu-id="4abbf-130">L’objet **DownloadCollection** est accessible par le biais des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4abbf-130">The **DownloadCollection** object is accessed through the following methods.</span></span>



| <span data-ttu-id="4abbf-131">Object</span><span class="sxs-lookup"><span data-stu-id="4abbf-131">Object</span></span>                                        | <span data-ttu-id="4abbf-132">Méthode</span><span class="sxs-lookup"><span data-stu-id="4abbf-132">Method</span></span>                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="4abbf-133">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="4abbf-133">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="4abbf-134">createDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="4abbf-134">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) |
| [<span data-ttu-id="4abbf-135">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="4abbf-135">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="4abbf-136">getDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="4abbf-136">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       |



 

<span data-ttu-id="4abbf-137">À des fins d’illustration, **downloadmanager**. **getDownloadCollection**(*porte*) est utilisé dans les sections de syntaxe de référence.</span><span class="sxs-lookup"><span data-stu-id="4abbf-137">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4abbf-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4abbf-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4abbf-139">**Référence pour les magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="4abbf-139">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




