---
title: DownloadCollection. Count
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété Count récupère le nombre de téléchargements en attente dans la collection.
ms.assetid: 8f9245aa-6d92-4dd3-9b45-97ee37de680d
keywords:
- DownloadCollection. Count lecteur Windows Media
topic_type:
- apiref
api_name:
- DownloadCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95f161143cf599dcfbc71b2e55764009ec5d4e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525413"
---
# <a name="downloadcollectioncount"></a><span data-ttu-id="c0a02-106">DownloadCollection. Count</span><span class="sxs-lookup"><span data-stu-id="c0a02-106">DownloadCollection.count</span></span>

> [!Note]  
> <span data-ttu-id="c0a02-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="c0a02-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c0a02-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c0a02-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c0a02-109">La propriété **Count** récupère le nombre de téléchargements en attente dans la collection.</span><span class="sxs-lookup"><span data-stu-id="c0a02-109">The **count** property retrieves the number of pending downloads in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0a02-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0a02-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).count
      
```

## <a name="possible-values"></a><span data-ttu-id="c0a02-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c0a02-111">Possible Values</span></span>

<span data-ttu-id="c0a02-112">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="c0a02-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a02-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0a02-113">Requirements</span></span>



| <span data-ttu-id="c0a02-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0a02-114">Requirement</span></span> | <span data-ttu-id="c0a02-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0a02-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a02-116">Version</span><span class="sxs-lookup"><span data-stu-id="c0a02-116">Version</span></span><br/> | <span data-ttu-id="c0a02-117">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c0a02-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="c0a02-118">DLL</span><span class="sxs-lookup"><span data-stu-id="c0a02-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="c0a02-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0a02-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0a02-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0a02-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a02-121">**Objet DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="c0a02-121">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





