---
title: DownloadItem.downloadState
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété downloadState récupère l’état du téléchargement.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- Lecteur Windows Media DownloadItem. downloadState
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540694"
---
# <a name="downloaditemdownloadstate"></a><span data-ttu-id="fad90-106">DownloadItem.downloadState</span><span class="sxs-lookup"><span data-stu-id="fad90-106">DownloadItem.downloadState</span></span>

> [!Note]  
> <span data-ttu-id="fad90-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="fad90-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="fad90-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fad90-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="fad90-109">La propriété **downloadState** récupère l’état du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="fad90-109">The **downloadState** property retrieves the state of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad90-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fad90-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a><span data-ttu-id="fad90-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="fad90-111">Possible Values</span></span>

<span data-ttu-id="fad90-112">Cette propriété est un **nombre** en lecture seule contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fad90-112">This property is a read-only **Number** containing one of the following values.</span></span>



| <span data-ttu-id="fad90-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="fad90-113">Value</span></span> | <span data-ttu-id="fad90-114">Description</span><span class="sxs-lookup"><span data-stu-id="fad90-114">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="fad90-115">0</span><span class="sxs-lookup"><span data-stu-id="fad90-115">0</span></span>     | <span data-ttu-id="fad90-116">Downloading</span><span class="sxs-lookup"><span data-stu-id="fad90-116">Downloading</span></span> |
| <span data-ttu-id="fad90-117">1</span><span class="sxs-lookup"><span data-stu-id="fad90-117">1</span></span>     | <span data-ttu-id="fad90-118">Suspendu</span><span class="sxs-lookup"><span data-stu-id="fad90-118">Paused</span></span>      |
| <span data-ttu-id="fad90-119">2</span><span class="sxs-lookup"><span data-stu-id="fad90-119">2</span></span>     | <span data-ttu-id="fad90-120">Traitement en cours</span><span class="sxs-lookup"><span data-stu-id="fad90-120">Processing</span></span>  |
| <span data-ttu-id="fad90-121">3</span><span class="sxs-lookup"><span data-stu-id="fad90-121">3</span></span>     | <span data-ttu-id="fad90-122">Effectué</span><span class="sxs-lookup"><span data-stu-id="fad90-122">Completed</span></span>   |
| <span data-ttu-id="fad90-123">4</span><span class="sxs-lookup"><span data-stu-id="fad90-123">4</span></span>     | <span data-ttu-id="fad90-124">Opération annulée</span><span class="sxs-lookup"><span data-stu-id="fad90-124">Canceled</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="fad90-125">Notes</span><span class="sxs-lookup"><span data-stu-id="fad90-125">Remarks</span></span>

<span data-ttu-id="fad90-126">Les États de téléchargement peuvent se produire dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="fad90-126">Download states can occur in any order.</span></span> <span data-ttu-id="fad90-127">N’écrivez pas de code qui dépend de l’occurrence d’un état de téléchargement particulier.</span><span class="sxs-lookup"><span data-stu-id="fad90-127">Do not write code that depends on the occurrence of any particular download state.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad90-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fad90-128">Requirements</span></span>



| <span data-ttu-id="fad90-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fad90-129">Requirement</span></span> | <span data-ttu-id="fad90-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="fad90-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fad90-131">Version</span><span class="sxs-lookup"><span data-stu-id="fad90-131">Version</span></span><br/> | <span data-ttu-id="fad90-132">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fad90-132">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="fad90-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fad90-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="fad90-134"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fad90-134"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad90-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fad90-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad90-136">**Objet DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="fad90-136">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





