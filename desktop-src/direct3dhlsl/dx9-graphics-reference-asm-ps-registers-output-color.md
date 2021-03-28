---
title: Registre des couleurs de sortie
description: Les registres de sortie de couleur de nuanceur de pixels (oC \) sont des registres en écriture seule qui génèrent les résultats dans plusieurs cibles de rendu.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382455"
---
# <a name="output-color-register"></a><span data-ttu-id="f99af-103">Registre des couleurs de sortie</span><span class="sxs-lookup"><span data-stu-id="f99af-103">Output Color Register</span></span>

<span data-ttu-id="f99af-104">Les registres de sortie de couleur de nuanceur de pixels (oC #) sont des registres en écriture seule qui génèrent les résultats dans plusieurs cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="f99af-104">The pixel shader color output registers (oC#) are write-only registers that output results to multiple render targets.</span></span>

<span data-ttu-id="f99af-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f99af-105">Syntax</span></span>



| <span data-ttu-id="f99af-106">c #</span><span class="sxs-lookup"><span data-stu-id="f99af-106">oC#</span></span> |
|------|



 

<span data-ttu-id="f99af-107">Où :</span><span class="sxs-lookup"><span data-stu-id="f99af-107">Where:</span></span>



| <span data-ttu-id="f99af-108">Nom</span><span class="sxs-lookup"><span data-stu-id="f99af-108">Name</span></span> | <span data-ttu-id="f99af-109">Description</span><span class="sxs-lookup"><span data-stu-id="f99af-109">Description</span></span>       |
|------|-------------------|
| <span data-ttu-id="f99af-110">oC0</span><span class="sxs-lookup"><span data-stu-id="f99af-110">oC0</span></span>  | <span data-ttu-id="f99af-111">cible de rendu \# 0</span><span class="sxs-lookup"><span data-stu-id="f99af-111">render target \#0</span></span> |
| <span data-ttu-id="f99af-112">oC1</span><span class="sxs-lookup"><span data-stu-id="f99af-112">oC1</span></span>  | <span data-ttu-id="f99af-113">cible de rendu \# 1</span><span class="sxs-lookup"><span data-stu-id="f99af-113">render target \#1</span></span> |
| <span data-ttu-id="f99af-114">oC2</span><span class="sxs-lookup"><span data-stu-id="f99af-114">oC2</span></span>  | <span data-ttu-id="f99af-115">cible de rendu \# 2</span><span class="sxs-lookup"><span data-stu-id="f99af-115">render target \#2</span></span> |
| <span data-ttu-id="f99af-116">oC3</span><span class="sxs-lookup"><span data-stu-id="f99af-116">oC3</span></span>  | <span data-ttu-id="f99af-117">cible de rendu \# 3</span><span class="sxs-lookup"><span data-stu-id="f99af-117">render target \#3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f99af-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f99af-118">Remarks</span></span>

-   <span data-ttu-id="f99af-119">Si oCn est écrit, mais qu’il n’existe aucune cible de rendu correspondante, cette écriture dans oCn est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f99af-119">If oCn is written but there is no corresponding render target, then this write to oCn is ignored.</span></span>
-   <span data-ttu-id="f99af-120">Les États de rendu D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 et D3DRS \_ COLORWRITEENABLE3 déterminent les composants de oCn qui sont finalement écrits dans la cible de rendu (après Blend, le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="f99af-120">The render states D3DRS\_COLORWRITEENABLE, D3DRS\_COLORWRITEENABLE1, D3DRS\_COLORWRITEENABLE2 and D3DRS\_COLORWRITEENABLE3 determine which components of oCn ultimately get written to the render target (after blend, if applicable).</span></span> <span data-ttu-id="f99af-121">Si le nuanceur écrit, mais pas tous les composants définis par les \_ \* États de rendu D3DRS COLORWRITEENABLE pour un registre oCn donné, les canaux non écrits produisent des valeurs non définies dans la cible de rendu correspondante.</span><span class="sxs-lookup"><span data-stu-id="f99af-121">If the shader writes some but not all of the components defined by the D3DRS\_COLORWRITEENABLE\* render states for a given oCn register, then the unwritten channels produce undefined values in the corresponding render target.</span></span> <span data-ttu-id="f99af-122">Si aucun des composants d’un oCn n’est écrit, la cible de rendu correspondante ne doit pas être mise à jour (comme indiqué ci-dessus), de sorte que les \_ États de rendu D3DRS COLORWRITEENABLE \* ne s’appliquent pas.</span><span class="sxs-lookup"><span data-stu-id="f99af-122">If none of the components of an oCn are written, the corresponding render target must not be updated at all (as stated above), so the D3DRS\_COLORWRITEENABLE\* render states do not apply.</span></span>

### <a name="shader-model-2-restrictions"></a><span data-ttu-id="f99af-123">Restrictions du modèle de nuanceur 2</span><span class="sxs-lookup"><span data-stu-id="f99af-123">Shader Model 2 Restrictions</span></span>

-   <span data-ttu-id="f99af-124">oCn peut uniquement être écrit avec l’instruction [MOV-PS](mov---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="f99af-124">oCn can only be written with the [mov - ps](mov---ps.md) instruction.</span></span>
-   <span data-ttu-id="f99af-125">oC0 doit toujours être écrit dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f99af-125">oC0 must be always written in the shader.</span></span>
-   <span data-ttu-id="f99af-126">Aucun Swizzle source (sauf. XYZW = default Swizzle) ou le modificateur source n’est autorisé lors de l’écriture dans un oCn.</span><span class="sxs-lookup"><span data-stu-id="f99af-126">No source swizzle (except .xyzw = default swizzle) or source modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="f99af-127">Aucun masque d’écriture de destination (à l’exception de XYZW = masque par défaut) ou modificateur d’instruction n’est autorisé lors de l’écriture dans un oCn.</span><span class="sxs-lookup"><span data-stu-id="f99af-127">No destination write mask (except .xyzw = default mask) or instruction modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="f99af-128">Si oCn est écrit, oC0-oCn-1 doit également être écrit.</span><span class="sxs-lookup"><span data-stu-id="f99af-128">If oCn is written, then oC0 - oCn-1 must also be written.</span></span> <span data-ttu-id="f99af-129">Par exemple, pour écrire dans oC2, vous devez également écrire dans oC0 et oC1.</span><span class="sxs-lookup"><span data-stu-id="f99af-129">For example, to write to oC2, you must also write to oC0 and oC1.</span></span>
-   <span data-ttu-id="f99af-130">Au plus une écriture vers n’importe quel nuanceur oC par nuanceur est autorisé.</span><span class="sxs-lookup"><span data-stu-id="f99af-130">At most one write to any oC# per shader is allowed.</span></span>
-   <span data-ttu-id="f99af-131">Pour PS \_ 2 \_ x et PS \_ 3 \_ 0, vous ne pouvez pas écrire dans les registres OC # et OD \# au sein d’un contrôle de workflow dynamique ou d’un prédicat (les écritures dans le contrôle de workflow statique ne sont pas correctes).</span><span class="sxs-lookup"><span data-stu-id="f99af-131">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>

### <a name="shader-model-3-restrictions"></a><span data-ttu-id="f99af-132">Restrictions du modèle de nuanceur 3</span><span class="sxs-lookup"><span data-stu-id="f99af-132">Shader Model 3 Restrictions</span></span>

-   <span data-ttu-id="f99af-133">Pour PS \_ 3 \_ 0, les registres de sortie OC # et OD \# peuvent être écrits un nombre quelconque de fois.</span><span class="sxs-lookup"><span data-stu-id="f99af-133">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="f99af-134">La sortie du nuanceur de pixels provient du contenu des registres de sortie à la fin de l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f99af-134">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="f99af-135">Si une écriture dans un registre de sortie ne se produit pas, peut-être en raison du contrôle de la transmission ou si le nuanceur ne l’a pas écrit, le renderTarget correspondant n’est pas non plus mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f99af-135">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding rendertarget is also not updated.</span></span> <span data-ttu-id="f99af-136">Si un sous-ensemble des canaux d’un registre de sortie est écrit, les valeurs non définies sont écrites sur les autres canaux.</span><span class="sxs-lookup"><span data-stu-id="f99af-136">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="f99af-137">Pour PS \_ 3 \_ 0, les registres OC # peuvent être écrits avec n’importe quel writemasks.</span><span class="sxs-lookup"><span data-stu-id="f99af-137">For ps\_3\_0, the oC# registers can be written with any writemasks.</span></span>
-   <span data-ttu-id="f99af-138">Pour PS \_ 2 \_ x et PS \_ 3 \_ 0, vous ne pouvez pas écrire dans les registres OC # et OD \# au sein d’un contrôle de workflow dynamique ou d’un prédicat (les écritures dans le contrôle de workflow statique ne sont pas correctes).</span><span class="sxs-lookup"><span data-stu-id="f99af-138">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>
-   <span data-ttu-id="f99af-139">Vous n’êtes pas autorisé à effectuer des calculs de dégradés (ou des opérations qui appellent implicitement des calculs de gradient tels que [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) à l’intérieur d’instructions de contrôle de Flow dont les conditions de création de branche varient en fonction de la primitive (c’est-à-dire : instructions de contrôle de workflow dynamique).</span><span class="sxs-lookup"><span data-stu-id="f99af-139">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="f99af-140">La prédicat d’instruction n’est pas considéré comme un contrôle de workflow dynamique.</span><span class="sxs-lookup"><span data-stu-id="f99af-140">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f99af-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f99af-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f99af-142">Inscrit</span><span class="sxs-lookup"><span data-stu-id="f99af-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="f99af-143">Plusieurs cibles de rendu (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f99af-143">Multiple Render Targets (Direct3D 9)</span></span>](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 