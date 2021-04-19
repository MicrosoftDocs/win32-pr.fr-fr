---
title: Attribut WM/MediaClassSecondaryID
description: L’attribut WM/MediaClassSecondaryID est un GUID spécifiant la classe de support secondaire, qui est une sous-classe de la classe de support primaire.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Attribut WM/MediaClassSecondaryID lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545916"
---
# <a name="wmmediaclasssecondaryid-attribute"></a><span data-ttu-id="9b656-104">Attribut WM/MediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="9b656-104">WM/MediaClassSecondaryID Attribute</span></span>

<span data-ttu-id="9b656-105">L’attribut **WM/MediaClassSecondaryID** est un GUID spécifiant la classe de support secondaire, qui est une sous-classe de la classe de support primaire.</span><span class="sxs-lookup"><span data-stu-id="9b656-105">The **WM/MediaClassSecondaryID** attribute is a GUID specifying the secondary media class, which is a subclass of the primary media class.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9b656-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="9b656-106">Applies To</span></span>

-   [<span data-ttu-id="9b656-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="9b656-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="9b656-108">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="9b656-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="9b656-109">Autres éléments</span><span class="sxs-lookup"><span data-stu-id="9b656-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="9b656-110">Éléments de photo</span><span class="sxs-lookup"><span data-stu-id="9b656-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="9b656-111">Sélections</span><span class="sxs-lookup"><span data-stu-id="9b656-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="9b656-112">Éléments radio</span><span class="sxs-lookup"><span data-stu-id="9b656-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="9b656-113">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="9b656-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="9b656-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9b656-114">Remarks</span></span>

<span data-ttu-id="9b656-115">Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="9b656-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="9b656-116">Le tableau suivant répertorie les GUID pris en charge et leurs descriptions.</span><span class="sxs-lookup"><span data-stu-id="9b656-116">The following table lists the supported GUIDs and their descriptions.</span></span>



| <span data-ttu-id="9b656-117">GUID</span><span class="sxs-lookup"><span data-stu-id="9b656-117">GUID</span></span>                                 | <span data-ttu-id="9b656-118">Description</span><span class="sxs-lookup"><span data-stu-id="9b656-118">Description</span></span>                                    |
|--------------------------------------|------------------------------------------------|
| <span data-ttu-id="9b656-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span><span class="sxs-lookup"><span data-stu-id="9b656-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span></span> | <span data-ttu-id="9b656-120">L’objet Media représente une sélection statique.</span><span class="sxs-lookup"><span data-stu-id="9b656-120">The media object represents a static playlist.</span></span> |
| <span data-ttu-id="9b656-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span><span class="sxs-lookup"><span data-stu-id="9b656-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span></span> | <span data-ttu-id="9b656-122">L’objet Media représente une sélection automatique.</span><span class="sxs-lookup"><span data-stu-id="9b656-122">The media object represents an auto playlist.</span></span>  |



 

<span data-ttu-id="9b656-123">**MediaClassSecondaryID** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="9b656-123">**MediaClassSecondaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="9b656-124">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMMediaClassSecondaryID.</span><span class="sxs-lookup"><span data-stu-id="9b656-124">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassSecondaryID.</span></span>

<span data-ttu-id="9b656-125">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="9b656-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b656-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b656-126">Requirements</span></span>



| <span data-ttu-id="9b656-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b656-127">Requirement</span></span> | <span data-ttu-id="9b656-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b656-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b656-129">Version</span><span class="sxs-lookup"><span data-stu-id="9b656-129">Version</span></span><br/> | <span data-ttu-id="9b656-130">L’élément photo est pris en charge uniquement dans le lecteur Windows Media 10 ou ultérieur. l’élément radio est pris en charge uniquement dans le lecteur Windows Media série 9. tous les autres éléments sont pris en charge dans le lecteur Windows Media 9 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="9b656-130">The photo item is supported only in Windows Media Player 10 or later The radio item is supported only in Windows Media Player 9 Series All other items are supported in Windows Media Player 9 Series and later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b656-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b656-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b656-132">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="9b656-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





