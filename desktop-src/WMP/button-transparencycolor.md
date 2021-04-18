---
title: BUTTON. transparencyColor
description: L’attribut transparencyColor spécifie ou récupère la couleur qui sera transparente dans les images de bouton.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- BUTTON. transparencyColor lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528994"
---
# <a name="buttontransparencycolor"></a><span data-ttu-id="f9357-104">BUTTON. transparencyColor</span><span class="sxs-lookup"><span data-stu-id="f9357-104">BUTTON.transparencyColor</span></span>

<span data-ttu-id="f9357-105">L’attribut **transparencyColor** spécifie ou récupère la couleur qui sera transparente dans les images de **bouton** .</span><span class="sxs-lookup"><span data-stu-id="f9357-105">The **transparencyColor** attribute specifies or retrieves the color that will be transparent in the **BUTTON** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="f9357-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="f9357-106">Possible Values</span></span>

<span data-ttu-id="f9357-107">Cet attribut est une **chaîne** en lecture/écriture sans valeur par défaut contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f9357-107">This attribute is a read/write **String** with no default containing one of the following values.</span></span>



| <span data-ttu-id="f9357-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9357-108">Value</span></span>                                    | <span data-ttu-id="f9357-109">Description</span><span class="sxs-lookup"><span data-stu-id="f9357-109">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9357-110">Auto</span><span class="sxs-lookup"><span data-stu-id="f9357-110">Auto</span></span>                                     | <span data-ttu-id="f9357-111">La couleur du pixel à l’emplacement 0, 0 dans l’image devient la couleur transparente.</span><span class="sxs-lookup"><span data-stu-id="f9357-111">The color of the pixel at location 0,0 in the image becomes the transparent color.</span></span>                        |
| <span data-ttu-id="f9357-112">Toute valeur de format de couleur Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f9357-112">Any Internet Explorer color format value</span></span> | <span data-ttu-id="f9357-113">Une valeur de format de couleur d’Internet Explorer devient la couleur transparente (par exemple, « rouge » ou « \# FF0000 »).</span><span class="sxs-lookup"><span data-stu-id="f9357-113">An Internet Explorer color format value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="f9357-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="f9357-114">None</span></span>                                     | <span data-ttu-id="f9357-115">Aucune transparence.</span><span class="sxs-lookup"><span data-stu-id="f9357-115">No transparency.</span></span>                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="f9357-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f9357-116">Remarks</span></span>

<span data-ttu-id="f9357-117">Une couleur transparente dans une image permet à tout ce qui se trouve derrière l’image de s’afficher dans les zones transparentes.</span><span class="sxs-lookup"><span data-stu-id="f9357-117">A transparent color in an image allows whatever is behind the image to show through the transparent areas.</span></span> <span data-ttu-id="f9357-118">Le **bouton** continuera de recevoir des clics sur la zone transparente.</span><span class="sxs-lookup"><span data-stu-id="f9357-118">The **BUTTON** will still receive clicks on the transparent region.</span></span>

<span data-ttu-id="f9357-119">La couleur transparente peut être n’importe quelle valeur de couleur Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f9357-119">The transparent color can be any Internet Explorer color value.</span></span> <span data-ttu-id="f9357-120">Si la valeur de l’attribut **transparencyColor** est définie sur « auto », la couleur du pixel à l’emplacement 0, 0 dans l’image est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f9357-120">If the value of the **transparencyColor** attribute is set to "Auto", the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="f9357-121">Si la couleur spécifiée ne fait pas partie des couleurs IE valides, la valeur précédente est conservée.</span><span class="sxs-lookup"><span data-stu-id="f9357-121">If the color specified is not one of the valid IE colors, the previous value is maintained.</span></span>

<span data-ttu-id="f9357-122">Étant donné que les JPGs sont perdus et, par conséquent, soumis à une modification de couleur inattendue, ils ne sont pas recommandés lorsque **transparencyColor** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f9357-122">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9357-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9357-123">Requirements</span></span>



| <span data-ttu-id="f9357-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9357-124">Requirement</span></span> | <span data-ttu-id="f9357-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9357-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f9357-126">Version</span><span class="sxs-lookup"><span data-stu-id="f9357-126">Version</span></span><br/> | <span data-ttu-id="f9357-127">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="f9357-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9357-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9357-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9357-129">**BUTTON, élément**</span><span class="sxs-lookup"><span data-stu-id="f9357-129">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="f9357-130">**BOUTON. image**</span><span class="sxs-lookup"><span data-stu-id="f9357-130">**BUTTON.image**</span></span>](button-image.md)
</dt> <dt>

[<span data-ttu-id="f9357-131">**Référence de couleur**</span><span class="sxs-lookup"><span data-stu-id="f9357-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





