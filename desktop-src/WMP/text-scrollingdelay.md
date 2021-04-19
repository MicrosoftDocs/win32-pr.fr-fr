---
title: TEXT. scrollingDelay
description: L’attribut scrollingDelay spécifie ou récupère le délai entre les mouvements de défilement.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- TEXT. scrollingDelay Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541136"
---
# <a name="textscrollingdelay"></a><span data-ttu-id="f078a-104">TEXT. scrollingDelay</span><span class="sxs-lookup"><span data-stu-id="f078a-104">TEXT.scrollingDelay</span></span>

<span data-ttu-id="f078a-105">L’attribut **scrollingDelay** spécifie ou récupère le délai entre les mouvements de défilement.</span><span class="sxs-lookup"><span data-stu-id="f078a-105">The **scrollingDelay** attribute specifies or retrieves the time delay between scrolling movements.</span></span>

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a><span data-ttu-id="f078a-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="f078a-106">Possible Values</span></span>

<span data-ttu-id="f078a-107">Cet attribut est un **nombre** en lecture/écriture (**int**) qui spécifie le délai en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="f078a-107">This attribute is a read/write **Number** (**int**) specifying the delay in milliseconds.</span></span> <span data-ttu-id="f078a-108">Elle a une valeur minimale de 30 et une valeur par défaut de 85.</span><span class="sxs-lookup"><span data-stu-id="f078a-108">It has a minimum value of 30, and a default value of 85.</span></span> <span data-ttu-id="f078a-109">Si une valeur inférieure à la valeur minimale est spécifiée, la valeur par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f078a-109">If a value less than the minimum is specified, the default is used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f078a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f078a-110">Remarks</span></span>

<span data-ttu-id="f078a-111">Si le **défilement** est défini sur false, **scrollingDelay** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f078a-111">If **scrolling** is set to false, **scrollingDelay** is ignored.</span></span>

<span data-ttu-id="f078a-112">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="f078a-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f078a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f078a-113">Requirements</span></span>



| <span data-ttu-id="f078a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f078a-114">Requirement</span></span> | <span data-ttu-id="f078a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f078a-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f078a-116">Version</span><span class="sxs-lookup"><span data-stu-id="f078a-116">Version</span></span><br/> | <span data-ttu-id="f078a-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="f078a-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f078a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f078a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f078a-119">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="f078a-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="f078a-120">**TEXTE. défilement**</span><span class="sxs-lookup"><span data-stu-id="f078a-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





