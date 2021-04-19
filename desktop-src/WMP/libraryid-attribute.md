---
title: Id_bibliothèque (attribut)
description: L’attribut Id_bibliothèque est l’identificateur de la bibliothèque à laquelle l’élément appartient.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- Attribut Id_bibliothèque lecteur Windows Media
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545924"
---
# <a name="libraryid-attribute"></a><span data-ttu-id="6c7a9-104">Id_bibliothèque (attribut)</span><span class="sxs-lookup"><span data-stu-id="6c7a9-104">LibraryID Attribute</span></span>

<span data-ttu-id="6c7a9-105">L’attribut **ID_bibliothèque** est l’identificateur de la bibliothèque à laquelle l’élément appartient.</span><span class="sxs-lookup"><span data-stu-id="6c7a9-105">The **LibraryID** attribute is the identifier of the library that the item belongs to.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6c7a9-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="6c7a9-106">Applies To</span></span>

-   [<span data-ttu-id="6c7a9-107">**Éléments audio**</span><span class="sxs-lookup"><span data-stu-id="6c7a9-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="6c7a9-108">**Éléments de photo**</span><span class="sxs-lookup"><span data-stu-id="6c7a9-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="6c7a9-109">**Éléments de sélection**</span><span class="sxs-lookup"><span data-stu-id="6c7a9-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="6c7a9-110">**Éléments vidéo**</span><span class="sxs-lookup"><span data-stu-id="6c7a9-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6c7a9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6c7a9-111">Remarks</span></span>

<span data-ttu-id="6c7a9-112">Un élément multimédia peut appartenir à la bibliothèque locale de l’utilisateur actuel ou il peut appartenir à une bibliothèque qui a été mise à la disposition d’un autre utilisateur sur le réseau local ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6c7a9-112">A media item might belong to the current user's local library or it might belong to a library that has been made available by another user on the home network or the Internet.</span></span>

<span data-ttu-id="6c7a9-113">La valeur de cet attribut est la même que la valeur retournée par la méthode [**IWMPLibrary2 :: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .</span><span class="sxs-lookup"><span data-stu-id="6c7a9-113">The value of this attribute is the same as the value returned by the [**IWMPLibrary2::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c7a9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c7a9-114">Requirements</span></span>



| <span data-ttu-id="6c7a9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c7a9-115">Requirement</span></span> | <span data-ttu-id="6c7a9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c7a9-116">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="6c7a9-117">Version</span><span class="sxs-lookup"><span data-stu-id="6c7a9-117">Version</span></span><br/> | <span data-ttu-id="6c7a9-118">Lecteur Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="6c7a9-118">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c7a9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c7a9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c7a9-120">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="6c7a9-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





