---
title: '\_ \_ modificateurs de Registre source PS 1 4 pour texld, texcrd'
description: Les instructions de texture de deux nuanceurs de pixels version 1 \_ 4, texld-PS \_ 1 \_ 4 et texcrd-PS, ont une syntaxe personnalisée.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104101141"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a><span data-ttu-id="abe27-103">\_ \_ modificateurs de Registre source PS 1 4 pour texld, texcrd</span><span class="sxs-lookup"><span data-stu-id="abe27-103">ps\_1\_4 source register modifiers for texld, texcrd</span></span>

<span data-ttu-id="abe27-104">Les instructions de texture de deux nuanceurs de pixels version 1 \_ 4, [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) et [texcrd-PS](texcrd---ps.md), ont une syntaxe personnalisée.</span><span class="sxs-lookup"><span data-stu-id="abe27-104">Two pixel shader version 1\_4 texture address instructions, [texld - ps\_1\_4](texld---ps-1-4.md) and [texcrd - ps](texcrd---ps.md), have custom syntax.</span></span> <span data-ttu-id="abe27-105">Ces instructions prennent en charge leur propre ensemble de modificateurs de Registre source, de sélecteurs de Registre source et de masques d’écriture de registre de destination, comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="abe27-105">These instructions support their own set of source register modifiers, source register selectors, and destination-register write masks, as shown here.</span></span>

## <a name="source-register-modifiers-for-texld-and-texcrd"></a><span data-ttu-id="abe27-106">Modificateurs de Registre source pour texld et texcrd</span><span class="sxs-lookup"><span data-stu-id="abe27-106">Source Register Modifiers for texld and texcrd</span></span>

<span data-ttu-id="abe27-107">Ces modificateurs fournissent une fonctionnalité de division projective en divisant les valeurs x et y par les valeurs z ou w.</span><span class="sxs-lookup"><span data-stu-id="abe27-107">These modifiers provide projective divide functionality by dividing the x and y values by either the z or w values.</span></span>



| <span data-ttu-id="abe27-108">Modificateurs de Registre source</span><span class="sxs-lookup"><span data-stu-id="abe27-108">Source register modifiers</span></span> | <span data-ttu-id="abe27-109">Description</span><span class="sxs-lookup"><span data-stu-id="abe27-109">Description</span></span>                | <span data-ttu-id="abe27-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abe27-110">Syntax</span></span>       |
|---------------------------|----------------------------|--------------|
| <span data-ttu-id="abe27-111">\_DZ</span><span class="sxs-lookup"><span data-stu-id="abe27-111">\_dz</span></span>                      | <span data-ttu-id="abe27-112">Diviser les composants x, y par z</span><span class="sxs-lookup"><span data-stu-id="abe27-112">Divide x,y components by z</span></span> | <span data-ttu-id="abe27-113">inscrire \_ DZ</span><span class="sxs-lookup"><span data-stu-id="abe27-113">register\_dz</span></span> |
| <span data-ttu-id="abe27-114">\_db</span><span class="sxs-lookup"><span data-stu-id="abe27-114">\_db</span></span>                      | <span data-ttu-id="abe27-115">Diviser les composants x, y par z</span><span class="sxs-lookup"><span data-stu-id="abe27-115">Divide x,y components by z</span></span> | <span data-ttu-id="abe27-116">inscrire la base de référence \_</span><span class="sxs-lookup"><span data-stu-id="abe27-116">register\_db</span></span> |
| <span data-ttu-id="abe27-117">\_DW</span><span class="sxs-lookup"><span data-stu-id="abe27-117">\_dw</span></span>                      | <span data-ttu-id="abe27-118">Diviser les composants x, y par w</span><span class="sxs-lookup"><span data-stu-id="abe27-118">Divide x,y components by w</span></span> | <span data-ttu-id="abe27-119">inscrire la \_ DW</span><span class="sxs-lookup"><span data-stu-id="abe27-119">register\_dw</span></span> |
| <span data-ttu-id="abe27-120">\_da</span><span class="sxs-lookup"><span data-stu-id="abe27-120">\_da</span></span>                      | <span data-ttu-id="abe27-121">Diviser les composants x, y par w</span><span class="sxs-lookup"><span data-stu-id="abe27-121">Divide x,y components by w</span></span> | <span data-ttu-id="abe27-122">inscrire \_ da</span><span class="sxs-lookup"><span data-stu-id="abe27-122">register\_da</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="abe27-123">Notes</span><span class="sxs-lookup"><span data-stu-id="abe27-123">Remarks</span></span>

<span data-ttu-id="abe27-124">Le \_ \_ modificateur DZ ou DB effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="abe27-124">The \_dz or \_db modifier does the following:</span></span>


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



<span data-ttu-id="abe27-125">Le \_ \_ modificateur DW ou da effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="abe27-125">The \_dw or \_da modifier does the following:</span></span>


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a><span data-ttu-id="abe27-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="abe27-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abe27-127">Modificateurs de Registre source du nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="abe27-127">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




