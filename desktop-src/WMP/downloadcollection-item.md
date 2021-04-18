---
title: DownloadCollection. Item, méthode
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode Item récupère un objet de téléchargement en attente.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- méthode Item lecteur Windows Media
- méthode Item lecteur Windows Media, classe DownloadCollection
- Classe DownloadCollection lecteur Windows Media, méthode Item
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526816"
---
# <a name="downloadcollectionitem-method"></a><span data-ttu-id="9511c-108">DownloadCollection. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="9511c-108">DownloadCollection.item method</span></span>

> [!Note]  
> <span data-ttu-id="9511c-109">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="9511c-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9511c-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9511c-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9511c-111">La méthode **Item** récupère un objet de téléchargement en attente.</span><span class="sxs-lookup"><span data-stu-id="9511c-111">The **item** method retrieves a pending download object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9511c-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9511c-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a><span data-ttu-id="9511c-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9511c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9511c-114">*ItemId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9511c-114">*itemId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9511c-115">**Nombre** (**long**) spécifiant l’index du **DownloadItem** à récupérer.</span><span class="sxs-lookup"><span data-stu-id="9511c-115">**Number** (**long**) specifying the index of the **DownloadItem** to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9511c-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9511c-116">Return value</span></span>

<span data-ttu-id="9511c-117">Cette méthode retourne un objet **DownloadItem** .</span><span class="sxs-lookup"><span data-stu-id="9511c-117">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9511c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9511c-118">Remarks</span></span>

<span data-ttu-id="9511c-119">La valeur *ItemId* est de base zéro.</span><span class="sxs-lookup"><span data-stu-id="9511c-119">The *itemID* value is zero-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="9511c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9511c-120">Requirements</span></span>



| <span data-ttu-id="9511c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9511c-121">Requirement</span></span> | <span data-ttu-id="9511c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9511c-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9511c-123">Version</span><span class="sxs-lookup"><span data-stu-id="9511c-123">Version</span></span><br/> | <span data-ttu-id="9511c-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9511c-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="9511c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9511c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9511c-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9511c-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9511c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9511c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9511c-128">**Objet DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="9511c-128">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="9511c-129">**Objet DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="9511c-129">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





