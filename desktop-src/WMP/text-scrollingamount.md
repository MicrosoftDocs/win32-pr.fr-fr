---
title: TEXT. scrollingAmount
description: L’attribut scrollingAmount spécifie ou récupère le nombre de pixels que le texte déplace au cours de chaque mouvement de défilement.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- TEXT. scrollingAmount Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526101"
---
# <a name="textscrollingamount"></a><span data-ttu-id="c75da-104">TEXT. scrollingAmount</span><span class="sxs-lookup"><span data-stu-id="c75da-104">TEXT.scrollingAmount</span></span>

<span data-ttu-id="c75da-105">L’attribut **scrollingAmount** spécifie ou récupère le nombre de pixels que le texte déplace au cours de chaque mouvement de défilement.</span><span class="sxs-lookup"><span data-stu-id="c75da-105">The **scrollingAmount** attribute specifies or retrieves the number of pixels that the text moves during each scrolling movement.</span></span>

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a><span data-ttu-id="c75da-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c75da-106">Possible Values</span></span>

<span data-ttu-id="c75da-107">Cet attribut est un **nombre** en lecture/écriture positif (**int**) avec une valeur par défaut de 6.</span><span class="sxs-lookup"><span data-stu-id="c75da-107">This attribute is a positive read/write **Number** (**int**) with a default value of 6.</span></span>

## <a name="remarks"></a><span data-ttu-id="c75da-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c75da-108">Remarks</span></span>

<span data-ttu-id="c75da-109">Pour le défilement Smooth, **scrollingAmount** doit être petit.</span><span class="sxs-lookup"><span data-stu-id="c75da-109">For smooth scrolling, **scrollingAmount** should be small.</span></span> <span data-ttu-id="c75da-110">Pour un dessin rapide avec de grands écarts, le **scrollingAmount** doit être plus grand.</span><span class="sxs-lookup"><span data-stu-id="c75da-110">For fast drawing with big gaps, the **scrollingAmount** should be larger.</span></span> <span data-ttu-id="c75da-111">Si le **défilement** = « false », **scrollingAmount** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="c75da-111">If **scrolling** ="false", **scrollingAmount** is ignored.</span></span>

<span data-ttu-id="c75da-112">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="c75da-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75da-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c75da-113">Requirements</span></span>



| <span data-ttu-id="c75da-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c75da-114">Requirement</span></span> | <span data-ttu-id="c75da-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c75da-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c75da-116">Version</span><span class="sxs-lookup"><span data-stu-id="c75da-116">Version</span></span><br/> | <span data-ttu-id="c75da-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="c75da-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c75da-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c75da-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75da-119">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="c75da-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="c75da-120">**TEXTE. défilement**</span><span class="sxs-lookup"><span data-stu-id="c75da-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





