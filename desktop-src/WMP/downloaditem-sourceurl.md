---
title: DownloadItem.sourceURL
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété sourceURL récupère l’URL source du téléchargement.
ms.assetid: 87af20a5-5721-498d-8417-3e7dbbec38a2
keywords:
- Lecteur Windows Media DownloadItem. sourceURL
topic_type:
- apiref
api_name:
- DownloadItem.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1670fb4fec0ff4adb68269cf6fe6bb39be248e01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525441"
---
# <a name="downloaditemsourceurl"></a><span data-ttu-id="41c82-106">DownloadItem.sourceURL</span><span class="sxs-lookup"><span data-stu-id="41c82-106">DownloadItem.sourceURL</span></span>

> [!Note]  
> <span data-ttu-id="41c82-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="41c82-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="41c82-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="41c82-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="41c82-109">La propriété **sourceURL** récupère l’URL source du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="41c82-109">The **sourceURL** property retrieves the source URL of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c82-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41c82-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).sourceURL
      
```

## <a name="possible-values"></a><span data-ttu-id="41c82-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="41c82-111">Possible Values</span></span>

<span data-ttu-id="41c82-112">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="41c82-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="41c82-113">Notes</span><span class="sxs-lookup"><span data-stu-id="41c82-113">Remarks</span></span>

<span data-ttu-id="41c82-114">Seuls les formats multimédias numériques suivants peuvent être téléchargés :</span><span class="sxs-lookup"><span data-stu-id="41c82-114">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="41c82-115">ASF (Advanced Systems Format)</span><span class="sxs-lookup"><span data-stu-id="41c82-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="41c82-116">MP3</span><span class="sxs-lookup"><span data-stu-id="41c82-116">MP3</span></span>
-   <span data-ttu-id="41c82-117">Audio Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="41c82-117">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="41c82-118">Vidéo Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="41c82-118">Windows Media Video (WMV)</span></span>

## <a name="requirements"></a><span data-ttu-id="41c82-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41c82-119">Requirements</span></span>



| <span data-ttu-id="41c82-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41c82-120">Requirement</span></span> | <span data-ttu-id="41c82-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="41c82-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41c82-122">Version</span><span class="sxs-lookup"><span data-stu-id="41c82-122">Version</span></span><br/> | <span data-ttu-id="41c82-123">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="41c82-123">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="41c82-124">DLL</span><span class="sxs-lookup"><span data-stu-id="41c82-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="41c82-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c82-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c82-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41c82-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c82-127">**Objet DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="41c82-127">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





