---
title: BUTTON. hoverImage
description: L’attribut hoverImage spécifie ou récupère l’image affichée lorsque le bouton est à l’État haut et que l’utilisateur place le pointeur de la souris sur celui-ci.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- BUTTON. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523502"
---
# <a name="buttonhoverimage"></a><span data-ttu-id="56be0-104">BUTTON. hoverImage</span><span class="sxs-lookup"><span data-stu-id="56be0-104">BUTTON.hoverImage</span></span>

<span data-ttu-id="56be0-105">L’attribut **hoverImage** spécifie ou récupère l’image affichée lorsque le **bouton** est à l’État haut et que l’utilisateur place le pointeur de la souris sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="56be0-105">The **hoverImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the up state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="56be0-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="56be0-106">Possible Values</span></span>

<span data-ttu-id="56be0-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.</span><span class="sxs-lookup"><span data-stu-id="56be0-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="56be0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="56be0-108">Remarks</span></span>

<span data-ttu-id="56be0-109">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.</span><span class="sxs-lookup"><span data-stu-id="56be0-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="56be0-110">L’image par défaut est celle spécifiée dans l’attribut **image** ou sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="56be0-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="56be0-111">Si l’image de survol est plus grande que la région définie dans l’attribut ambiant, l’image de survol est rognée.</span><span class="sxs-lookup"><span data-stu-id="56be0-111">If the hover image is larger than the defined region in the ambient attribute, the hover image will be cropped.</span></span>

<span data-ttu-id="56be0-112">Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="56be0-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="56be0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56be0-113">Requirements</span></span>



| <span data-ttu-id="56be0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56be0-114">Requirement</span></span> | <span data-ttu-id="56be0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="56be0-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="56be0-116">Version</span><span class="sxs-lookup"><span data-stu-id="56be0-116">Version</span></span><br/> | <span data-ttu-id="56be0-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="56be0-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56be0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56be0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56be0-119">**BUTTON, élément**</span><span class="sxs-lookup"><span data-stu-id="56be0-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="56be0-120">**BOUTON. image**</span><span class="sxs-lookup"><span data-stu-id="56be0-120">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





