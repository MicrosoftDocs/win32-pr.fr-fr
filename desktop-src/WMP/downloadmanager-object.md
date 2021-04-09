---
title: Objet DownloadManager
description: Objet DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player Online stores, objet DownloadManager
- magasins en ligne, objet DownloadManager
- types 2 magasins en ligne, objet DownloadManager
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840230"
---
# <a name="downloadmanager-object"></a><span data-ttu-id="41694-107">Objet DownloadManager</span><span class="sxs-lookup"><span data-stu-id="41694-107">DownloadManager Object</span></span>

> [!Note]  
> <span data-ttu-id="41694-108">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="41694-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="41694-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="41694-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="41694-110">L’objet **downloadmanager** est l’objet racine du gestionnaire de téléchargement du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="41694-110">The **DownloadManager** object is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="41694-111">Il peut être utilisé par les pages Web qui sont hébergées dans les volets de tâches du service de magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="41694-111">It can be used by webpages that are hosted in online store service task panes.</span></span>

<span data-ttu-id="41694-112">L’objet **downloadmanager** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="41694-112">The **DownloadManager** object supports the following methods.</span></span>



| <span data-ttu-id="41694-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="41694-113">Method</span></span>                                                                   | <span data-ttu-id="41694-114">Description</span><span class="sxs-lookup"><span data-stu-id="41694-114">Description</span></span>                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="41694-115">createDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="41694-115">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) | <span data-ttu-id="41694-116">Crée une collection de téléchargements vide.</span><span class="sxs-lookup"><span data-stu-id="41694-116">Creates an empty download collection.</span></span>        |
| [<span data-ttu-id="41694-117">getDownloadCollection</span><span class="sxs-lookup"><span data-stu-id="41694-117">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       | <span data-ttu-id="41694-118">Récupère la collection de téléchargements spécifiée.</span><span class="sxs-lookup"><span data-stu-id="41694-118">Retrieves the specified download collection.</span></span> |



 

<span data-ttu-id="41694-119">L’objet **downloadmanager** est accessible à l’aide de l' **External. DownloadManager**.</span><span class="sxs-lookup"><span data-stu-id="41694-119">The **DownloadManager** object is accessed by using **external.DownloadManager**.</span></span> <span data-ttu-id="41694-120">À des fins d’illustration, il est supposé que cette valeur a été assignée à une variable nommée « DownloadManager », qui sera utilisée pour identifier cet objet dans les sections de syntaxe de référence.</span><span class="sxs-lookup"><span data-stu-id="41694-120">For illustration purposes, it is assumed that this value has been assigned to a variable named "DownloadManager", which will be used to identify this object in the reference syntax sections.</span></span>

<span data-ttu-id="41694-121">Dans le lecteur Windows Media 10 ou version ultérieure, la propriété et l’objet **downloadmanager** sont accessibles uniquement à partir des volets de tâches du service de magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="41694-121">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="41694-122">Vous ne pouvez pas utiliser **downloadmanager** à partir d’autres fonctionnalités où l’objet **externe** est disponible, par exemple HTMLView, le mode Info Center et les informations sur l’album.</span><span class="sxs-lookup"><span data-stu-id="41694-122">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41694-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41694-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41694-124">**Référence pour les magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="41694-124">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




