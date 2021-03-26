---
title: Registre source Swizzling (référence HLSL VS)
description: Avant l’exécution d’une instruction, les données d’un registre source sont copiées dans un registre temporaire. Swizzling fait référence à la capacité de copier n’importe quel composant Registre source vers un composant de registre temporaire. Swizzling n’affecte pas les données du Registre source.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104381255"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a><span data-ttu-id="e4f41-105">Registre source Swizzling (référence HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="e4f41-105">Source Register Swizzling (HLSL VS reference)</span></span>

<span data-ttu-id="e4f41-106">Avant l’exécution d’une instruction, les données d’un registre source sont copiées dans un registre temporaire.</span><span class="sxs-lookup"><span data-stu-id="e4f41-106">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span> <span data-ttu-id="e4f41-107">Swizzling fait référence à la capacité de copier n’importe quel composant Registre source vers un composant de registre temporaire.</span><span class="sxs-lookup"><span data-stu-id="e4f41-107">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="e4f41-108">Swizzling n’affecte pas les données du Registre source.</span><span class="sxs-lookup"><span data-stu-id="e4f41-108">Swizzling does not affect the source register data.</span></span>

## <a name="component-swizzling"></a><span data-ttu-id="e4f41-109">Swizzling composant</span><span class="sxs-lookup"><span data-stu-id="e4f41-109">Component Swizzling</span></span>

<span data-ttu-id="e4f41-110">Comme indiqué dans le tableau suivant, swizzling peut être appliqué aux composants individuels des données du Registre source (où sont l’un des registres d’entrée de nuanceur de sommets valides [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span><span class="sxs-lookup"><span data-stu-id="e4f41-110">As shown in the following table, swizzling can be applied to the individual components of the source register data (where r is one of the valid vertex shader input [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span></span>



| <span data-ttu-id="e4f41-111">Modificateur de composant</span><span class="sxs-lookup"><span data-stu-id="e4f41-111">Component modifier</span></span>                 | <span data-ttu-id="e4f41-112">Description</span><span class="sxs-lookup"><span data-stu-id="e4f41-112">Description</span></span>    |
|------------------------------------|----------------|
| <span data-ttu-id="e4f41-113">r. \[ XYZW \] \[ XYZW \] \[ XYZW \] \[ XYZW\]</span><span class="sxs-lookup"><span data-stu-id="e4f41-113">r.\[xyzw\]\[xyzw\]\[xyzw\]\[xyzw\]</span></span> | <span data-ttu-id="e4f41-114">Swizzle source</span><span class="sxs-lookup"><span data-stu-id="e4f41-114">Source swizzle</span></span> |



 

-   <span data-ttu-id="e4f41-115">Les quatre composants sont toujours copiés.</span><span class="sxs-lookup"><span data-stu-id="e4f41-115">All four components are always copied.</span></span> <span data-ttu-id="e4f41-116">Si moins de quatre composants sont spécifiés, le dernier composant est répété (XY signifie. xyyy).</span><span class="sxs-lookup"><span data-stu-id="e4f41-116">If fewer than four components are specified, the last component is repeated (xy means .xyyy).</span></span> <span data-ttu-id="e4f41-117">Si aucun composant n’est spécifié, x est répété (. xxxx).</span><span class="sxs-lookup"><span data-stu-id="e4f41-117">If no components are specified, x is repeated (.xxxx).</span></span>
-   <span data-ttu-id="e4f41-118">Les composants peuvent apparaître dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="e4f41-118">The components can appear in any order.</span></span> <span data-ttu-id="e4f41-119">v0. ywx résultats dans v0. ywxx.</span><span class="sxs-lookup"><span data-stu-id="e4f41-119">v0.ywx results in v0.ywxx.</span></span>
-   <span data-ttu-id="e4f41-120">Les composants RVBA peuvent être utilisés respectivement pour XYZW (r pour x, g pour b, etc.).</span><span class="sxs-lookup"><span data-stu-id="e4f41-120">The rgba components can be used respectively for xyzw (r for x, g for b, etc.).</span></span>
-   <span data-ttu-id="e4f41-121">Ces instructions implémentent la source-inscrire un composant unique Swizzles : exp, expp, log, logP, Pow, RCP, rsq.</span><span class="sxs-lookup"><span data-stu-id="e4f41-121">These instructions implement source-register single component swizzles: exp, expp, log, logp, pow, rcp, rsq.</span></span> <span data-ttu-id="e4f41-122">Le résultat de ces instructions est copié dans les quatre composants du registre de destination.</span><span class="sxs-lookup"><span data-stu-id="e4f41-122">The result of these instructions is copied to all four destination register components.</span></span>

<span data-ttu-id="e4f41-123">Swizzling ne peut pas être utilisé sur les instructions [M3X2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [m4x3-vs](m4x3---vs.md)et [M4X4-vs](m4x4---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f41-123">Swizzling cannot be used on the [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m4x3 - vs](m4x3---vs.md), and [m4x4 - vs](m4x4---vs.md) instructions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4f41-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e4f41-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f41-125">Modificateurs de registre de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="e4f41-125">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




