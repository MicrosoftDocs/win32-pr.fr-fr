---
title: VIDEO. Zoom
description: L’attribut zoom spécifie le pourcentage de mise à l’échelle de la vidéo.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- VIDEO. Zoom lecteur Windows Media
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525323"
---
# <a name="videozoom"></a><span data-ttu-id="9ef64-104">VIDEO. Zoom</span><span class="sxs-lookup"><span data-stu-id="9ef64-104">VIDEO.zoom</span></span>

<span data-ttu-id="9ef64-105">L’attribut **Zoom** spécifie le pourcentage de mise à l’échelle de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="9ef64-105">The **zoom** attribute specifies the percentage by which to scale the video.</span></span>

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a><span data-ttu-id="9ef64-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9ef64-106">Possible Values</span></span>

<span data-ttu-id="9ef64-107">Cet attribut est un **nombre** en lecture/écriture (**long**) compris entre 1 et la taille maximale prise en charge par la largeur et la hauteur du contrôle Video.</span><span class="sxs-lookup"><span data-stu-id="9ef64-107">This attribute is a read/write **Number** (**long**) ranging from 1 to the maximum size accommodated by the width and height of the Video control.</span></span> <span data-ttu-id="9ef64-108">Sa valeur par défaut est 100.</span><span class="sxs-lookup"><span data-stu-id="9ef64-108">It has a default value of 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef64-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9ef64-109">Remarks</span></span>

<span data-ttu-id="9ef64-110">Cet attribut ne peut pas être utilisé conjointement avec l’attribut **fullscreen** .</span><span class="sxs-lookup"><span data-stu-id="9ef64-110">This attribute cannot be used in conjunction with the **fullScreen** attribute.</span></span>

<span data-ttu-id="9ef64-111">Si la **largeur** et la **hauteur** sont spécifiées et que la fenêtre vidéo obtenue est plus grande que la vidéo en cours de lecture, la vidéo peut être agrandie en augmentant jusqu’à la taille maximale prise en charge par la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9ef64-111">If **width** and **height** are specified, and the resulting video window is larger than the video being played, the video can be enlarged by scaling up to the maximum size accommodated by the window.</span></span> <span data-ttu-id="9ef64-112">Si la **largeur** et la **hauteur** ne sont pas spécifiées, le **zoom** est limité aux valeurs 100 ou inférieures.</span><span class="sxs-lookup"><span data-stu-id="9ef64-112">If **width** and **height** are not specified, **zoom** is limited to values of 100 or less.</span></span>

<span data-ttu-id="9ef64-113">Si la propriété **shrinkToFit** a la valeur false, la vidéo change de proportion lors du zoom, pour s’adapter à l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="9ef64-113">If the **shrinkToFit** property is false, the video will change proportion upon zooming, to fit itself to the available space.</span></span> <span data-ttu-id="9ef64-114">Si **shrinkToFit** a la valeur true, la vidéo sera réduite pour s’ajuster à la dimension la plus restrictive, tout en conservant ses proportions d’origine.</span><span class="sxs-lookup"><span data-stu-id="9ef64-114">If **shrinkToFit** is true, the video will shrink to fit within the most restrictive dimension, while retaining its original proportions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef64-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ef64-115">Requirements</span></span>



| <span data-ttu-id="9ef64-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ef64-116">Requirement</span></span> | <span data-ttu-id="9ef64-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ef64-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9ef64-118">Version</span><span class="sxs-lookup"><span data-stu-id="9ef64-118">Version</span></span><br/> | <span data-ttu-id="9ef64-119">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="9ef64-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ef64-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ef64-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef64-121">**Élément VIDEO**</span><span class="sxs-lookup"><span data-stu-id="9ef64-121">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="9ef64-122">**VIDEO. fullScreen**</span><span class="sxs-lookup"><span data-stu-id="9ef64-122">**VIDEO.fullScreen**</span></span>](video-fullscreen.md)
</dt> <dt>

[<span data-ttu-id="9ef64-123">**VIDÉO. shrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="9ef64-123">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> </dl>

 

 





