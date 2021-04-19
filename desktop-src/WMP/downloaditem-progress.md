---
title: DownloadItem. Progress
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété Progress récupère la progression du téléchargement en octets.
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- DownloadItem. Progress lecteur Windows Media
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535919"
---
# <a name="downloaditemprogress"></a><span data-ttu-id="272f8-106">DownloadItem. Progress</span><span class="sxs-lookup"><span data-stu-id="272f8-106">DownloadItem.progress</span></span>

> [!Note]  
> <span data-ttu-id="272f8-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="272f8-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="272f8-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="272f8-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="272f8-109">La propriété **Progress** récupère la progression du téléchargement en octets.</span><span class="sxs-lookup"><span data-stu-id="272f8-109">The **progress** property retrieves the progress of the download in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="272f8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="272f8-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
```

## <a name="possible-values"></a><span data-ttu-id="272f8-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="272f8-111">Possible Values</span></span>

<span data-ttu-id="272f8-112">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="272f8-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="272f8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="272f8-113">Requirements</span></span>



| <span data-ttu-id="272f8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="272f8-114">Requirement</span></span> | <span data-ttu-id="272f8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="272f8-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="272f8-116">Version</span><span class="sxs-lookup"><span data-stu-id="272f8-116">Version</span></span><br/> | <span data-ttu-id="272f8-117">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="272f8-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="272f8-118">DLL</span><span class="sxs-lookup"><span data-stu-id="272f8-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="272f8-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="272f8-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="272f8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="272f8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="272f8-121">**Objet DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="272f8-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="272f8-122">**DownloadItem. Size**</span><span class="sxs-lookup"><span data-stu-id="272f8-122">**DownloadItem.size**</span></span>](downloaditem-size.md)
</dt> </dl>

 

 





