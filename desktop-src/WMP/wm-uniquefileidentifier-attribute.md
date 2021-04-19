---
title: Attribut WM/UniqueFileIdentifier
description: L’attribut WM/UniqueFileIdentifier est une chaîne qui identifie de façon unique l’élément.
ms.assetid: 8196fc38-05dc-4c9e-98cb-1e160ce28a9a
keywords:
- Attribut WM/UniqueFileIdentifier lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a4297f299f6e7df64088066b3137d844a0c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539282"
---
# <a name="wmuniquefileidentifier-attribute"></a><span data-ttu-id="c2101-104">Attribut WM/UniqueFileIdentifier</span><span class="sxs-lookup"><span data-stu-id="c2101-104">WM/UniqueFileIdentifier Attribute</span></span>

<span data-ttu-id="c2101-105">L’attribut **WM/UniqueFileIdentifier** est une chaîne qui identifie de façon unique l’élément.</span><span class="sxs-lookup"><span data-stu-id="c2101-105">The **WM/UniqueFileIdentifier** attribute is a string that uniquely identifies the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c2101-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="c2101-106">Applies To</span></span>

-   [<span data-ttu-id="c2101-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="c2101-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="c2101-108">Sélections de CD</span><span class="sxs-lookup"><span data-stu-id="c2101-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="c2101-109">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="c2101-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="c2101-110">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="c2101-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="c2101-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c2101-111">Remarks</span></span>

<span data-ttu-id="c2101-112">Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="c2101-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="c2101-113">**UniqueFileIdentifier** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="c2101-113">**UniqueFileIdentifier** is an alias for this attribute.</span></span>

<span data-ttu-id="c2101-114">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMUniqueFileIdentifier.</span><span class="sxs-lookup"><span data-stu-id="c2101-114">The Windows Media Format SDK constant for this attribute is g\_wszWMUniqueFileIdentifier.</span></span>

<span data-ttu-id="c2101-115">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c2101-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2101-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2101-116">Requirements</span></span>



| <span data-ttu-id="c2101-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2101-117">Requirement</span></span> | <span data-ttu-id="c2101-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2101-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="c2101-119">Version</span><span class="sxs-lookup"><span data-stu-id="c2101-119">Version</span></span><br/> | <span data-ttu-id="c2101-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c2101-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2101-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2101-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2101-122">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="c2101-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





