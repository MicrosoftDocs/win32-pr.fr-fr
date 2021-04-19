---
title: Attribut WM/MCDI
description: L’attribut WM/MCDI est l’identificateur de CD de musique du CD à partir duquel le fichier ou la piste a été copié.
ms.assetid: f0bec14d-416c-477f-98df-dece0bf85ea4
keywords:
- Attribut WM/MCDI lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec51c306f94e25acb94155c4d87f1f1a8b95866
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520873"
---
# <a name="wmmcdi-attribute"></a><span data-ttu-id="6bc8d-104">Attribut WM/MCDI</span><span class="sxs-lookup"><span data-stu-id="6bc8d-104">WM/MCDI Attribute</span></span>

<span data-ttu-id="6bc8d-105">L’attribut **WM/MCDI** est l’identificateur de CD de musique du CD à partir duquel le fichier ou la piste a été copié.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-105">The **WM/MCDI** attribute is the music CD identifier of the CD from which the file or track was copied.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6bc8d-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="6bc8d-106">Applies To</span></span>

-   [<span data-ttu-id="6bc8d-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="6bc8d-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="6bc8d-108">Pistes de CD</span><span class="sxs-lookup"><span data-stu-id="6bc8d-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="6bc8d-109">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="6bc8d-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6bc8d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6bc8d-110">Remarks</span></span>

<span data-ttu-id="6bc8d-111">Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="6bc8d-112">**TOC** est un alias pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-112">**TOC** is an alias for this attribute.</span></span>

<span data-ttu-id="6bc8d-113">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMMCDI.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-113">The Windows Media Format SDK constant for this attribute is g\_wszWMMCDI.</span></span>

<span data-ttu-id="6bc8d-114">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6bc8d-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bc8d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bc8d-115">Requirements</span></span>



| <span data-ttu-id="6bc8d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bc8d-116">Requirement</span></span> | <span data-ttu-id="6bc8d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bc8d-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="6bc8d-118">Version</span><span class="sxs-lookup"><span data-stu-id="6bc8d-118">Version</span></span><br/> | <span data-ttu-id="6bc8d-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6bc8d-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6bc8d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bc8d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bc8d-121">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="6bc8d-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





