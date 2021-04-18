---
title: External. Download, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode Download lance le téléchargement d’un ensemble d’éléments multimédias.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- Télécharger la méthode lecteur Windows Media
- méthode de téléchargement lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode de téléchargement
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532726"
---
# <a name="externaldownload-method"></a><span data-ttu-id="4c214-108">External. Download, méthode</span><span class="sxs-lookup"><span data-stu-id="4c214-108">External.download method</span></span>

> [!Note]  
> <span data-ttu-id="4c214-109">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="4c214-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4c214-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4c214-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4c214-111">La méthode **Download** lance le téléchargement d’un ensemble d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="4c214-111">The **download** method initiates the download of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c214-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c214-112">Syntax</span></span>


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a><span data-ttu-id="4c214-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c214-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c214-114">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c214-114">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c214-115">[Constante d’emplacement de bibliothèque](library-location-constants.md) qui spécifie le type d’élément à télécharger.</span><span class="sxs-lookup"><span data-stu-id="4c214-115">A [library location constant](library-location-constants.md) that specifies the type of item to be downloaded.</span></span> <span data-ttu-id="4c214-116">Par exemple, CPTrackID spécifie qu’une ou plusieurs pistes doivent être téléchargées.</span><span class="sxs-lookup"><span data-stu-id="4c214-116">For example, CPTrackID specifies that one or more tracks are to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="4c214-117">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c214-117">*IDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c214-118">**Chaîne** contenant les ID, délimités par des points-virgules, des éléments multimédias à télécharger.</span><span class="sxs-lookup"><span data-stu-id="4c214-118">**String** containing the IDs, delimited by semicolons, of the media items to be downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c214-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c214-119">Return value</span></span>

<span data-ttu-id="4c214-120">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4c214-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c214-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c214-121">Requirements</span></span>



| <span data-ttu-id="4c214-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c214-122">Requirement</span></span> | <span data-ttu-id="4c214-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c214-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c214-124">Version</span><span class="sxs-lookup"><span data-stu-id="4c214-124">Version</span></span><br/> | <span data-ttu-id="4c214-125">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="4c214-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="4c214-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4c214-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="4c214-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c214-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c214-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c214-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c214-129">**Téléchargement du contenu multimédia**</span><span class="sxs-lookup"><span data-stu-id="4c214-129">**Downloading Media Content**</span></span>](downloading-media-content.md)
</dt> <dt>

[<span data-ttu-id="4c214-130">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="4c214-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4c214-131">**Externe. acheter**</span><span class="sxs-lookup"><span data-stu-id="4c214-131">**External.buy**</span></span>](external-buy.md)
</dt> <dt>

[<span data-ttu-id="4c214-132">**IWMPContentPartner ::D lécharger**</span><span class="sxs-lookup"><span data-stu-id="4c214-132">**IWMPContentPartner::Download**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





