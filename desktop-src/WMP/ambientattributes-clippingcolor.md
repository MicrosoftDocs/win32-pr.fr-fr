---
title: AmbientAttributes.clippingColor
description: L’attribut clippingColor spécifie ou récupère la couleur à découper de la bitmap clippingImage.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- Lecteur Windows Media AmbientAttributes. clippingColor
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529963"
---
# <a name="ambientattributesclippingcolor"></a><span data-ttu-id="ebd19-104">AmbientAttributes.clippingColor</span><span class="sxs-lookup"><span data-stu-id="ebd19-104">AmbientAttributes.clippingColor</span></span>

<span data-ttu-id="ebd19-105">L’attribut **clippingColor** spécifie ou récupère la couleur à découper de la bitmap **clippingImage** .</span><span class="sxs-lookup"><span data-stu-id="ebd19-105">The **clippingColor** attribute specifies or retrieves the color to clip out from the **clippingImage** bitmap.</span></span>

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a><span data-ttu-id="ebd19-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="ebd19-106">Possible Values</span></span>

<span data-ttu-id="ebd19-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ebd19-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="ebd19-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebd19-108">Value</span></span>                                       | <span data-ttu-id="ebd19-109">Description</span><span class="sxs-lookup"><span data-stu-id="ebd19-109">Description</span></span>                                       |
|---------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ebd19-110">Auto</span><span class="sxs-lookup"><span data-stu-id="ebd19-110">Auto</span></span>                                        | <span data-ttu-id="ebd19-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="ebd19-111">Default.</span></span> <span data-ttu-id="ebd19-112">La couleur de l’emplacement de pixel 0 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ebd19-112">The color at pixel location 0,0 is used.</span></span> |
| <span data-ttu-id="ebd19-113">toute valeur de couleur Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="ebd19-113">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="ebd19-114">La couleur Internet Explorer spécifiée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ebd19-114">The specified Internet Explorer color is used.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="ebd19-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ebd19-115">Remarks</span></span>

<span data-ttu-id="ebd19-116">La couleur de découpage indique les régions du **clippingImage** (ou **BackgroundImage** pour la **vue** ou la sous- **vue**) qui correspondent à des portions transparentes et non intercliquables du contrôle.</span><span class="sxs-lookup"><span data-stu-id="ebd19-116">The clipping color indicates the regions of the **clippingImage** (or **backgroundImage** for **VIEW** or **SUBVIEW**) that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="ebd19-117">La couleur de découpage peut indiquer plusieurs régions à découper. Un avertissement est émis si **clippingImage** est un jpg pour signaler une perte de couleur dans jpgs.</span><span class="sxs-lookup"><span data-stu-id="ebd19-117">The clipping color can indicate multiple regions to be clipped out. A warning is issued if the **clippingImage** is a JPG to warn of loss of color in JPGs.</span></span>

<span data-ttu-id="ebd19-118">L’attribut **clippingColor** n’est pas pris en charge par l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="ebd19-118">The **clippingColor** attribute is not supported by the **PLAYLIST** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd19-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebd19-119">Requirements</span></span>



| <span data-ttu-id="ebd19-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebd19-120">Requirement</span></span> | <span data-ttu-id="ebd19-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebd19-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ebd19-122">Version</span><span class="sxs-lookup"><span data-stu-id="ebd19-122">Version</span></span><br/> | <span data-ttu-id="ebd19-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="ebd19-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebd19-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebd19-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd19-125">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="ebd19-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="ebd19-126">**AmbientAttributes.clippingImage**</span><span class="sxs-lookup"><span data-stu-id="ebd19-126">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> <dt>

[<span data-ttu-id="ebd19-127">**Référence de couleur**</span><span class="sxs-lookup"><span data-stu-id="ebd19-127">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





