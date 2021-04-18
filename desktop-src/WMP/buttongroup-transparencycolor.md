---
title: BUTTONGROUP. transparencyColor
description: L’attribut transparencyColor spécifie ou récupère la couleur transparente des images BUTTONGROUP.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- Lecteur Windows Media BUTTONGROUP. transparencyColor
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526030"
---
# <a name="buttongrouptransparencycolor"></a><span data-ttu-id="82b69-104">BUTTONGROUP. transparencyColor</span><span class="sxs-lookup"><span data-stu-id="82b69-104">BUTTONGROUP.transparencyColor</span></span>

<span data-ttu-id="82b69-105">L’attribut **transparencyColor** spécifie ou récupère la couleur transparente des images **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="82b69-105">The **transparencyColor** attribute specifies or retrieves the transparent color of the **BUTTONGROUP** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="82b69-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="82b69-106">Possible Values</span></span>

<span data-ttu-id="82b69-107">Cet attribut est une **chaîne** en lecture/écriture sans valeur par défaut, contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="82b69-107">This attribute is a read/write **String** with no default, containing one of the following values.</span></span>



| <span data-ttu-id="82b69-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="82b69-108">Value</span></span>                                       | <span data-ttu-id="82b69-109">Description</span><span class="sxs-lookup"><span data-stu-id="82b69-109">Description</span></span>                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b69-110">Auto</span><span class="sxs-lookup"><span data-stu-id="82b69-110">Auto</span></span>                                        | <span data-ttu-id="82b69-111">Le pixel à l’emplacement 0, 0 dans l’image devient la couleur transparente.</span><span class="sxs-lookup"><span data-stu-id="82b69-111">The pixel at location 0,0 in the image becomes the transparent color.</span></span>                              |
| <span data-ttu-id="82b69-112">toute valeur de couleur Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="82b69-112">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="82b69-113">Une valeur de couleur d’Internet Explorer devient la couleur transparente (par exemple, « rouge » ou « \# FF0000 »).</span><span class="sxs-lookup"><span data-stu-id="82b69-113">An Internet Explorer color value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="82b69-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="82b69-114">None</span></span>                                        | <span data-ttu-id="82b69-115">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="82b69-115">Default.</span></span> <span data-ttu-id="82b69-116">Aucune transparence.</span><span class="sxs-lookup"><span data-stu-id="82b69-116">No transparency.</span></span>                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="82b69-117">Notes</span><span class="sxs-lookup"><span data-stu-id="82b69-117">Remarks</span></span>

<span data-ttu-id="82b69-118">Une couleur transparente dans une image permet à tout ce qui se trouve derrière l’image de s’afficher dans les zones de transparence.</span><span class="sxs-lookup"><span data-stu-id="82b69-118">A transparent color in an image will allow whatever is behind the image to show through the areas of transparency.</span></span> <span data-ttu-id="82b69-119">La région transparente est cliquable, sauf si elle est découpée par la balise **clippingImage** .</span><span class="sxs-lookup"><span data-stu-id="82b69-119">The transparent region is clickable unless clipped by the **clippingImage** tag.</span></span>

<span data-ttu-id="82b69-120">La couleur peut être n’importe quelle valeur de couleur Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="82b69-120">The color can be any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="82b69-121">Si la valeur est auto, la couleur du pixel à l’emplacement 0, 0 dans l’image est utilisée.</span><span class="sxs-lookup"><span data-stu-id="82b69-121">If the value is Auto, then the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="82b69-122">Si la couleur spécifiée ne fait pas partie des couleurs Internet Explorer valides, un avertissement est renvoyé et la valeur précédente est conservée.</span><span class="sxs-lookup"><span data-stu-id="82b69-122">If the color specified is not one of the valid Internet Explorer colors, a warning is returned and the previous value is maintained.</span></span>

<span data-ttu-id="82b69-123">Étant donné que les JPGs sont perdus et, par conséquent, soumis à une modification de couleur inattendue, ils ne sont pas recommandés lorsque **transparencyColor** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="82b69-123">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b69-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82b69-124">Requirements</span></span>



| <span data-ttu-id="82b69-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82b69-125">Requirement</span></span> | <span data-ttu-id="82b69-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="82b69-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="82b69-127">Version</span><span class="sxs-lookup"><span data-stu-id="82b69-127">Version</span></span><br/> | <span data-ttu-id="82b69-128">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="82b69-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82b69-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82b69-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b69-130">**Élément BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="82b69-130">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="82b69-131">**Référence de couleur**</span><span class="sxs-lookup"><span data-stu-id="82b69-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





