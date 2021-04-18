---
title: External. addToBasket, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. addToBasket, méthode
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- méthode addToBasket lecteur Windows Media
- méthode addToBasket lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode addToBasket
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540551"
---
# <a name="externaladdtobasket-method"></a><span data-ttu-id="317c9-107">External. addToBasket, méthode</span><span class="sxs-lookup"><span data-stu-id="317c9-107">External.addToBasket method</span></span>

> [!Note]  
> <span data-ttu-id="317c9-108">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="317c9-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="317c9-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="317c9-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="317c9-110">La méthode **addToBasket** ajoute des éléments multimédias au volet Liste (également appelé panier) dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="317c9-110">The **addToBasket** method adds media items to the list pane (also called the basket) in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="317c9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="317c9-111">Syntax</span></span>


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="317c9-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="317c9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="317c9-113">*ViewType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="317c9-113">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="317c9-114">**Chaîne** qui spécifie le type d’élément ajouté au volet liste.</span><span class="sxs-lookup"><span data-stu-id="317c9-114">**String** that specifies the type of item being added to the list pane.</span></span> <span data-ttu-id="317c9-115">L’appelant doit définir ce paramètre sur l’une des [constantes d’emplacement de bibliothèque](library-location-constants.md)suivantes :</span><span class="sxs-lookup"><span data-stu-id="317c9-115">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="317c9-116">CPListID</span><span class="sxs-lookup"><span data-stu-id="317c9-116">CPListID</span></span>

<span data-ttu-id="317c9-117">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="317c9-117">CPTrackID</span></span>

<span data-ttu-id="317c9-118">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="317c9-118">CPAlbumID</span></span>

<span data-ttu-id="317c9-119">CPArtist</span><span class="sxs-lookup"><span data-stu-id="317c9-119">CPArtist</span></span>

<span data-ttu-id="317c9-120">CPGenreID</span><span class="sxs-lookup"><span data-stu-id="317c9-120">CPGenreID</span></span>

<span data-ttu-id="317c9-121">CPAlbumSubGenreID</span><span class="sxs-lookup"><span data-stu-id="317c9-121">CPAlbumSubGenreID</span></span>

<span data-ttu-id="317c9-122">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="317c9-122">CPRadioID</span></span>

</dd> <dt>

<span data-ttu-id="317c9-123">*ViewIDs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="317c9-123">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="317c9-124">**Chaîne** contenant les ID, délimités par des points-virgules, des éléments à ajouter au volet de liste.</span><span class="sxs-lookup"><span data-stu-id="317c9-124">**String** containing the IDs, delimited by semicolons, of the items to be added to the list pane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="317c9-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="317c9-125">Return value</span></span>

<span data-ttu-id="317c9-126">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="317c9-126">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="317c9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="317c9-127">Requirements</span></span>



| <span data-ttu-id="317c9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="317c9-128">Requirement</span></span> | <span data-ttu-id="317c9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="317c9-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="317c9-130">Version</span><span class="sxs-lookup"><span data-stu-id="317c9-130">Version</span></span><br/> | <span data-ttu-id="317c9-131">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="317c9-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="317c9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="317c9-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="317c9-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="317c9-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="317c9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="317c9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="317c9-135">**ExternalObject pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="317c9-135">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="317c9-136">**External. basketTitle**</span><span class="sxs-lookup"><span data-stu-id="317c9-136">**External.basketTitle**</span></span>](external-baskettitle.md)
</dt> </dl>

 

 





