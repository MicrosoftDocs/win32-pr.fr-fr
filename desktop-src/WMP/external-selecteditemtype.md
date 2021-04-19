---
title: External. selectedItemType
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. selectedItemType
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- External. selectedItemType Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542438"
---
# <a name="externalselecteditemtype"></a><span data-ttu-id="89b71-105">External. selectedItemType</span><span class="sxs-lookup"><span data-stu-id="89b71-105">External.selectedItemType</span></span>

> [!Note]  
> <span data-ttu-id="89b71-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="89b71-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="89b71-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="89b71-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="89b71-108">La propriété **selectedItemType** récupère le type de l’élément multimédia actuellement sélectionné dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="89b71-108">The **selectedItemType** property retrieves the type of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b71-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89b71-109">Syntax</span></span>

<span data-ttu-id="89b71-110">Window. external. selectedItemType ()</span><span class="sxs-lookup"><span data-stu-id="89b71-110">window.external.selectedItemType()</span></span>

## <a name="possible-values"></a><span data-ttu-id="89b71-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="89b71-111">Possible Values</span></span>

<span data-ttu-id="89b71-112">Cette propriété est une **chaîne** en lecture seule qui contient l’une des [constantes d’emplacement](library-location-constants.md)de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="89b71-112">This property is a read-only **String** that contains one of the [library location constants](library-location-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="89b71-113">Notes</span><span class="sxs-lookup"><span data-stu-id="89b71-113">Remarks</span></span>

<span data-ttu-id="89b71-114">Cette propriété est utilisée en association avec la propriété **External. SelectedItemId** .</span><span class="sxs-lookup"><span data-stu-id="89b71-114">This property is used in combination with the **External.selectedItemID** property.</span></span> <span data-ttu-id="89b71-115">Par exemple, si **selectedItemType** est égal à CPTrackID, **SELECTEDITEMID** est l’ID de la piste sélectionnée. Pour plus d’informations sur la façon dont le lecteur Windows Media caractérise les vues du contenu de la boutique en ligne, consultez [emplacement et élément sélectionné](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="89b71-115">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="89b71-116">Certains affichages dans le lecteur Windows Media ont un élément multimédia spécifique qui est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="89b71-116">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="89b71-117">Par exemple, supposons que la vue actuelle représente un album.</span><span class="sxs-lookup"><span data-stu-id="89b71-117">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="89b71-118">Un album est un conteneur de pistes. par conséquent, **selectedItemType** est égal à CPTrackID et **SELECTEDITEMID** est l’ID de la piste sélectionnée. Les autres vues n’ont pas d’élément multimédia sélectionné.</span><span class="sxs-lookup"><span data-stu-id="89b71-118">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="89b71-119">Par exemple, si l’utilisateur clique sur le nœud racine du magasin en ligne dans le contrôle d’arborescence, le lecteur Windows Media affiche une page de détection fournie par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="89b71-119">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="89b71-120">Le lecteur n’affiche aucun conteneur d’éléments multimédias dans l’interface utilisateur du lecteur.</span><span class="sxs-lookup"><span data-stu-id="89b71-120">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="89b71-121">Dans ce cas, **selectedItemType** est égal à UnknownLocation et **SelectedItemId** est égal à la chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="89b71-121">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b71-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89b71-122">Requirements</span></span>



| <span data-ttu-id="89b71-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89b71-123">Requirement</span></span> | <span data-ttu-id="89b71-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="89b71-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89b71-125">Version</span><span class="sxs-lookup"><span data-stu-id="89b71-125">Version</span></span><br/> | <span data-ttu-id="89b71-126">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="89b71-126">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="89b71-127">DLL</span><span class="sxs-lookup"><span data-stu-id="89b71-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="89b71-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89b71-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b71-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89b71-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b71-130">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="89b71-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="89b71-131">**External. selectedItemID**</span><span class="sxs-lookup"><span data-stu-id="89b71-131">**External.selectedItemID**</span></span>](external-selecteditemid.md)
</dt> <dt>

[<span data-ttu-id="89b71-132">**Emplacement et élément sélectionné**</span><span class="sxs-lookup"><span data-stu-id="89b71-132">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





