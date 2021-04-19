---
title: Attribut auteur
description: L’attribut Author est le nom d’un artiste multimédia ou d’un acteur associé au contenu.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Attribut auteur lecteur Windows Media
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541394"
---
# <a name="author-attribute"></a><span data-ttu-id="6c0d6-104">Attribut auteur</span><span class="sxs-lookup"><span data-stu-id="6c0d6-104">Author Attribute</span></span>

<span data-ttu-id="6c0d6-105">L’attribut **Author** est le nom d’un artiste multimédia ou d’un acteur associé au contenu.</span><span class="sxs-lookup"><span data-stu-id="6c0d6-105">The **Author** attribute is the name of a media artist or actor associated with the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6c0d6-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="6c0d6-106">Applies To</span></span>

-   [<span data-ttu-id="6c0d6-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="6c0d6-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="6c0d6-108">Sélections de CD</span><span class="sxs-lookup"><span data-stu-id="6c0d6-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="6c0d6-109">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="6c0d6-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="6c0d6-110">Fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="6c0d6-110">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="6c0d6-111">DVD</span><span class="sxs-lookup"><span data-stu-id="6c0d6-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="6c0d6-112">Media. getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="6c0d6-112">Media.getItemInfoByType</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="6c0d6-113">Éléments de photo</span><span class="sxs-lookup"><span data-stu-id="6c0d6-113">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="6c0d6-114">Sélections</span><span class="sxs-lookup"><span data-stu-id="6c0d6-114">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="6c0d6-115">Éléments radio</span><span class="sxs-lookup"><span data-stu-id="6c0d6-115">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="6c0d6-116">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="6c0d6-116">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6c0d6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6c0d6-117">Remarks</span></span>

<span data-ttu-id="6c0d6-118">Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="6c0d6-118">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="6c0d6-119">Cet attribut peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="6c0d6-119">This attribute may have multiple values.</span></span> <span data-ttu-id="6c0d6-120">Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser le *média*. méthode **getItemInfoByType** , pas le *média*. méthode **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="6c0d6-120">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.**getItemInfo** method.</span></span>

<span data-ttu-id="6c0d6-121">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMAuthor.</span><span class="sxs-lookup"><span data-stu-id="6c0d6-121">The Windows Media Format SDK constant for this attribute is g\_wszWMAuthor.</span></span>

<span data-ttu-id="6c0d6-122">L' **acteur** et l' **artiste** sont des alias de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="6c0d6-122">**Actor** and **Artist** are aliases for this attribute.</span></span>

<span data-ttu-id="6c0d6-123">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6c0d6-123">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c0d6-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c0d6-124">Requirements</span></span>



| <span data-ttu-id="6c0d6-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c0d6-125">Requirement</span></span> | <span data-ttu-id="6c0d6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c0d6-126">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="6c0d6-127">Version</span><span class="sxs-lookup"><span data-stu-id="6c0d6-127">Version</span></span><br/> | <span data-ttu-id="6c0d6-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6c0d6-128">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c0d6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c0d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0d6-130">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="6c0d6-130">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





