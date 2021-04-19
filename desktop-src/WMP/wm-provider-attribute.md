---
title: Attribut WM/Provider
description: L’attribut WM/Provider est le nom du fournisseur des valeurs d’attribut.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- Attribut WM/Provider lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c2c1c796edf28a567f72708c60c7976f718bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542537"
---
# <a name="wmprovider-attribute"></a><span data-ttu-id="7df40-104">Attribut WM/Provider</span><span class="sxs-lookup"><span data-stu-id="7df40-104">WM/Provider Attribute</span></span>

<span data-ttu-id="7df40-105">L’attribut **WM/Provider** est le nom du fournisseur des valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="7df40-105">The **WM/Provider** attribute is the name of the provider of the attribute values.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7df40-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="7df40-106">Applies To</span></span>

-   [<span data-ttu-id="7df40-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="7df40-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="7df40-108">Sélections de CD</span><span class="sxs-lookup"><span data-stu-id="7df40-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="7df40-109">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="7df40-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="7df40-110">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="7df40-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="7df40-111">Éléments radio</span><span class="sxs-lookup"><span data-stu-id="7df40-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="7df40-112">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="7df40-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="7df40-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7df40-113">Remarks</span></span>

<span data-ttu-id="7df40-114">Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="7df40-114">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="7df40-115">La **redatasource** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="7df40-115">**MetadataSource** is an alias for this attribute.</span></span>

<span data-ttu-id="7df40-116">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMProvider.</span><span class="sxs-lookup"><span data-stu-id="7df40-116">The Windows Media Format SDK constant for this attribute is g\_wszWMProvider.</span></span>

<span data-ttu-id="7df40-117">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="7df40-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7df40-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7df40-118">Requirements</span></span>



| <span data-ttu-id="7df40-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7df40-119">Requirement</span></span> | <span data-ttu-id="7df40-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7df40-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df40-121">Version</span><span class="sxs-lookup"><span data-stu-id="7df40-121">Version</span></span><br/> | <span data-ttu-id="7df40-122">Lecteur Windows Media série 9 ou version ultérieure (l’élément photo est pris en charge uniquement dans le lecteur Windows Media 10 ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="7df40-122">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7df40-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7df40-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df40-124">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="7df40-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





