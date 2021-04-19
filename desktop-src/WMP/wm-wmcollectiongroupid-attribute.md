---
title: Attribut WM/WMCollectionGroupID
description: L’attribut WM/WMCollectionGroupID est un GUID identifiant le groupe contenant la collection à laquelle l’élément appartient.
ms.assetid: 5383fb12-fc16-474e-b9a0-c1e69b86a057
keywords:
- Attribut WM/WMCollectionGroupID lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681ad7049520ed77de3ebb385e74efcfef66b4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539726"
---
# <a name="wmwmcollectiongroupid-attribute"></a><span data-ttu-id="cccbd-104">Attribut WM/WMCollectionGroupID</span><span class="sxs-lookup"><span data-stu-id="cccbd-104">WM/WMCollectionGroupID Attribute</span></span>

<span data-ttu-id="cccbd-105">L’attribut **WM/WMCollectionGroupID** est un GUID identifiant le groupe contenant la collection à laquelle l’élément appartient.</span><span class="sxs-lookup"><span data-stu-id="cccbd-105">The **WM/WMCollectionGroupID** attribute is a GUID identifying the group containing the collection to which the item belongs.</span></span>

## <a name="applies-to"></a><span data-ttu-id="cccbd-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="cccbd-106">Applies To</span></span>

-   [<span data-ttu-id="cccbd-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="cccbd-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="cccbd-108">Sélections de CD</span><span class="sxs-lookup"><span data-stu-id="cccbd-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="cccbd-109">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="cccbd-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="cccbd-110">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="cccbd-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="cccbd-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cccbd-111">Remarks</span></span>

<span data-ttu-id="cccbd-112">Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="cccbd-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="cccbd-113">**WMCollectionGroupID** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="cccbd-113">**WMCollectionGroupID** is an alias for this attribute.</span></span>

<span data-ttu-id="cccbd-114">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMCollectionGroupID.</span><span class="sxs-lookup"><span data-stu-id="cccbd-114">The Windows Media Format SDK constant for this attribute is g\_wszWMCollectionGroupID.</span></span>

<span data-ttu-id="cccbd-115">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="cccbd-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cccbd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cccbd-116">Requirements</span></span>



| <span data-ttu-id="cccbd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cccbd-117">Requirement</span></span> | <span data-ttu-id="cccbd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cccbd-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="cccbd-119">Version</span><span class="sxs-lookup"><span data-stu-id="cccbd-119">Version</span></span><br/> | <span data-ttu-id="cccbd-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cccbd-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cccbd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cccbd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cccbd-122">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="cccbd-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





