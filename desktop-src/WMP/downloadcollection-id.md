---
title: DownloadCollection.id
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété ID récupère l’ID de la collection de téléchargements.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- Lecteur Windows Media DownloadCollection.id
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541764"
---
# <a name="downloadcollectionid"></a><span data-ttu-id="bebad-106">DownloadCollection.id</span><span class="sxs-lookup"><span data-stu-id="bebad-106">DownloadCollection.id</span></span>

> [!Note]  
> <span data-ttu-id="bebad-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="bebad-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="bebad-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bebad-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="bebad-109">La propriété **ID** récupère l’ID de la collection de téléchargements.</span><span class="sxs-lookup"><span data-stu-id="bebad-109">The **id** property retrieves the ID of the download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bebad-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bebad-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a><span data-ttu-id="bebad-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="bebad-111">Possible Values</span></span>

<span data-ttu-id="bebad-112">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="bebad-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="bebad-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bebad-113">Remarks</span></span>

<span data-ttu-id="bebad-114">Lorsque le gestionnaire de téléchargement crée une collection de téléchargements, il attribue un numéro d’identification au regroupement.</span><span class="sxs-lookup"><span data-stu-id="bebad-114">When the Download Manager creates a new download collection, it assigns the collection an ID number.</span></span> <span data-ttu-id="bebad-115">Les numéros d’identification sont conservés entre les sessions du lecteur Windows Media et les sessions du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bebad-115">ID numbers persist between Windows Media Player sessions and operating system sessions.</span></span>

<span data-ttu-id="bebad-116">Les numéros d’ID ne sont pas uniques.</span><span class="sxs-lookup"><span data-stu-id="bebad-116">ID numbers are not unique.</span></span> <span data-ttu-id="bebad-117">Toutefois, il existe un nombre suffisant de numéros d’ID disponibles dans la valeur 32 bits, car il est très improbable qu’un numéro d’identification existant soit remplacé par un nouveau.</span><span class="sxs-lookup"><span data-stu-id="bebad-117">However, there are enough ID numbers available in the 32-bit value that it is extremely unlikely that an existing ID number will ever be overwritten by a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="bebad-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bebad-118">Requirements</span></span>



| <span data-ttu-id="bebad-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bebad-119">Requirement</span></span> | <span data-ttu-id="bebad-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bebad-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bebad-121">Version</span><span class="sxs-lookup"><span data-stu-id="bebad-121">Version</span></span><br/> | <span data-ttu-id="bebad-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bebad-122">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="bebad-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bebad-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="bebad-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bebad-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bebad-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bebad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bebad-126">**Objet DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="bebad-126">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





