---
title: Attribut WM/WMCollectionID
description: L’attribut WM/WMCollectionID est un GUID identifiant la collection à laquelle l’élément appartient.
ms.assetid: 21fc0a62-d374-4ca3-bbb8-278e0d2497ce
keywords:
- Attribut WM/WMCollectionID lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bce21196e1da9583db293dab004812265c85308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529887"
---
# <a name="wmwmcollectionid-attribute"></a><span data-ttu-id="e76f6-104">Attribut WM/WMCollectionID</span><span class="sxs-lookup"><span data-stu-id="e76f6-104">WM/WMCollectionID Attribute</span></span>

<span data-ttu-id="e76f6-105">L’attribut **WM/WMCollectionID** est un GUID identifiant la collection à laquelle l’élément appartient.</span><span class="sxs-lookup"><span data-stu-id="e76f6-105">The **WM/WMCollectionID** attribute is a GUID identifying the collection to which the item belongs.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e76f6-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="e76f6-106">Applies To</span></span>

-   [<span data-ttu-id="e76f6-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="e76f6-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="e76f6-108">Sélections de CD</span><span class="sxs-lookup"><span data-stu-id="e76f6-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="e76f6-109">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="e76f6-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="e76f6-110">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="e76f6-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e76f6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e76f6-111">Remarks</span></span>

<span data-ttu-id="e76f6-112">Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="e76f6-112">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="e76f6-113">**WMCollectionID** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="e76f6-113">**WMCollectionID** is an alias for this attribute.</span></span>

<span data-ttu-id="e76f6-114">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMCollectionID.</span><span class="sxs-lookup"><span data-stu-id="e76f6-114">The Windows Media Format SDK constant for this attribute is g\_wszWMCollectionID.</span></span>

<span data-ttu-id="e76f6-115">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="e76f6-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e76f6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e76f6-116">Requirements</span></span>



| <span data-ttu-id="e76f6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e76f6-117">Requirement</span></span> | <span data-ttu-id="e76f6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e76f6-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e76f6-119">Version</span><span class="sxs-lookup"><span data-stu-id="e76f6-119">Version</span></span><br/> | <span data-ttu-id="e76f6-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e76f6-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e76f6-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e76f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76f6-122">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="e76f6-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





