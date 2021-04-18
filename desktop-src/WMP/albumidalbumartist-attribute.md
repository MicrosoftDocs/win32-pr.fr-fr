---
title: Attribut AlbumIDAlbumArtist
description: L’attribut AlbumIDAlbumArtist est un identificateur unique pour l’album.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- Attribut AlbumIDAlbumArtist lecteur Windows Media
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1925f40a50b15efcd339ad949d5d54ddb915cbe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528954"
---
# <a name="albumidalbumartist-attribute"></a><span data-ttu-id="4bdbd-104">Attribut AlbumIDAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="4bdbd-104">AlbumIDAlbumArtist Attribute</span></span>

<span data-ttu-id="4bdbd-105">L’attribut **AlbumIDAlbumArtist** est un identificateur unique pour l’album.</span><span class="sxs-lookup"><span data-stu-id="4bdbd-105">The **AlbumIDAlbumArtist** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4bdbd-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="4bdbd-106">Applies To</span></span>

-   [<span data-ttu-id="4bdbd-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="4bdbd-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="4bdbd-108">Notes</span><span class="sxs-lookup"><span data-stu-id="4bdbd-108">Remarks</span></span>

<span data-ttu-id="4bdbd-109">Cet attribut est stocké uniquement dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4bdbd-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="4bdbd-110">L’identificateur unique est une combinaison du titre de l’album et du nom de l’artiste de l’album.</span><span class="sxs-lookup"><span data-stu-id="4bdbd-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="4bdbd-111">Dans cet attribut, le nom de l’artiste de l’album est le premier.</span><span class="sxs-lookup"><span data-stu-id="4bdbd-111">In this attribute, the album artist name comes first.</span></span> <span data-ttu-id="4bdbd-112">Lorsque vous utilisez la méthode [MediaCollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) pour obtenir un objet **StringCollection** à l’aide de cet attribut, les valeurs sont triées par nom de l’artiste de l’album.</span><span class="sxs-lookup"><span data-stu-id="4bdbd-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album artist name.</span></span>

<span data-ttu-id="4bdbd-113">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4bdbd-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bdbd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bdbd-114">Requirements</span></span>



| <span data-ttu-id="4bdbd-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bdbd-115">Requirement</span></span> | <span data-ttu-id="4bdbd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bdbd-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="4bdbd-117">Version</span><span class="sxs-lookup"><span data-stu-id="4bdbd-117">Version</span></span><br/> | <span data-ttu-id="4bdbd-118">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4bdbd-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bdbd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bdbd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bdbd-120">**Attribut AlbumID**</span><span class="sxs-lookup"><span data-stu-id="4bdbd-120">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="4bdbd-121">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="4bdbd-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





