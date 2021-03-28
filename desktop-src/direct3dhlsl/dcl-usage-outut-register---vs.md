---
title: sortie dcl_usage (SM1, SM2, SM3-vs ASM)
description: Les différents types de registres de sortie ont été réduits en douze registres de sortie (deux pour la couleur, huit pour la texture, un pour la position et un pour le brouillard et la taille du point).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c653c5af43bd3392f97e30571ac56ded66cbfc04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990985"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="a73f4-103">sortie d’utilisation de DCL \_ (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="a73f4-103">dcl\_usage output (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="a73f4-104">Les différents types de registres de sortie ont été réduits en douze registres de sortie (deux pour la couleur, huit pour la texture, un pour la position et un pour le brouillard et la taille du point).</span><span class="sxs-lookup"><span data-stu-id="a73f4-104">The various types of output registers have been collapsed into twelve output registers (two for color, eight for texture, one for position, and one for fog and point size).</span></span> <span data-ttu-id="a73f4-105">Elles peuvent être utilisées pour tout ce que l’utilisateur souhaite interpoler pour le nuanceur de pixels : les coordonnées de la texture, les couleurs, le brouillard, etc.</span><span class="sxs-lookup"><span data-stu-id="a73f4-105">These can be used for anything the user wants to interpolate for the pixel shader: texture coordinates, colors, fog, and so on.</span></span>

<span data-ttu-id="a73f4-106">Les registres de sortie requièrent des déclarations qui incluent une sémantique.</span><span class="sxs-lookup"><span data-stu-id="a73f4-106">Output registers require declarations that include semantics.</span></span> <span data-ttu-id="a73f4-107">Par exemple, les anciens registres de position et de taille de point sont remplacés par la déclaration d’un registre de sortie avec une sémantique de position ou de taille de point.</span><span class="sxs-lookup"><span data-stu-id="a73f4-107">For instance, the old position and point size registers are replaced by declaring an output register with a position or point-size semantic.</span></span>

<span data-ttu-id="a73f4-108">Parmi les douze registres de sortie, les dix (pas nécessairement o0 à O9) comportent quatre composants (XYZW), un autre doit être déclaré comme position (et doit également inclure les quatre composants) et, éventuellement, une taille de point scalaire.</span><span class="sxs-lookup"><span data-stu-id="a73f4-108">Of the twelve output registers, any ten (not necessarily o0 to o9) have four components (xyzw), another one must be declared as position (and must also include all four components), and optionally one more can be a scalar point size.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73f4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a73f4-109">Syntax</span></span>

<span data-ttu-id="a73f4-110">La syntaxe de déclaration des registres de sortie est similaire aux déclarations du registre d’entrée :</span><span class="sxs-lookup"><span data-stu-id="a73f4-110">The syntax for declaring output registers is similar to the declarations for the input register:</span></span>



|                                  |
|----------------------------------|
| <span data-ttu-id="a73f4-111">sémantique de DCL \_ o \[ . masque d’écriture \_\]</span><span class="sxs-lookup"><span data-stu-id="a73f4-111">dcl\_semantics o\[.write\_mask\]</span></span> |



 

<span data-ttu-id="a73f4-112">Où :</span><span class="sxs-lookup"><span data-stu-id="a73f4-112">Where:</span></span>

-   <span data-ttu-id="a73f4-113">la \_ sémantique DCL peut utiliser le même ensemble de sémantique que pour la déclaration d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a73f4-113">dcl\_semantics can use the same set of semantics as for the input declaration.</span></span> <span data-ttu-id="a73f4-114">Les noms sémantiques proviennent de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (et sont associés à un index, tel que position3).</span><span class="sxs-lookup"><span data-stu-id="a73f4-114">Semantic names come from [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (and are paired with an index, such as position3).</span></span> <span data-ttu-id="a73f4-115">Il doit toujours y avoir un registre de sortie avec la sémantique positiont0 lorsqu’il n’est pas utilisé pour le traitement des vertex.</span><span class="sxs-lookup"><span data-stu-id="a73f4-115">There always has to be one output register with the positiont0 semantic when not used for processing vertices.</span></span> <span data-ttu-id="a73f4-116">La sémantique positiont0 et la sémantique pointsize0 sont les seules qui ont un sens au-delà de la simple autorisation de la liaison entre vertex et nuanceurs de pixels.</span><span class="sxs-lookup"><span data-stu-id="a73f4-116">The positiont0 semantic and the pointsize0 semantic are the only ones that have meaning beyond simply allowing linkage from vertex to pixel shaders.</span></span> <span data-ttu-id="a73f4-117">Pour les nuanceurs avec contrôle de Flow, on suppose que la sortie de cas le plus défavorable est déclarée.</span><span class="sxs-lookup"><span data-stu-id="a73f4-117">For shaders with flow control, it is assumed that the worst case output is declared.</span></span> <span data-ttu-id="a73f4-118">Il n’y a pas de valeurs par défaut si un nuanceur ne génère pas réellement ce qu’il déclare (en raison du contrôle de Flow).</span><span class="sxs-lookup"><span data-stu-id="a73f4-118">There are no defaults if a shader does not actually output what it declares it should (due to flow control).</span></span>
-   <span data-ttu-id="a73f4-119">o est un registre de sortie.</span><span class="sxs-lookup"><span data-stu-id="a73f4-119">o is an output register.</span></span> <span data-ttu-id="a73f4-120">Consultez [ \_ registres de sortie](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="a73f4-120">See [Output\_Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>
-   <span data-ttu-id="a73f4-121">\_le masque d’écriture indique le même registre de sortie qui peut être déclaré plusieurs fois (par conséquent, une sémantique différente peut être appliquée à des composants individuels), à chaque fois avec un masque d’écriture unique.</span><span class="sxs-lookup"><span data-stu-id="a73f4-121">write\_mask indicates the same output register that can be declared multiple times (so different semantics can be applied to individual components), each time with a unique write mask.</span></span> <span data-ttu-id="a73f4-122">Toutefois, la même sémantique ne peut pas être utilisée plusieurs fois dans une déclaration.</span><span class="sxs-lookup"><span data-stu-id="a73f4-122">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="a73f4-123">Cela signifie que les vecteurs doivent avoir quatre composants ou moins, et ne peuvent pas traverser les limites d’un registre à quatre composants (registres individuels).</span><span class="sxs-lookup"><span data-stu-id="a73f4-123">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual registers).</span></span> <span data-ttu-id="a73f4-124">Lorsque la sémantique de taille de point est utilisée, elle doit avoir un masque d’écriture complet, car elle est considérée comme une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="a73f4-124">When the point-size semantic is used, it should have full write mask because it is considered a scalar.</span></span> <span data-ttu-id="a73f4-125">Lorsque la sémantique de position est utilisée, elle doit avoir un masque d’écriture complet, car les quatre composants doivent être écrits.</span><span class="sxs-lookup"><span data-stu-id="a73f4-125">When the position semantic is used, it should have a full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="a73f4-126">Notes</span><span class="sxs-lookup"><span data-stu-id="a73f4-126">Remarks</span></span>



| <span data-ttu-id="a73f4-127">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="a73f4-127">Vertex shader versions</span></span> | <span data-ttu-id="a73f4-128">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a73f4-128">3\_0</span></span> | <span data-ttu-id="a73f4-129">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a73f4-129">3\_sw</span></span> |
|------------------------|------|-------|
| <span data-ttu-id="a73f4-130">utilisation de DCL \_</span><span class="sxs-lookup"><span data-stu-id="a73f4-130">dcl\_usage</span></span>             | <span data-ttu-id="a73f4-131">x</span><span class="sxs-lookup"><span data-stu-id="a73f4-131">x</span></span>    | <span data-ttu-id="a73f4-132">x</span><span class="sxs-lookup"><span data-stu-id="a73f4-132">x</span></span>     |



 

<span data-ttu-id="a73f4-133">Toutes les instructions d' [ \_ utilisation](dcl-usage-input-register---vs.md) de la DCL doivent apparaître avant la première instruction exécutable.</span><span class="sxs-lookup"><span data-stu-id="a73f4-133">All [dcl\_usage](dcl-usage-input-register---vs.md) instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="a73f4-134">Exemples de déclaration</span><span class="sxs-lookup"><span data-stu-id="a73f4-134">Declaration Examples</span></span>


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a><span data-ttu-id="a73f4-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a73f4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a73f4-136">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="a73f4-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 