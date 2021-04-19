---
title: EDITBOX. fontStyle
description: L’attribut fontStyle spécifie ou récupère le style de police pour le contrôle zone d’édition.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- EDITBOX. fontStyle lecteur Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525351"
---
# <a name="editboxfontstyle"></a><span data-ttu-id="16aa0-104">EDITBOX. fontStyle</span><span class="sxs-lookup"><span data-stu-id="16aa0-104">EDITBOX.fontStyle</span></span>

<span data-ttu-id="16aa0-105">L’attribut **FontStyle** spécifie ou récupère le style de police pour le contrôle zone d’édition.</span><span class="sxs-lookup"><span data-stu-id="16aa0-105">The **fontStyle** attribute specifies or retrieves the font style for the edit box control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="16aa0-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="16aa0-106">Possible Values</span></span>

<span data-ttu-id="16aa0-107">Cet attribut est une **chaîne** en lecture/écriture contenant une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="16aa0-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="16aa0-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="16aa0-108">Value</span></span>     | <span data-ttu-id="16aa0-109">Description</span><span class="sxs-lookup"><span data-stu-id="16aa0-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="16aa0-110">Gras</span><span class="sxs-lookup"><span data-stu-id="16aa0-110">Bold</span></span>      | <span data-ttu-id="16aa0-111">Style de police gras.</span><span class="sxs-lookup"><span data-stu-id="16aa0-111">Bold font style.</span></span>      |
| <span data-ttu-id="16aa0-112">Italique</span><span class="sxs-lookup"><span data-stu-id="16aa0-112">Italic</span></span>    | <span data-ttu-id="16aa0-113">Style de police en italique.</span><span class="sxs-lookup"><span data-stu-id="16aa0-113">Italic font style.</span></span>    |
| <span data-ttu-id="16aa0-114">Souligner</span><span class="sxs-lookup"><span data-stu-id="16aa0-114">Underline</span></span> | <span data-ttu-id="16aa0-115">Style de police souligné.</span><span class="sxs-lookup"><span data-stu-id="16aa0-115">Underline font style.</span></span> |
| <span data-ttu-id="16aa0-116">Barré</span><span class="sxs-lookup"><span data-stu-id="16aa0-116">Strikeout</span></span> | <span data-ttu-id="16aa0-117">Style de police barré.</span><span class="sxs-lookup"><span data-stu-id="16aa0-117">Strikeout font style.</span></span> |
| <span data-ttu-id="16aa0-118">Normal</span><span class="sxs-lookup"><span data-stu-id="16aa0-118">Normal</span></span>    | <span data-ttu-id="16aa0-119">Style de police normal.</span><span class="sxs-lookup"><span data-stu-id="16aa0-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="16aa0-120">Notes</span><span class="sxs-lookup"><span data-stu-id="16aa0-120">Remarks</span></span>

<span data-ttu-id="16aa0-121">Vous pouvez utiliser n’importe quelle combinaison de valeurs, en les séparant par des espaces.</span><span class="sxs-lookup"><span data-stu-id="16aa0-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="16aa0-122">Le style normal est prioritaire sur toutes les autres valeurs, et les autres valeurs spécifiées en même temps que normal seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="16aa0-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="16aa0-123">À des fins de rendu, normal est le style de police par défaut.</span><span class="sxs-lookup"><span data-stu-id="16aa0-123">For rendering purposes, Normal is the default font style.</span></span> <span data-ttu-id="16aa0-124">La valeur par défaut Récupérée à partir de cet attribut est "" (chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="16aa0-124">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="16aa0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16aa0-125">Requirements</span></span>



| <span data-ttu-id="16aa0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16aa0-126">Requirement</span></span> | <span data-ttu-id="16aa0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="16aa0-127">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="16aa0-128">Version</span><span class="sxs-lookup"><span data-stu-id="16aa0-128">Version</span></span><br/> | <span data-ttu-id="16aa0-129">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="16aa0-129">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16aa0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16aa0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16aa0-131">**Élément EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="16aa0-131">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="16aa0-132">**EDITBOX. fontFace**</span><span class="sxs-lookup"><span data-stu-id="16aa0-132">**EDITBOX.fontFace**</span></span>](editbox-fontface.md)
</dt> <dt>

[<span data-ttu-id="16aa0-133">**EDITBOX. FontSize**</span><span class="sxs-lookup"><span data-stu-id="16aa0-133">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> </dl>

 

 





