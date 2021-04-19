---
title: Objet DownloadItem
description: Objet DownloadItem
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player Online stores, objet DownloadItem
- magasins en ligne, objet DownloadItem
- types 2 magasins en ligne, objet DownloadItem
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512471"
---
# <a name="downloaditem-object"></a><span data-ttu-id="2c405-107">Objet DownloadItem</span><span class="sxs-lookup"><span data-stu-id="2c405-107">DownloadItem Object</span></span>

> [!Note]  
> <span data-ttu-id="2c405-108">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="2c405-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2c405-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2c405-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2c405-110">L’objet **DownloadItem** représente une demande de téléchargement de fichier.</span><span class="sxs-lookup"><span data-stu-id="2c405-110">The **DownloadItem** object represents a file download request.</span></span> <span data-ttu-id="2c405-111">Il peut être utilisé par les pages Web qui sont hébergées dans le lecteur Windows Media en mode complet et qui ont accès à l’objet **externe** , tel que les services Premium.</span><span class="sxs-lookup"><span data-stu-id="2c405-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as premium services.</span></span>

<span data-ttu-id="2c405-112">L’objet **DownloadItem** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2c405-112">The **DownloadItem** object supports the following properties.</span></span>



| <span data-ttu-id="2c405-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="2c405-113">Property</span></span>                                        | <span data-ttu-id="2c405-114">Description</span><span class="sxs-lookup"><span data-stu-id="2c405-114">Description</span></span>                                      |
|-------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="2c405-115">downloadState</span><span class="sxs-lookup"><span data-stu-id="2c405-115">downloadState</span></span>](downloaditem-downloadstate.md) | <span data-ttu-id="2c405-116">Récupère l’état du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2c405-116">Retrieves the state of the download.</span></span>             |
| [<span data-ttu-id="2c405-117">avancement</span><span class="sxs-lookup"><span data-stu-id="2c405-117">progress</span></span>](downloaditem-progress.md)           | <span data-ttu-id="2c405-118">Récupère la progression du téléchargement en octets.</span><span class="sxs-lookup"><span data-stu-id="2c405-118">Retrieves the progress of the download in bytes.</span></span> |
| [<span data-ttu-id="2c405-119">size</span><span class="sxs-lookup"><span data-stu-id="2c405-119">size</span></span>](downloaditem-size.md)                   | <span data-ttu-id="2c405-120">Récupère la taille du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2c405-120">Retrieves the size of the download.</span></span>              |
| [<span data-ttu-id="2c405-121">sourceURL</span><span class="sxs-lookup"><span data-stu-id="2c405-121">sourceURL</span></span>](downloaditem-sourceurl.md)         | <span data-ttu-id="2c405-122">Récupère l’URL source du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2c405-122">Retrieves the source URL of the download.</span></span>        |
| [<span data-ttu-id="2c405-123">type</span><span class="sxs-lookup"><span data-stu-id="2c405-123">type</span></span>](downloaditem-type.md)                   | <span data-ttu-id="2c405-124">Récupère le type du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2c405-124">Retrieves the type of the download.</span></span>              |



 

<span data-ttu-id="2c405-125">L’objet **DownloadItem** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="2c405-125">The **DownloadItem** object supports the following methods.</span></span>



| <span data-ttu-id="2c405-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="2c405-126">Method</span></span>                                      | <span data-ttu-id="2c405-127">Description</span><span class="sxs-lookup"><span data-stu-id="2c405-127">Description</span></span>                                                |
|---------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="2c405-128">cancel</span><span class="sxs-lookup"><span data-stu-id="2c405-128">cancel</span></span>](downloaditem-cancel.md)           | <span data-ttu-id="2c405-129">Annule le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2c405-129">Cancels the download.</span></span>                                      |
| [<span data-ttu-id="2c405-130">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="2c405-130">getItemInfo</span></span>](downloaditem-getiteminfo.md) | <span data-ttu-id="2c405-131">Récupère la valeur d’un attribut pour l’élément de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2c405-131">Retrieves the value of an attribute for the download item.</span></span> |
| [<span data-ttu-id="2c405-132">pause</span><span class="sxs-lookup"><span data-stu-id="2c405-132">pause</span></span>](downloaditem-pause.md)             | <span data-ttu-id="2c405-133">Interrompt le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2c405-133">Pauses the download.</span></span>                                       |
| [<span data-ttu-id="2c405-134">sort</span><span class="sxs-lookup"><span data-stu-id="2c405-134">resume</span></span>](downloaditem-resume.md)           | <span data-ttu-id="2c405-135">Reprend le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2c405-135">Resumes the download.</span></span>                                      |



 

<span data-ttu-id="2c405-136">L’objet **DownloadItem** est accessible par le biais de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="2c405-136">The **DownloadItem** object is accessed through the following property.</span></span>



| <span data-ttu-id="2c405-137">Object</span><span class="sxs-lookup"><span data-stu-id="2c405-137">Object</span></span>                                              | <span data-ttu-id="2c405-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="2c405-138">Property</span></span>                            |
|-----------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="2c405-139">DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="2c405-139">DownloadCollection</span></span>](downloadcollection-object.md) | [<span data-ttu-id="2c405-140">item</span><span class="sxs-lookup"><span data-stu-id="2c405-140">item</span></span>](downloadcollection-item.md) |



 

<span data-ttu-id="2c405-141">À des fins d’illustration, **downloadmanager**. **getDownloadCollection**(*le* biais). **Item**(*ItemId*) est utilisé dans les sections de syntaxe de référence.</span><span class="sxs-lookup"><span data-stu-id="2c405-141">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*).**item**(*itemId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c405-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c405-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c405-143">**Référence pour les magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="2c405-143">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




