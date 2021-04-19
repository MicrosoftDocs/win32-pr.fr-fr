---
title: Attribut WM/Publisher
description: L’attribut WM/Publisher est le nom de la société qui a publié le contenu.
ms.assetid: 5f3aa5de-237e-449c-918e-8750481adc6f
keywords:
- Attribut WM/Publisher pour le lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Publisher
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00bd0d2ab2b6d886639cffa1df0770dfe329f7f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532259"
---
# <a name="wmpublisher-attribute"></a><span data-ttu-id="79350-104">Attribut WM/Publisher</span><span class="sxs-lookup"><span data-stu-id="79350-104">WM/Publisher Attribute</span></span>

<span data-ttu-id="79350-105">L’attribut **WM/Publisher** est le nom de la société qui a publié le contenu.</span><span class="sxs-lookup"><span data-stu-id="79350-105">The **WM/Publisher** attribute is the name of the company that published the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="79350-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="79350-106">Applies To</span></span>

-   [<span data-ttu-id="79350-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="79350-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="79350-108">Sélections de CD</span><span class="sxs-lookup"><span data-stu-id="79350-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="79350-109">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="79350-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="79350-110">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="79350-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="79350-111">DVD</span><span class="sxs-lookup"><span data-stu-id="79350-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="79350-112">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="79350-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="79350-113">Notes</span><span class="sxs-lookup"><span data-stu-id="79350-113">Remarks</span></span>

<span data-ttu-id="79350-114">Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="79350-114">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="79350-115">**Label**, **ReleasedBy** et **Studio** sont des alias de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="79350-115">**Label**, **ReleasedBy**, and **Studio** are aliases for this attribute.</span></span>

<span data-ttu-id="79350-116">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMPublisher.</span><span class="sxs-lookup"><span data-stu-id="79350-116">The Windows Media Format SDK constant for this attribute is g\_wszWMPublisher.</span></span>

<span data-ttu-id="79350-117">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="79350-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="79350-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79350-118">Requirements</span></span>



| <span data-ttu-id="79350-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79350-119">Requirement</span></span> | <span data-ttu-id="79350-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="79350-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="79350-121">Version</span><span class="sxs-lookup"><span data-stu-id="79350-121">Version</span></span><br/> | <span data-ttu-id="79350-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="79350-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79350-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79350-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79350-124">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="79350-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





