---
title: DownloadCollection. removeItem, méthode
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode removeItem supprime un élément de téléchargement d’une collection de téléchargements.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- méthode removeItem lecteur Windows Media
- méthode removeItem lecteur Windows Media, classe DownloadCollection
- Classe DownloadCollection lecteur Windows Media, removeItem, méthode
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543962"
---
# <a name="downloadcollectionremoveitem-method"></a><span data-ttu-id="28b73-108">DownloadCollection. removeItem, méthode</span><span class="sxs-lookup"><span data-stu-id="28b73-108">DownloadCollection.removeItem method</span></span>

> [!Note]  
> <span data-ttu-id="28b73-109">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="28b73-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="28b73-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="28b73-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="28b73-111">La méthode **RemoveItem** supprime un élément de téléchargement d’une collection de téléchargements.</span><span class="sxs-lookup"><span data-stu-id="28b73-111">The **removeItem** method removes a download item from a download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="28b73-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28b73-112">Syntax</span></span>


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a><span data-ttu-id="28b73-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28b73-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28b73-114">*ItemId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28b73-114">*itemID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28b73-115">**Nombre** (**long**) spécifiant l’index du **DownloadItem** à supprimer.</span><span class="sxs-lookup"><span data-stu-id="28b73-115">**Number** (**long**) specifying the index of the **DownloadItem** to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28b73-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28b73-116">Return value</span></span>

<span data-ttu-id="28b73-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="28b73-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28b73-118">Notes</span><span class="sxs-lookup"><span data-stu-id="28b73-118">Remarks</span></span>

<span data-ttu-id="28b73-119">Si le téléchargement représenté par *ItemId* est en cours, cette méthode annule le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="28b73-119">If the download represented by *itemID* is in progress, this method cancels the download.</span></span>

## <a name="requirements"></a><span data-ttu-id="28b73-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28b73-120">Requirements</span></span>



| <span data-ttu-id="28b73-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28b73-121">Requirement</span></span> | <span data-ttu-id="28b73-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="28b73-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28b73-123">Version</span><span class="sxs-lookup"><span data-stu-id="28b73-123">Version</span></span><br/> | <span data-ttu-id="28b73-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="28b73-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="28b73-125">DLL</span><span class="sxs-lookup"><span data-stu-id="28b73-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="28b73-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28b73-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28b73-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28b73-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28b73-128">**DownloadCollection. Item**</span><span class="sxs-lookup"><span data-stu-id="28b73-128">**DownloadCollection.item**</span></span>](downloadcollection-item.md)
</dt> <dt>

[<span data-ttu-id="28b73-129">**Objet DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="28b73-129">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





