---
title: Attribut PeakValue
description: L’attribut PeakValue est une valeur d’amplitude de 16 bits indiquant le niveau de volume maximal.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Attribut PeakValue lecteur Windows Media
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537874"
---
# <a name="peakvalue-attribute"></a><span data-ttu-id="7453c-104">Attribut PeakValue</span><span class="sxs-lookup"><span data-stu-id="7453c-104">PeakValue Attribute</span></span>

<span data-ttu-id="7453c-105">L’attribut **PeakValue** est une valeur d’amplitude de 16 bits indiquant le niveau de volume maximal.</span><span class="sxs-lookup"><span data-stu-id="7453c-105">The **PeakValue** attribute is a 16-bit amplitude value indicating the peak volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7453c-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="7453c-106">Applies To</span></span>

-   [<span data-ttu-id="7453c-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="7453c-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="7453c-108">Fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="7453c-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="7453c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="7453c-109">Remarks</span></span>

<span data-ttu-id="7453c-110">Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="7453c-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="7453c-111">Le lecteur Windows Media définit cette valeur dans l’une ou l’autre des situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7453c-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="7453c-112">Après avoir extrait un fichier.</span><span class="sxs-lookup"><span data-stu-id="7453c-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="7453c-113">Après avoir lu un fichier (lorsque l’optimisation du niveau de volume automatique est activée).</span><span class="sxs-lookup"><span data-stu-id="7453c-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="7453c-114">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszPeakValue.</span><span class="sxs-lookup"><span data-stu-id="7453c-114">The Windows Media Format SDK constant for this attribute is g\_wszPeakValue.</span></span>

<span data-ttu-id="7453c-115">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="7453c-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7453c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7453c-116">Requirements</span></span>



| <span data-ttu-id="7453c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7453c-117">Requirement</span></span> | <span data-ttu-id="7453c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7453c-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="7453c-119">Version</span><span class="sxs-lookup"><span data-stu-id="7453c-119">Version</span></span><br/> | <span data-ttu-id="7453c-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7453c-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7453c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7453c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7453c-122">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="7453c-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





