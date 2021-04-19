---
title: TEXT. backgroundColor
description: L’attribut backgroundColor spécifie ou récupère la couleur d’arrière-plan du contrôle de texte.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- TEXT. backgroundColor lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540948"
---
# <a name="textbackgroundcolor"></a><span data-ttu-id="3ee0f-104">TEXT. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="3ee0f-104">TEXT.backgroundColor</span></span>

<span data-ttu-id="3ee0f-105">L’attribut **backgroundColor** spécifie ou récupère la couleur d’arrière-plan du contrôle de texte.</span><span class="sxs-lookup"><span data-stu-id="3ee0f-105">The **backgroundColor** attribute specifies or retrieves the background color for the Text control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="3ee0f-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="3ee0f-106">Possible Values</span></span>

<span data-ttu-id="3ee0f-107">Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer ou la valeur « None ».</span><span class="sxs-lookup"><span data-stu-id="3ee0f-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="3ee0f-108">Sa valeur par défaut est « None », ce qui signifie que l’arrière-plan est transparent.</span><span class="sxs-lookup"><span data-stu-id="3ee0f-108">It has a default value of "none", which means the background is transparent.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ee0f-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3ee0f-109">Remarks</span></span>

<span data-ttu-id="3ee0f-110">La couleur d’arrière-plan est définie pour la hauteur et la largeur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="3ee0f-110">The background color is set for the height and width of the control.</span></span> <span data-ttu-id="3ee0f-111">Si la hauteur et la largeur ne sont pas définies, la couleur d’arrière-plan est définie sur la hauteur et la largeur du texte.</span><span class="sxs-lookup"><span data-stu-id="3ee0f-111">If height and width are not set, the background color is set to the height and width of the text.</span></span>

<span data-ttu-id="3ee0f-112">Quand vous utilisez **alphaBlend** ou **alphaBlendTo** avec un élément de **texte** pour lequel le **backgroundColor** n’est pas spécifié, une couleur d’arrière-plan noire est utilisée.</span><span class="sxs-lookup"><span data-stu-id="3ee0f-112">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="3ee0f-113">Si la couleur de premier plan est également noire (valeur par défaut pour l’attribut **foregroundColor** ), votre texte peut devenir illisible.</span><span class="sxs-lookup"><span data-stu-id="3ee0f-113">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="3ee0f-114">Pour éviter cela, spécifiez toujours l’attribut **backgroundColor** ou définissez **foregroundColor** sur une couleur autre que Black.</span><span class="sxs-lookup"><span data-stu-id="3ee0f-114">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

<span data-ttu-id="3ee0f-115">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="3ee0f-115">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ee0f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ee0f-116">Requirements</span></span>



| <span data-ttu-id="3ee0f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ee0f-117">Requirement</span></span> | <span data-ttu-id="3ee0f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ee0f-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3ee0f-119">Version</span><span class="sxs-lookup"><span data-stu-id="3ee0f-119">Version</span></span><br/> | <span data-ttu-id="3ee0f-120">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="3ee0f-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ee0f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ee0f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee0f-122">**AmbientAttributes. alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="3ee0f-122">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="3ee0f-123">**AmbientAttributes.alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="3ee0f-123">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="3ee0f-124">**Référence de couleur**</span><span class="sxs-lookup"><span data-stu-id="3ee0f-124">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="3ee0f-125">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="3ee0f-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="3ee0f-126">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="3ee0f-126">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





