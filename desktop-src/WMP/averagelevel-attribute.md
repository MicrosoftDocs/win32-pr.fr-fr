---
title: Attribut AverageLevel
description: L’attribut AverageLevel est une valeur d’amplitude de 16 bits indiquant le niveau de volume moyen.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- Attribut AverageLevel lecteur Windows Media
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541045"
---
# <a name="averagelevel-attribute"></a><span data-ttu-id="68ba8-104">Attribut AverageLevel</span><span class="sxs-lookup"><span data-stu-id="68ba8-104">AverageLevel Attribute</span></span>

<span data-ttu-id="68ba8-105">L’attribut **AverageLevel** est une valeur d’amplitude de 16 bits indiquant le niveau de volume moyen.</span><span class="sxs-lookup"><span data-stu-id="68ba8-105">The **AverageLevel** attribute is a 16-bit amplitude value indicating the average volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="68ba8-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="68ba8-106">Applies To</span></span>

-   [<span data-ttu-id="68ba8-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="68ba8-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="68ba8-108">Fichiers Windows Media couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="68ba8-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="68ba8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="68ba8-109">Remarks</span></span>

<span data-ttu-id="68ba8-110">Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="68ba8-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="68ba8-111">Le lecteur Windows Media définit cette valeur dans l’une ou l’autre des situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="68ba8-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="68ba8-112">Après avoir extrait un fichier.</span><span class="sxs-lookup"><span data-stu-id="68ba8-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="68ba8-113">Après avoir lu un fichier (lorsque l’optimisation du niveau de volume automatique est activée).</span><span class="sxs-lookup"><span data-stu-id="68ba8-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="68ba8-114">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszAverageLevel.</span><span class="sxs-lookup"><span data-stu-id="68ba8-114">The Windows Media Format SDK constant for this attribute is g\_wszAverageLevel.</span></span>

<span data-ttu-id="68ba8-115">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="68ba8-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="68ba8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68ba8-116">Requirements</span></span>



| <span data-ttu-id="68ba8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68ba8-117">Requirement</span></span> | <span data-ttu-id="68ba8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="68ba8-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="68ba8-119">Version</span><span class="sxs-lookup"><span data-stu-id="68ba8-119">Version</span></span><br/> | <span data-ttu-id="68ba8-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="68ba8-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68ba8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68ba8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ba8-122">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="68ba8-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





