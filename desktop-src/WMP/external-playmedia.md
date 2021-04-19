---
title: External. playMedia, méthode
description: Cette page décrit une fonctionnalité du kit de développement logiciel (SDK) Windows Media Player 9 Series et le kit de développement logiciel (SDK) Windows Media Player 10. Elle n’est peut-être pas disponible dans les versions ultérieures.
ms.assetid: 48071318-e853-4139-8fe4-17d1cdbef8f5
keywords:
- méthode playMedia lecteur Windows Media
- méthode playMedia lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode playMedia
topic_type:
- apiref
api_name:
- External.playMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0330e7e68d8b4e3747c019e0841f872d279c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528614"
---
# <a name="externalplaymedia-method"></a><span data-ttu-id="3d2b8-107">External. playMedia, méthode</span><span class="sxs-lookup"><span data-stu-id="3d2b8-107">External.playMedia method</span></span>

<span data-ttu-id="3d2b8-108">Cette page décrit une fonctionnalité du kit de développement logiciel (SDK) Windows Media Player 9 Series et le kit de développement logiciel (SDK) Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="3d2b8-108">This page documents a feature of the Windows Media Player 9 Series SDK and the Windows Media Player 10 SDK.</span></span> <span data-ttu-id="3d2b8-109">Elle n’est peut-être pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d2b8-109">It may be unavailable in subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="3d2b8-110">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="3d2b8-110">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3d2b8-111">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="3d2b8-111">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3d2b8-112">La méthode **playMedia** spécifie l’URL d’un élément multimédia numérique à lire.</span><span class="sxs-lookup"><span data-stu-id="3d2b8-112">The **playMedia** method specifies the URL of a digital media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2b8-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d2b8-113">Syntax</span></span>


```JScript
External.playMedia(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="3d2b8-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d2b8-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d2b8-115">*URL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d2b8-115">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2b8-116">**Chaîne** spécifiant l’URL de l’élément multimédia numérique à lire.</span><span class="sxs-lookup"><span data-stu-id="3d2b8-116">**String** specifying the URL of the digital media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d2b8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d2b8-117">Return value</span></span>

<span data-ttu-id="3d2b8-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3d2b8-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d2b8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3d2b8-119">Remarks</span></span>

<span data-ttu-id="3d2b8-120">Cette méthode est uniquement disponible pour les pages Web hébergées dans la fonctionnalité de **Guide** .</span><span class="sxs-lookup"><span data-stu-id="3d2b8-120">This method is only available to webpages hosted in the **Guide** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d2b8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d2b8-121">Requirements</span></span>



| <span data-ttu-id="3d2b8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d2b8-122">Requirement</span></span> | <span data-ttu-id="3d2b8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d2b8-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2b8-124">Version</span><span class="sxs-lookup"><span data-stu-id="3d2b8-124">Version</span></span><br/> | <span data-ttu-id="3d2b8-125">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3d2b8-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="3d2b8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3d2b8-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="3d2b8-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d2b8-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d2b8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d2b8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d2b8-129">**Objet externe pour les magasins de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="3d2b8-129">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





