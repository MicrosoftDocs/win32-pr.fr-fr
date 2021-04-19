---
title: TEXT. fontStyle
description: L’attribut fontStyle spécifie ou récupère le style de police pour le contrôle de texte.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- TEXT. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545366"
---
# <a name="textfontstyle"></a><span data-ttu-id="831a8-104">TEXT. fontStyle</span><span class="sxs-lookup"><span data-stu-id="831a8-104">TEXT.fontStyle</span></span>

<span data-ttu-id="831a8-105">L’attribut **FontStyle** spécifie ou récupère le style de police pour le contrôle de texte.</span><span class="sxs-lookup"><span data-stu-id="831a8-105">The **fontStyle** attribute specifies or retrieves the font style for the Text control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="831a8-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="831a8-106">Possible Values</span></span>

<span data-ttu-id="831a8-107">Cet attribut est une **chaîne** en lecture/écriture contenant une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="831a8-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="831a8-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="831a8-108">Value</span></span>     | <span data-ttu-id="831a8-109">Description</span><span class="sxs-lookup"><span data-stu-id="831a8-109">Description</span></span>                 |
|-----------|-----------------------------|
| <span data-ttu-id="831a8-110">Gras</span><span class="sxs-lookup"><span data-stu-id="831a8-110">Bold</span></span>      | <span data-ttu-id="831a8-111">Style de police gras.</span><span class="sxs-lookup"><span data-stu-id="831a8-111">Bold font style.</span></span>            |
| <span data-ttu-id="831a8-112">Italique</span><span class="sxs-lookup"><span data-stu-id="831a8-112">Italic</span></span>    | <span data-ttu-id="831a8-113">Style de police en italique.</span><span class="sxs-lookup"><span data-stu-id="831a8-113">Italic font style.</span></span>          |
| <span data-ttu-id="831a8-114">Souligner</span><span class="sxs-lookup"><span data-stu-id="831a8-114">Underline</span></span> | <span data-ttu-id="831a8-115">Style de police souligné.</span><span class="sxs-lookup"><span data-stu-id="831a8-115">Underline font style.</span></span>       |
| <span data-ttu-id="831a8-116">Barré</span><span class="sxs-lookup"><span data-stu-id="831a8-116">Strikeout</span></span> | <span data-ttu-id="831a8-117">Style de police barré.</span><span class="sxs-lookup"><span data-stu-id="831a8-117">Strikeout font style.</span></span>       |
| <span data-ttu-id="831a8-118">Normal</span><span class="sxs-lookup"><span data-stu-id="831a8-118">Normal</span></span>    | <span data-ttu-id="831a8-119">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="831a8-119">Default.</span></span> <span data-ttu-id="831a8-120">Style de police normal.</span><span class="sxs-lookup"><span data-stu-id="831a8-120">Normal font style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="831a8-121">Notes</span><span class="sxs-lookup"><span data-stu-id="831a8-121">Remarks</span></span>

<span data-ttu-id="831a8-122">Vous pouvez utiliser n’importe quelle combinaison de valeurs, en les séparant par des espaces.</span><span class="sxs-lookup"><span data-stu-id="831a8-122">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="831a8-123">Le style normal est prioritaire sur toutes les autres valeurs, et les autres valeurs spécifiées en même temps que normal seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="831a8-123">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="831a8-124">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="831a8-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="831a8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="831a8-125">Requirements</span></span>



| <span data-ttu-id="831a8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="831a8-126">Requirement</span></span> | <span data-ttu-id="831a8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="831a8-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="831a8-128">Version</span><span class="sxs-lookup"><span data-stu-id="831a8-128">Version</span></span><br/> | <span data-ttu-id="831a8-129">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="831a8-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="831a8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="831a8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="831a8-131">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="831a8-131">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





