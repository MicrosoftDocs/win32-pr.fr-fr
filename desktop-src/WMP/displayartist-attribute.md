---
title: Attribut DisplayArtist
description: L’attribut DisplayArtist est le nom de l’artiste affiché pour un élément.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- Attribut DisplayArtist lecteur Windows Media
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523597"
---
# <a name="displayartist-attribute"></a><span data-ttu-id="6ec6c-104">Attribut DisplayArtist</span><span class="sxs-lookup"><span data-stu-id="6ec6c-104">DisplayArtist Attribute</span></span>

<span data-ttu-id="6ec6c-105">L’attribut **DisplayArtist** est le nom de l’artiste affiché pour un élément.</span><span class="sxs-lookup"><span data-stu-id="6ec6c-105">The **DisplayArtist** attribute is the name of the artist that is displayed for an item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6ec6c-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="6ec6c-106">Applies To</span></span>

-   [<span data-ttu-id="6ec6c-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="6ec6c-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6ec6c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6ec6c-108">Remarks</span></span>

<span data-ttu-id="6ec6c-109">En règle générale, **DisplayArtist** aura la même valeur que l’attribut **WM/AlbumArtist** lorsque cet attribut est défini.</span><span class="sxs-lookup"><span data-stu-id="6ec6c-109">Generally, **DisplayArtist** will have the same value as the **WM/AlbumArtist** attribute when that attribute is set.</span></span> <span data-ttu-id="6ec6c-110">Dans le cas contraire, la valeur sera le nom de l’artiste associé à la première piste de l’album.</span><span class="sxs-lookup"><span data-stu-id="6ec6c-110">Otherwise, the value will be the name of the artist that is associated with the first track on the album.</span></span>

<span data-ttu-id="6ec6c-111">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6ec6c-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec6c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ec6c-112">Requirements</span></span>



| <span data-ttu-id="6ec6c-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ec6c-113">Requirement</span></span> | <span data-ttu-id="6ec6c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ec6c-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="6ec6c-115">Version</span><span class="sxs-lookup"><span data-stu-id="6ec6c-115">Version</span></span><br/> | <span data-ttu-id="6ec6c-116">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="6ec6c-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ec6c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ec6c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec6c-118">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="6ec6c-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="6ec6c-119">**Attribut WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="6ec6c-119">**WM/AlbumArtist Attribute**</span></span>](wm-albumartist-attribute.md)
</dt> </dl>

 

 





