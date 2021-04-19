---
title: Attribut WM/AlbumCoverURL
description: L’attribut WM/AlbumCoverURL est l’URL (Uniform Resource Locator) de la pochette de l’album ou d’une image miniature.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- Attribut WM/AlbumCoverURL lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520878"
---
# <a name="wmalbumcoverurl-attribute"></a><span data-ttu-id="fdfac-104">Attribut WM/AlbumCoverURL</span><span class="sxs-lookup"><span data-stu-id="fdfac-104">WM/AlbumCoverURL Attribute</span></span>

<span data-ttu-id="fdfac-105">L’attribut **WM/AlbumCoverURL** est l’URL (Uniform Resource Locator) de la pochette de l’album ou d’une image miniature.</span><span class="sxs-lookup"><span data-stu-id="fdfac-105">The **WM/AlbumCoverURL** attribute is the uniform resource locator (URL) for album art or a thumbnail image.</span></span>

## <a name="applies-to"></a><span data-ttu-id="fdfac-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="fdfac-106">Applies To</span></span>

-   [<span data-ttu-id="fdfac-107">**Éléments audio**</span><span class="sxs-lookup"><span data-stu-id="fdfac-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="fdfac-108">**Éléments de photo**</span><span class="sxs-lookup"><span data-stu-id="fdfac-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="fdfac-109">**Éléments vidéo**</span><span class="sxs-lookup"><span data-stu-id="fdfac-109">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="fdfac-110">Notes</span><span class="sxs-lookup"><span data-stu-id="fdfac-110">Remarks</span></span>

<span data-ttu-id="fdfac-111">Pour un élément audio, cet attribut est l’URL de la pochette de l’album.</span><span class="sxs-lookup"><span data-stu-id="fdfac-111">For an audio item, this attribute is the URL of the album art.</span></span> <span data-ttu-id="fdfac-112">Pour un élément photo ou vidéo, cet attribut est l’URL d’une image miniature.</span><span class="sxs-lookup"><span data-stu-id="fdfac-112">For a photo or video item, this attribute is the URL of a thumbnail image.</span></span>

<span data-ttu-id="fdfac-113">Cet attribut n’est pas disponible pour les éléments multimédias dans la bibliothèque locale de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="fdfac-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="fdfac-114">Elle est disponible uniquement pour les éléments multimédias appartenant à une bibliothèque distante ; autrement dit, une bibliothèque qui a été mise à la disposition d’un autre utilisateur sur le réseau privé.</span><span class="sxs-lookup"><span data-stu-id="fdfac-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="fdfac-115">Pour déterminer si une bibliothèque multimédia est distante, appelez [**IWMPLibrary :: obtenir le \_ type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="fdfac-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdfac-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdfac-116">Requirements</span></span>



| <span data-ttu-id="fdfac-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdfac-117">Requirement</span></span> | <span data-ttu-id="fdfac-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdfac-118">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="fdfac-119">Version</span><span class="sxs-lookup"><span data-stu-id="fdfac-119">Version</span></span><br/> | <span data-ttu-id="fdfac-120">Lecteur Windows Media 12 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fdfac-120">Windows Media Player 12 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fdfac-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdfac-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdfac-122">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="fdfac-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





