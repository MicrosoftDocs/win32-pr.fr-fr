---
title: TEXTE. défilement
description: L’attribut de défilement spécifie ou récupère une valeur indiquant si le texte défile.
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- TEXT. défilement du lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545492"
---
# <a name="textscrolling"></a><span data-ttu-id="50935-104">TEXTE. défilement</span><span class="sxs-lookup"><span data-stu-id="50935-104">TEXT.scrolling</span></span>

<span data-ttu-id="50935-105">L’attribut de **défilement** spécifie ou récupère une valeur indiquant si le texte défile.</span><span class="sxs-lookup"><span data-stu-id="50935-105">The **scrolling** attribute specifies or retrieves a value indicating whether the text scrolls.</span></span>

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a><span data-ttu-id="50935-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="50935-106">Possible Values</span></span>

<span data-ttu-id="50935-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="50935-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="50935-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="50935-108">Value</span></span> | <span data-ttu-id="50935-109">Description</span><span class="sxs-lookup"><span data-stu-id="50935-109">Description</span></span>                     |
|-------|---------------------------------|
| <span data-ttu-id="50935-110">true</span><span class="sxs-lookup"><span data-stu-id="50935-110">true</span></span>  | <span data-ttu-id="50935-111">Le défilement est activé.</span><span class="sxs-lookup"><span data-stu-id="50935-111">Scrolling is enabled.</span></span>           |
| <span data-ttu-id="50935-112">false</span><span class="sxs-lookup"><span data-stu-id="50935-112">false</span></span> | <span data-ttu-id="50935-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="50935-113">Default.</span></span> <span data-ttu-id="50935-114">Le défilement est désactivé.</span><span class="sxs-lookup"><span data-stu-id="50935-114">Scrolling is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="50935-115">Notes</span><span class="sxs-lookup"><span data-stu-id="50935-115">Remarks</span></span>

<span data-ttu-id="50935-116">La fonctionnalité de défilement fournit une mémoire tampon à deux espaces entre la fin du texte et le début de la ligne répétée.</span><span class="sxs-lookup"><span data-stu-id="50935-116">The scrolling feature provides a two-space buffer between the end of the text and the beginning of the repeated line.</span></span>

<span data-ttu-id="50935-117">L’attribut **Justification** spécifie l’emplacement où le texte apparaît pour la première fois avant le début du défilement.</span><span class="sxs-lookup"><span data-stu-id="50935-117">The **justification** attribute specifies where the text first appears before the scrolling begins.</span></span>

<span data-ttu-id="50935-118">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="50935-118">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="50935-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50935-119">Requirements</span></span>



| <span data-ttu-id="50935-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50935-120">Requirement</span></span> | <span data-ttu-id="50935-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="50935-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="50935-122">Version</span><span class="sxs-lookup"><span data-stu-id="50935-122">Version</span></span><br/> | <span data-ttu-id="50935-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="50935-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50935-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50935-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50935-125">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="50935-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="50935-126">**TEXT. Justification**</span><span class="sxs-lookup"><span data-stu-id="50935-126">**TEXT.justification**</span></span>](text-justification.md)
</dt> <dt>

[<span data-ttu-id="50935-127">**TEXT. scrollingAmount**</span><span class="sxs-lookup"><span data-stu-id="50935-127">**TEXT.scrollingAmount**</span></span>](text-scrollingamount.md)
</dt> <dt>

[<span data-ttu-id="50935-128">**TEXT. scrollingDelay**</span><span class="sxs-lookup"><span data-stu-id="50935-128">**TEXT.scrollingDelay**</span></span>](text-scrollingdelay.md)
</dt> <dt>

[<span data-ttu-id="50935-129">**TEXT. scrollingDirection**</span><span class="sxs-lookup"><span data-stu-id="50935-129">**TEXT.scrollingDirection**</span></span>](text-scrollingdirection.md)
</dt> </dl>

 

 





