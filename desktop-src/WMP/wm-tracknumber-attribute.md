---
title: Attribut WM/TrackNumber
description: L’attribut WM/TrackNumber est le numéro de suivi de l’élément sur l’album sur lequel il a été publié à l’origine.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- Attribut WM/TrackNumber lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539932"
---
# <a name="wmtracknumber-attribute"></a><span data-ttu-id="0a994-104">Attribut WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="0a994-104">WM/TrackNumber Attribute</span></span>

<span data-ttu-id="0a994-105">L’attribut **WM/TrackNumber** est le numéro de suivi de l’élément sur l’album sur lequel il a été publié à l’origine.</span><span class="sxs-lookup"><span data-stu-id="0a994-105">The **WM/TrackNumber** attribute is the track number of the item on the album on which it was originally released.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0a994-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="0a994-106">Applies To</span></span>

-   [<span data-ttu-id="0a994-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="0a994-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="0a994-108">Attributs de fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="0a994-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="0a994-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0a994-109">Remarks</span></span>

<span data-ttu-id="0a994-110">Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="0a994-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="0a994-111">Le suivi des nombres pour un album commence à 1.</span><span class="sxs-lookup"><span data-stu-id="0a994-111">Track numbers for an album start at 1.</span></span>

<span data-ttu-id="0a994-112">**OriginalIndex** et **OriginalIndexLeft** sont des alias de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="0a994-112">**OriginalIndex** and **OriginalIndexLeft** are aliases for this attribute.</span></span>

<span data-ttu-id="0a994-113">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMTrackNumber.</span><span class="sxs-lookup"><span data-stu-id="0a994-113">The Windows Media Format SDK constant for this attribute is g\_wszWMTrackNumber.</span></span>

<span data-ttu-id="0a994-114">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="0a994-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a994-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a994-115">Requirements</span></span>



| <span data-ttu-id="0a994-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a994-116">Requirement</span></span> | <span data-ttu-id="0a994-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a994-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="0a994-118">Version</span><span class="sxs-lookup"><span data-stu-id="0a994-118">Version</span></span><br/> | <span data-ttu-id="0a994-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0a994-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a994-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a994-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a994-121">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="0a994-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





