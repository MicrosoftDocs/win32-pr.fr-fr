---
description: Les techniques fournissent le muscle de rendu. Une technique encapsule l’état d’effet qui détermine un style de rendu. Une technique est constituée d’une ou de plusieurs passes.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Techniques et passes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544567"
---
# <a name="techniques-and-passes-direct3d-9"></a><span data-ttu-id="c2897-105">Techniques et passes (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c2897-105">Techniques and Passes (Direct3D 9)</span></span>

<span data-ttu-id="c2897-106">Les techniques fournissent le muscle de rendu.</span><span class="sxs-lookup"><span data-stu-id="c2897-106">Techniques provide the rendering muscle.</span></span> <span data-ttu-id="c2897-107">Une technique encapsule l’état d’effet qui détermine un style de rendu.</span><span class="sxs-lookup"><span data-stu-id="c2897-107">A technique encapsulates the effect state that determines a rendering style.</span></span> <span data-ttu-id="c2897-108">Une technique est constituée d’une ou de plusieurs passes.</span><span class="sxs-lookup"><span data-stu-id="c2897-108">A technique is made up of one or more passes.</span></span>

## <a name="techniques"></a><span data-ttu-id="c2897-109">Technologie</span><span class="sxs-lookup"><span data-stu-id="c2897-109">Techniques</span></span>

<span data-ttu-id="c2897-110">La syntaxe d’appel d’une technique est la suivante :</span><span class="sxs-lookup"><span data-stu-id="c2897-110">The syntax for calling a technique is as follows:</span></span>


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



<span data-ttu-id="c2897-111">Où :</span><span class="sxs-lookup"><span data-stu-id="c2897-111">Where:</span></span>

-   <span data-ttu-id="c2897-112">ID est un nom unique facultatif.</span><span class="sxs-lookup"><span data-stu-id="c2897-112">id is an optional unique name.</span></span>
-   <span data-ttu-id="c2897-113">l’annotation est égale à zéro, un ou plusieurs éléments facultatifs d’informations spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2897-113">annotation is zero or more optional pieces of user-specific information.</span></span> <span data-ttu-id="c2897-114">Consultez [Ajouter des informations pour appliquer des paramètres avec des \_ Annotations](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="c2897-114">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="c2897-115">Pass (es) est égal à zéro ou plusieurs passes.</span><span class="sxs-lookup"><span data-stu-id="c2897-115">pass(es) is zero or more passes.</span></span> <span data-ttu-id="c2897-116">Chaque passe contient des attributions d’État.</span><span class="sxs-lookup"><span data-stu-id="c2897-116">Each pass contains state assignments.</span></span> <span data-ttu-id="c2897-117">Voir ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c2897-117">See below.</span></span>

## <a name="passes"></a><span data-ttu-id="c2897-118">Mettent</span><span class="sxs-lookup"><span data-stu-id="c2897-118">Passes</span></span>

<span data-ttu-id="c2897-119">Une passe contient les assignations d’État requises pour effectuer le rendu.</span><span class="sxs-lookup"><span data-stu-id="c2897-119">A pass contains the state assignments required to render.</span></span>


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



<span data-ttu-id="c2897-120">Où :</span><span class="sxs-lookup"><span data-stu-id="c2897-120">Where:</span></span>

-   <span data-ttu-id="c2897-121">ID est un nom unique facultatif.</span><span class="sxs-lookup"><span data-stu-id="c2897-121">id is an optional unique name.</span></span>
-   <span data-ttu-id="c2897-122">l’annotation est une partie facultative d’informations spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2897-122">annotation is one or more optional piece of user-specific information.</span></span> <span data-ttu-id="c2897-123">Consultez [Ajouter des informations pour appliquer des paramètres avec des \_ Annotations](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="c2897-123">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="c2897-124">les affectations assignent zéro ou plusieurs valeurs d’État, ou évaluent une ou plusieurs expressions.</span><span class="sxs-lookup"><span data-stu-id="c2897-124">assignment(s) assigns zero or more state values, or evaluates one or more expressions.</span></span> <span data-ttu-id="c2897-125">Consultez [États d’effet (Direct3D 9)](effect-states.md) et [expressions (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="c2897-125">See [Effect States (Direct3D 9)](effect-states.md) and [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="c2897-126">Les passes ignorent toutes les affectations, sauf la dernière, dans un ensemble d’affectations répétées au même État.</span><span class="sxs-lookup"><span data-stu-id="c2897-126">Passes ignore all but the last assignment in a set of repeated assignments to the same state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2897-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2897-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2897-128">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="c2897-128">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



