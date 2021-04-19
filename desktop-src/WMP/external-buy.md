---
title: External. Buy, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode Buy lance l’achat d’un ensemble d’éléments multimédias.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- méthode Buy lecteur Windows Media
- méthode Buy lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode Buy
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545509"
---
# <a name="externalbuy-method"></a><span data-ttu-id="4c7bb-108">External. Buy, méthode</span><span class="sxs-lookup"><span data-stu-id="4c7bb-108">External.buy method</span></span>

> [!Note]  
> <span data-ttu-id="4c7bb-109">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="4c7bb-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4c7bb-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4c7bb-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4c7bb-111">La méthode **Buy** lance l’achat d’un ensemble d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="4c7bb-111">The **buy** method initiates the purchase of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c7bb-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c7bb-112">Syntax</span></span>


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="4c7bb-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c7bb-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c7bb-114">*ViewType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c7bb-114">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c7bb-115">**Chaîne** qui spécifie le type d’élément à acheter.</span><span class="sxs-lookup"><span data-stu-id="4c7bb-115">**String** that specifies the type of item to be purchased.</span></span> <span data-ttu-id="4c7bb-116">L’appelant doit définir ce paramètre sur l’une des [constantes d’emplacement de bibliothèque](library-location-constants.md)suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c7bb-116">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="4c7bb-117">CPListID</span><span class="sxs-lookup"><span data-stu-id="4c7bb-117">CPListID</span></span>

<span data-ttu-id="4c7bb-118">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="4c7bb-118">CPTrackID</span></span>

<span data-ttu-id="4c7bb-119">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="4c7bb-119">CPAlbumID</span></span>

</dd> <dt>

<span data-ttu-id="4c7bb-120">*ViewIDs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c7bb-120">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c7bb-121">**Chaîne** contenant les ID, délimités par des points-virgules, des éléments à acheter.</span><span class="sxs-lookup"><span data-stu-id="4c7bb-121">**String** containing the IDs, delimited by semicolons, of the items to be purchased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c7bb-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c7bb-122">Return value</span></span>

<span data-ttu-id="4c7bb-123">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4c7bb-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7bb-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c7bb-124">Requirements</span></span>



| <span data-ttu-id="4c7bb-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c7bb-125">Requirement</span></span> | <span data-ttu-id="4c7bb-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c7bb-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7bb-127">Version</span><span class="sxs-lookup"><span data-stu-id="4c7bb-127">Version</span></span><br/> | <span data-ttu-id="4c7bb-128">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="4c7bb-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="4c7bb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4c7bb-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="4c7bb-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c7bb-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c7bb-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c7bb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c7bb-132">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="4c7bb-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4c7bb-133">**External. Download**</span><span class="sxs-lookup"><span data-stu-id="4c7bb-133">**External.download**</span></span>](external-download.md)
</dt> <dt>

[<span data-ttu-id="4c7bb-134">**IWMPContentPartner :: Buy**</span><span class="sxs-lookup"><span data-stu-id="4c7bb-134">**IWMPContentPartner::Buy**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[<span data-ttu-id="4c7bb-135">**Achat de contenu multimédia**</span><span class="sxs-lookup"><span data-stu-id="4c7bb-135">**Purchasing Media Content**</span></span>](purchasing-media-content.md)
</dt> </dl>

 

 





