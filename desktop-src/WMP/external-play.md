---
title: External. Play, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode Play demande au lecteur Windows Media de lire un ensemble d’éléments multimédias.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- Play, méthode lecteur Windows Media
- méthode Play lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode Play
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525344"
---
# <a name="externalplay-method"></a><span data-ttu-id="0fad6-108">External. Play, méthode</span><span class="sxs-lookup"><span data-stu-id="0fad6-108">External.play method</span></span>

> [!Note]  
> <span data-ttu-id="0fad6-109">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="0fad6-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="0fad6-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0fad6-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="0fad6-111">La méthode **Play** demande au lecteur Windows Media de lire un ensemble d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="0fad6-111">The **play** method instructs Windows Media Player to play a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fad6-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fad6-112">Syntax</span></span>


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a><span data-ttu-id="0fad6-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fad6-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fad6-114">*LibraryLocationType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0fad6-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fad6-115">[Constante d’emplacement de bibliothèque](library-location-constants.md) qui spécifie le type des éléments multimédias à lire.</span><span class="sxs-lookup"><span data-stu-id="0fad6-115">A [library location constant](library-location-constants.md) that specifies the type of the media items to be played.</span></span> <span data-ttu-id="0fad6-116">Par exemple, CPAlbumID spécifie qu’un ou plusieurs albums doivent être lus.</span><span class="sxs-lookup"><span data-stu-id="0fad6-116">For example, CPAlbumID specifies that one or more albums are to be played.</span></span>

</dd> <dt>

<span data-ttu-id="0fad6-117">*LibraryLocationIDs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0fad6-117">*LibraryLocationIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fad6-118">**Chaîne** contenant les identificateurs, délimités par des points-virgules, des éléments multimédias à lire.</span><span class="sxs-lookup"><span data-stu-id="0fad6-118">**String** containing the identifiers, delimited by semicolons, of the media items to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fad6-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0fad6-119">Return value</span></span>

<span data-ttu-id="0fad6-120">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0fad6-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fad6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fad6-121">Requirements</span></span>



| <span data-ttu-id="0fad6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fad6-122">Requirement</span></span> | <span data-ttu-id="0fad6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fad6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0fad6-124">Version</span><span class="sxs-lookup"><span data-stu-id="0fad6-124">Version</span></span><br/> | <span data-ttu-id="0fad6-125">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="0fad6-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="0fad6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0fad6-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="0fad6-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fad6-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fad6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fad6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fad6-129">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="0fad6-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





