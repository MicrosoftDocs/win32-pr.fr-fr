---
title: DownloadItem. Cancel, méthode
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode Cancel annule le téléchargement.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- méthode Cancel Windows Media Player
- méthode Cancel lecteur Windows Media, classe DownloadItem
- Classe DownloadItem lecteur Windows Media, méthode Cancel
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c14d538e85d0930a43db883e226c007bea70de24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545603"
---
# <a name="downloaditemcancel-method"></a><span data-ttu-id="1a4e7-108">DownloadItem. Cancel, méthode</span><span class="sxs-lookup"><span data-stu-id="1a4e7-108">DownloadItem.cancel method</span></span>

> [!Note]  
> <span data-ttu-id="1a4e7-109">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="1a4e7-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1a4e7-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1a4e7-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1a4e7-111">La méthode **Cancel** annule le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="1a4e7-111">The **cancel** method cancels the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a4e7-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a4e7-112">Syntax</span></span>


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a><span data-ttu-id="1a4e7-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a4e7-113">Parameters</span></span>

<span data-ttu-id="1a4e7-114">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1a4e7-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a4e7-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a4e7-115">Return value</span></span>

<span data-ttu-id="1a4e7-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1a4e7-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a4e7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1a4e7-117">Remarks</span></span>

<span data-ttu-id="1a4e7-118">Les éléments annulés ne sont pas supprimés de la collection de téléchargements.</span><span class="sxs-lookup"><span data-stu-id="1a4e7-118">Cancelled items are not removed from the download collection.</span></span> <span data-ttu-id="1a4e7-119">Les éléments annulés retournent une valeur **downloadState** de 4 (annulée).</span><span class="sxs-lookup"><span data-stu-id="1a4e7-119">Cancelled items return a **downloadState** value of 4 (canceled).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a4e7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a4e7-120">Requirements</span></span>



| <span data-ttu-id="1a4e7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a4e7-121">Requirement</span></span> | <span data-ttu-id="1a4e7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a4e7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4e7-123">Version</span><span class="sxs-lookup"><span data-stu-id="1a4e7-123">Version</span></span><br/> | <span data-ttu-id="1a4e7-124">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1a4e7-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="1a4e7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1a4e7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a4e7-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a4e7-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a4e7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a4e7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a4e7-128">**Objet DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="1a4e7-128">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="1a4e7-129">**DownloadItem.downloadState**</span><span class="sxs-lookup"><span data-stu-id="1a4e7-129">**DownloadItem.downloadState**</span></span>](downloaditem-downloadstate.md)
</dt> </dl>

 

 





