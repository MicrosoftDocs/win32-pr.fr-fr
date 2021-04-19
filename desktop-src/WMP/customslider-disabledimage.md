---
title: CUSTOMSLIDER.disabledImage
description: L’attribut disabledImage spécifie ou récupère l’image du curseur utilisé lorsque le curseur est désactivé.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- Lecteur Windows Media CUSTOMSLIDER. disabledImage
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169057d952170fb92c4e3a98617c7db22f5456b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542713"
---
# <a name="customsliderdisabledimage"></a><span data-ttu-id="a877c-104">CUSTOMSLIDER.disabledImage</span><span class="sxs-lookup"><span data-stu-id="a877c-104">CUSTOMSLIDER.disabledImage</span></span>

<span data-ttu-id="a877c-105">L’attribut **disabledImage** spécifie ou récupère l’image du curseur utilisé lorsque le curseur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a877c-105">The **disabledImage** attribute specifies or retrieves the image of the slider used when the slider is disabled.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="a877c-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="a877c-106">Possible Values</span></span>

<span data-ttu-id="a877c-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="a877c-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="a877c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a877c-108">Remarks</span></span>

<span data-ttu-id="a877c-109">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a877c-109">This attribute is optional.</span></span> <span data-ttu-id="a877c-110">S’il n’est pas spécifié, le fichier spécifié dans l’attribut **image** sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="a877c-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="a877c-111">**DisabledImage** représente l’état désactivé du contrôle **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="a877c-111">The **disabledImage** represents the disabled state of the **CUSTOMSLIDER** control.</span></span> <span data-ttu-id="a877c-112">Il peut s’agir d’une image unique ou d’une série d’images représentant les différents États du curseur.</span><span class="sxs-lookup"><span data-stu-id="a877c-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="a877c-113">Si plusieurs images sont utilisées, elles sont organisées de la même façon que le fichier **image** .</span><span class="sxs-lookup"><span data-stu-id="a877c-113">If multiple images are used, they are arranged in the same way as the **image** file.</span></span>

<span data-ttu-id="a877c-114">Les types de fichiers image pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).</span><span class="sxs-lookup"><span data-stu-id="a877c-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="a877c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a877c-115">Requirements</span></span>



| <span data-ttu-id="a877c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a877c-116">Requirement</span></span> | <span data-ttu-id="a877c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a877c-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a877c-118">Version</span><span class="sxs-lookup"><span data-stu-id="a877c-118">Version</span></span><br/> | <span data-ttu-id="a877c-119">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="a877c-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a877c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a877c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a877c-121">**Élément CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="a877c-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="a877c-122">**CUSTOMSLIDER. image**</span><span class="sxs-lookup"><span data-stu-id="a877c-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





