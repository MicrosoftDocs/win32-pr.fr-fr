---
title: External. selectedItemID
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. selectedItemID
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- External. selectedItemID Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540157"
---
# <a name="externalselecteditemid"></a><span data-ttu-id="b042f-105">External. selectedItemID</span><span class="sxs-lookup"><span data-stu-id="b042f-105">External.selectedItemID</span></span>

> [!Note]  
> <span data-ttu-id="b042f-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="b042f-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b042f-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b042f-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b042f-108">La propriété **SelectedItemId** récupère l’identificateur de l’élément multimédia qui est actuellement sélectionné dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b042f-108">The **selectedItemID** property retrieves the identifier of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="b042f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b042f-109">Syntax</span></span>

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a><span data-ttu-id="b042f-110">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b042f-110">Possible Values</span></span>

<span data-ttu-id="b042f-111">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b042f-111">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b042f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b042f-112">Remarks</span></span>

<span data-ttu-id="b042f-113">Cette propriété est utilisée en association avec la propriété [External. selectedItemType](external-selecteditemtype.md) .</span><span class="sxs-lookup"><span data-stu-id="b042f-113">This property is used in combination with the [External.selectedItemType](external-selecteditemtype.md) property.</span></span> <span data-ttu-id="b042f-114">Par exemple, si **selectedItemType** est égal à CPTrackID, **SELECTEDITEMID** est l’ID de la piste sélectionnée. Pour plus d’informations sur la façon dont le lecteur Windows Media caractérise les vues du contenu de la boutique en ligne, consultez [emplacement et élément sélectionné](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="b042f-114">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="b042f-115">Certains affichages dans le lecteur Windows Media ont un élément multimédia spécifique qui est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b042f-115">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="b042f-116">Par exemple, supposons que la vue actuelle représente un album.</span><span class="sxs-lookup"><span data-stu-id="b042f-116">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="b042f-117">Un album est un conteneur de pistes. par conséquent, **selectedItemType** est égal à CPTrackID et **SELECTEDITEMID** est l’ID de la piste sélectionnée. Les autres vues n’ont pas d’élément multimédia sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b042f-117">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="b042f-118">Par exemple, si l’utilisateur clique sur le nœud racine du magasin en ligne dans le contrôle d’arborescence, le lecteur Windows Media affiche une page de détection fournie par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="b042f-118">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="b042f-119">Le lecteur n’affiche aucun conteneur d’éléments multimédias dans l’interface utilisateur du lecteur.</span><span class="sxs-lookup"><span data-stu-id="b042f-119">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="b042f-120">Dans ce cas, **selectedItemType** est égal à UnknownLocation et **SelectedItemId** est égal à la chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="b042f-120">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="b042f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b042f-121">Requirements</span></span>



| <span data-ttu-id="b042f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b042f-122">Requirement</span></span> | <span data-ttu-id="b042f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b042f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b042f-124">Version</span><span class="sxs-lookup"><span data-stu-id="b042f-124">Version</span></span><br/> | <span data-ttu-id="b042f-125">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="b042f-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="b042f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b042f-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="b042f-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b042f-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b042f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b042f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b042f-129">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="b042f-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b042f-130">**External. selectedItemType**</span><span class="sxs-lookup"><span data-stu-id="b042f-130">**External.selectedItemType**</span></span>](external-selecteditemtype.md)
</dt> <dt>

[<span data-ttu-id="b042f-131">**Emplacement et élément sélectionné**</span><span class="sxs-lookup"><span data-stu-id="b042f-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





