---
title: BUTTON. hoverDownImage
description: L’attribut hoverDownImage spécifie ou récupère l’image affichée lorsque le bouton est à l’état inactif et que l’utilisateur pointe dessus avec le pointeur de la souris.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- BUTTON. hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545379"
---
# <a name="buttonhoverdownimage"></a><span data-ttu-id="356b5-104">BUTTON. hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="356b5-104">BUTTON.hoverDownImage</span></span>

<span data-ttu-id="356b5-105">L’attribut **hoverDownImage** spécifie ou récupère l’image affichée lorsque le **bouton** est à l’état inactif et que l’utilisateur pointe dessus avec le pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="356b5-105">The **hoverDownImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the down state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="356b5-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="356b5-106">Possible Values</span></span>

<span data-ttu-id="356b5-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.</span><span class="sxs-lookup"><span data-stu-id="356b5-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="356b5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="356b5-108">Remarks</span></span>

<span data-ttu-id="356b5-109">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.</span><span class="sxs-lookup"><span data-stu-id="356b5-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="356b5-110">L’image par défaut est celle spécifiée dans l’attribut **downImage** ou sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="356b5-110">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="356b5-111">Si l’image de survol est plus grande que la région définie dans l’attribut ambiant, l’image de survol est rognée.</span><span class="sxs-lookup"><span data-stu-id="356b5-111">If the hover-down image is larger than the defined region in the ambient attribute, the hover-down image will be cropped.</span></span>

<span data-ttu-id="356b5-112">Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="356b5-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="356b5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="356b5-113">Requirements</span></span>



| <span data-ttu-id="356b5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="356b5-114">Requirement</span></span> | <span data-ttu-id="356b5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="356b5-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="356b5-116">Version</span><span class="sxs-lookup"><span data-stu-id="356b5-116">Version</span></span><br/> | <span data-ttu-id="356b5-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="356b5-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="356b5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="356b5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="356b5-119">**BUTTON, élément**</span><span class="sxs-lookup"><span data-stu-id="356b5-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="356b5-120">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="356b5-120">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





