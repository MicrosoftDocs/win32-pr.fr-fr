---
title: External. libraryLocationID
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- External. libraryLocationID Windows Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525940"
---
# <a name="externallibrarylocationid"></a><span data-ttu-id="03745-105">External. libraryLocationID</span><span class="sxs-lookup"><span data-stu-id="03745-105">External.libraryLocationID</span></span>

> [!Note]  
> <span data-ttu-id="03745-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="03745-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="03745-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="03745-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="03745-108">La propriété **libraryLocationID** récupère l’identificateur de l’élément multimédia spécifique qui est actuellement affiché dans la vue du joueur.</span><span class="sxs-lookup"><span data-stu-id="03745-108">The **libraryLocationID** property retrieves the identifier of the specific media item that is currently displayed in the Player's view.</span></span>

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a><span data-ttu-id="03745-109">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="03745-109">Possible Values</span></span>

<span data-ttu-id="03745-110">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="03745-110">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03745-111">Notes</span><span class="sxs-lookup"><span data-stu-id="03745-111">Remarks</span></span>

<span data-ttu-id="03745-112">Cette propriété fonctionne en association avec la propriété [External. libraryLocationType](external-librarylocationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="03745-112">This property works in combination with the [External.libraryLocationType](external-librarylocationtype.md) property.</span></span> <span data-ttu-id="03745-113">Par exemple, supposons que **libraryLocationType** est égal à CPAlbumID et que **libraryLocationID** est égal à 3.</span><span class="sxs-lookup"><span data-stu-id="03745-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="03745-114">Cela signifie que la vue actuelle dans le lecteur Windows Media affiche l’album dont l’ID est 3.</span><span class="sxs-lookup"><span data-stu-id="03745-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="03745-115">Pour plus d’informations sur la façon dont le lecteur Windows Media caractérise les vues du contenu de la boutique en ligne, consultez [emplacement et élément sélectionné](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="03745-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="03745-116">Certains affichages du lecteur Windows Media sont associés à un élément multimédia particulier.</span><span class="sxs-lookup"><span data-stu-id="03745-116">Certain views in Windows Media Player are associated with a particular media item.</span></span> <span data-ttu-id="03745-117">Par exemple, si la vue actuelle représente un album individuel, **libraryLocationType** est égal à CPAlbumID et **LIBRARYLOCATIONID** est l’ID de l’album.</span><span class="sxs-lookup"><span data-stu-id="03745-117">For example, if the current view represents an individual album, **libraryLocationType** is equal to CPAlbumID, and **libraryLocationID** is the ID of the album.</span></span> <span data-ttu-id="03745-118">Les autres vues ne sont pas associées à un élément multimédia particulier.</span><span class="sxs-lookup"><span data-stu-id="03745-118">Other views are not associated with any particular media item.</span></span> <span data-ttu-id="03745-119">Par exemple, si la vue actuelle représente tous les albums, **libraryLocationType** est égal à AllCPAlbumIDs, mais il n’existe aucune valeur significative pouvant être assignée à **libraryLocationID**.</span><span class="sxs-lookup"><span data-stu-id="03745-119">For example, if the current view represents all albums, **libraryLocationType** is equal to AllCPAlbumIDs, but there is no meaningful value that can be assigned to **libraryLocationID**.</span></span> <span data-ttu-id="03745-120">Dans les cas où la propriété **libraryLocationID** n’a aucune valeur significative, elle est égale à la chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="03745-120">In cases where the **libraryLocationID** property has no meaningful value, it is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="03745-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03745-121">Requirements</span></span>



| <span data-ttu-id="03745-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03745-122">Requirement</span></span> | <span data-ttu-id="03745-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="03745-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03745-124">Version</span><span class="sxs-lookup"><span data-stu-id="03745-124">Version</span></span><br/> | <span data-ttu-id="03745-125">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="03745-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="03745-126">DLL</span><span class="sxs-lookup"><span data-stu-id="03745-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="03745-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03745-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03745-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03745-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03745-129">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="03745-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="03745-130">**External. libraryLocationType**</span><span class="sxs-lookup"><span data-stu-id="03745-130">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="03745-131">**Emplacement et élément sélectionné**</span><span class="sxs-lookup"><span data-stu-id="03745-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





