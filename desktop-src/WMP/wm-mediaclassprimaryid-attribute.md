---
title: Attribut WM/MediaClassPrimaryID
description: L’attribut WM/MediaClassPrimaryID est un GUID spécifiant l’une des classes de médias primaires musique, audio non musicale, vidéo ou autre.
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- Attribut WM/MediaClassPrimaryID lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5107a2c4e04e9424bf0a20a7d4cf7b8edef80492
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523568"
---
# <a name="wmmediaclassprimaryid-attribute"></a><span data-ttu-id="d3139-104">Attribut WM/MediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="d3139-104">WM/MediaClassPrimaryID Attribute</span></span>

<span data-ttu-id="d3139-105">L’attribut **WM/MediaClassPrimaryID** est un GUID spécifiant l’une des classes de support principales : musique, audio non musicale, vidéo ou autre.</span><span class="sxs-lookup"><span data-stu-id="d3139-105">The **WM/MediaClassPrimaryID** attribute is a GUID specifying one of the primary media classes: music, non-music audio, video, or other.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d3139-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="d3139-106">Applies To</span></span>

-   [<span data-ttu-id="d3139-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="d3139-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="d3139-108">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="d3139-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="d3139-109">Autres éléments</span><span class="sxs-lookup"><span data-stu-id="d3139-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="d3139-110">Éléments de photo</span><span class="sxs-lookup"><span data-stu-id="d3139-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="d3139-111">Sélections</span><span class="sxs-lookup"><span data-stu-id="d3139-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="d3139-112">Éléments radio</span><span class="sxs-lookup"><span data-stu-id="d3139-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="d3139-113">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="d3139-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="d3139-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d3139-114">Remarks</span></span>

<span data-ttu-id="d3139-115">Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="d3139-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="d3139-116">**MediaClassPrimaryID** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="d3139-116">**MediaClassPrimaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="d3139-117">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMMediaClassPrimaryID.</span><span class="sxs-lookup"><span data-stu-id="d3139-117">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassPrimaryID.</span></span>

<span data-ttu-id="d3139-118">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="d3139-118">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3139-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3139-119">Requirements</span></span>



| <span data-ttu-id="d3139-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3139-120">Requirement</span></span> | <span data-ttu-id="d3139-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3139-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3139-122">Version</span><span class="sxs-lookup"><span data-stu-id="d3139-122">Version</span></span><br/> | <span data-ttu-id="d3139-123">Lecteur Windows Media série 9 ou version ultérieure (l’élément photo est pris en charge uniquement dans le lecteur Windows Media 10 ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="d3139-123">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3139-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3139-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3139-125">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="d3139-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





