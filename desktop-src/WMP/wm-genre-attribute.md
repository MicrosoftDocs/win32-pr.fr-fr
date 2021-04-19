---
title: Attribut WM/genre
description: L’attribut WM/genre est le genre du contenu.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- Attribut WM/genre lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae4a0c6ae27e85fa1ed147a3173c4cc31b20f1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545917"
---
# <a name="wmgenre-attribute"></a><span data-ttu-id="b6565-104">Attribut WM/genre</span><span class="sxs-lookup"><span data-stu-id="b6565-104">WM/Genre Attribute</span></span>

<span data-ttu-id="b6565-105">L’attribut **WM/genre** est le genre du contenu.</span><span class="sxs-lookup"><span data-stu-id="b6565-105">The **WM/Genre** attribute is the genre of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b6565-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="b6565-106">Applies To</span></span>

-   [<span data-ttu-id="b6565-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="b6565-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b6565-108">Sélections de CD</span><span class="sxs-lookup"><span data-stu-id="b6565-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="b6565-109">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="b6565-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="b6565-110">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="b6565-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="b6565-111">DVD</span><span class="sxs-lookup"><span data-stu-id="b6565-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="b6565-112">Autres éléments</span><span class="sxs-lookup"><span data-stu-id="b6565-112">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="b6565-113">Sélections</span><span class="sxs-lookup"><span data-stu-id="b6565-113">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="b6565-114">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="b6565-114">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b6565-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b6565-115">Remarks</span></span>

<span data-ttu-id="b6565-116">Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="b6565-116">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="b6565-117">Cet attribut peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="b6565-117">This attribute may have multiple values.</span></span> <span data-ttu-id="b6565-118">Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser la méthode **Media. getItemInfoByType** , et non la méthode **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="b6565-118">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="b6565-119">Le **genre** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="b6565-119">**Genre** is an alias for this attribute.</span></span>

<span data-ttu-id="b6565-120">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMGenre.</span><span class="sxs-lookup"><span data-stu-id="b6565-120">The Windows Media Format SDK constant for this attribute is g\_wszWMGenre.</span></span>

<span data-ttu-id="b6565-121">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b6565-121">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6565-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6565-122">Requirements</span></span>



| <span data-ttu-id="b6565-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6565-123">Requirement</span></span> | <span data-ttu-id="b6565-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6565-124">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b6565-125">Version</span><span class="sxs-lookup"><span data-stu-id="b6565-125">Version</span></span><br/> | <span data-ttu-id="b6565-126">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b6565-126">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6565-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6565-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6565-128">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="b6565-128">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="b6565-129">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="b6565-129">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





