---
title: TEXT. hoverFontStyle
description: L’attribut hoverFontStyle spécifie ou récupère le style de police utilisé pour le contrôle de texte lorsque le curseur de la souris pointe dessus.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- TEXT. hoverFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeed6d9701b6e81ac91bc5292dc5b431aa70d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535910"
---
# <a name="texthoverfontstyle"></a><span data-ttu-id="ebc4f-104">TEXT. hoverFontStyle</span><span class="sxs-lookup"><span data-stu-id="ebc4f-104">TEXT.hoverFontStyle</span></span>

<span data-ttu-id="ebc4f-105">L’attribut **hoverFontStyle** spécifie ou récupère le style de police utilisé pour le contrôle de texte lorsque le curseur de la souris pointe dessus.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-105">The **hoverFontStyle** attribute specifies or retrieves the font style used for the Text control when the mouse cursor hovers over it.</span></span>

``` syntax
        elementID.hoverFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="ebc4f-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="ebc4f-106">Possible Values</span></span>

<span data-ttu-id="ebc4f-107">Cet attribut est une **chaîne** en lecture/écriture contenant une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="ebc4f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebc4f-108">Value</span></span>     | <span data-ttu-id="ebc4f-109">Description</span><span class="sxs-lookup"><span data-stu-id="ebc4f-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="ebc4f-110">Gras</span><span class="sxs-lookup"><span data-stu-id="ebc4f-110">Bold</span></span>      | <span data-ttu-id="ebc4f-111">Style de police gras.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-111">Bold font style.</span></span>      |
| <span data-ttu-id="ebc4f-112">Italique</span><span class="sxs-lookup"><span data-stu-id="ebc4f-112">Italic</span></span>    | <span data-ttu-id="ebc4f-113">Style de police en italique.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-113">Italic font style.</span></span>    |
| <span data-ttu-id="ebc4f-114">Souligner</span><span class="sxs-lookup"><span data-stu-id="ebc4f-114">Underline</span></span> | <span data-ttu-id="ebc4f-115">Style de police souligné.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-115">Underline font style.</span></span> |
| <span data-ttu-id="ebc4f-116">Barré</span><span class="sxs-lookup"><span data-stu-id="ebc4f-116">Strikeout</span></span> | <span data-ttu-id="ebc4f-117">Style de police barré.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-117">Strikeout font style.</span></span> |
| <span data-ttu-id="ebc4f-118">Normal</span><span class="sxs-lookup"><span data-stu-id="ebc4f-118">Normal</span></span>    | <span data-ttu-id="ebc4f-119">Style de police normal.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="ebc4f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ebc4f-120">Remarks</span></span>

<span data-ttu-id="ebc4f-121">Vous pouvez utiliser n’importe quelle combinaison de valeurs, en les séparant par des espaces.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="ebc4f-122">Le style normal est prioritaire sur toutes les autres valeurs, et les autres valeurs spécifiées en même temps que normal seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="ebc4f-123">Si **hoverFontStyle** n’est pas spécifié, **FontStyle** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-123">If **hoverFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="ebc4f-124">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="ebc4f-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebc4f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebc4f-125">Requirements</span></span>



| <span data-ttu-id="ebc4f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebc4f-126">Requirement</span></span> | <span data-ttu-id="ebc4f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebc4f-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ebc4f-128">Version</span><span class="sxs-lookup"><span data-stu-id="ebc4f-128">Version</span></span><br/> | <span data-ttu-id="ebc4f-129">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="ebc4f-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebc4f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebc4f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc4f-131">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="ebc4f-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="ebc4f-132">**TEXT. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="ebc4f-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





