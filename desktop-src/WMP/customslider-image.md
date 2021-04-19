---
title: CUSTOMSLIDER. image
description: L’attribut image spécifie ou récupère le nom du fichier contenant les images correspondant aux différents États du curseur personnalisé.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- Lecteur Windows Media CUSTOMSLIDER. image
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540959"
---
# <a name="customsliderimage"></a><span data-ttu-id="9d999-104">CUSTOMSLIDER. image</span><span class="sxs-lookup"><span data-stu-id="9d999-104">CUSTOMSLIDER.image</span></span>

<span data-ttu-id="9d999-105">L’attribut **image** spécifie ou récupère le nom du fichier contenant les images correspondant aux différents États du curseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9d999-105">The **image** attribute specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="9d999-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9d999-106">Possible Values</span></span>

<span data-ttu-id="9d999-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="9d999-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d999-108">Notes</span><span class="sxs-lookup"><span data-stu-id="9d999-108">Remarks</span></span>

<span data-ttu-id="9d999-109">L’attribut **image** est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9d999-109">The **image** attribute is required.</span></span> <span data-ttu-id="9d999-110">Il spécifie un fichier image qui se compose d’une ou de plusieurs sous-images, agencées horizontalement ou verticalement, représentant les différents États du curseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9d999-110">It specifies an image file that consists of one or more sub-images, arranged either horizontally or vertically, representing the various states of the custom slider.</span></span> <span data-ttu-id="9d999-111">Chaque sous-image doit avoir les mêmes dimensions que le **positionImage** ou le curseur personnalisé ne fonctionnera pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9d999-111">Each sub-image must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span> <span data-ttu-id="9d999-112">La hauteur ou la largeur de l’image globale doit donc être un multiple pair de la hauteur ou de la largeur du **positionImage**.</span><span class="sxs-lookup"><span data-stu-id="9d999-112">The height or width of the overall image must therefore be an even multiple of the height or width of the **positionImage**.</span></span>

<span data-ttu-id="9d999-113">Les types de fichiers image pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).</span><span class="sxs-lookup"><span data-stu-id="9d999-113">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="9d999-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="9d999-114">Examples</span></span>

<span data-ttu-id="9d999-115">Voici un exemple d’image de curseur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="9d999-115">The following is an example of a custom slider image.</span></span> <span data-ttu-id="9d999-116">Le **positionImage** correspondant est affiché dans la section exemple de la propriété **positionImage** .</span><span class="sxs-lookup"><span data-stu-id="9d999-116">The corresponding **positionImage** is shown in the example section of the **positionImage** property.</span></span>

![exemple d’image customslider](images/dial.png)

<span data-ttu-id="9d999-118">L’attribut **positionImage** contient également un exemple de code illustrant la façon dont les attributs de l’élément **CUSTOMSLIDER** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="9d999-118">The **positionImage** attribute also contains a code sample illustrating how the attributes of the **CUSTOMSLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d999-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d999-119">Requirements</span></span>



| <span data-ttu-id="9d999-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d999-120">Requirement</span></span> | <span data-ttu-id="9d999-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d999-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9d999-122">Version</span><span class="sxs-lookup"><span data-stu-id="9d999-122">Version</span></span><br/> | <span data-ttu-id="9d999-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="9d999-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d999-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d999-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d999-125">**Élément CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="9d999-125">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="9d999-126">**CUSTOMSLIDER.positionImage**</span><span class="sxs-lookup"><span data-stu-id="9d999-126">**CUSTOMSLIDER.positionImage**</span></span>](customslider-positionimage.md)
</dt> </dl>

 

 





