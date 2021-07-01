---
title: dcl_semantics (SM3-PS ASM)
description: Déclarez l’association entre la sortie du nuanceur de sommets et l’entrée de nuanceur de pixels.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c506d2ad23003f93bbaea409cacc60b18c86534
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129706"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="8a6b8-103">\_sémantique DCL (SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="8a6b8-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="8a6b8-104">Déclarez l’association entre la sortie du nuanceur de sommets et l’entrée de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="8a6b8-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a6b8-105">Syntax</span></span>

<span data-ttu-id="8a6b8-106">sémantique DCL Centre d' \_ \[ \_ \] heure d’été \[ \_\]</span><span class="sxs-lookup"><span data-stu-id="8a6b8-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span>



 

<span data-ttu-id="8a6b8-107">Où :</span><span class="sxs-lookup"><span data-stu-id="8a6b8-107">Where:</span></span>

-   <span data-ttu-id="8a6b8-108">\_Semantics : identifie l’utilisation des données prévue et peut être l’une des valeurs de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (sans le \_ préfixe D3DDECLUSAGE).</span><span class="sxs-lookup"><span data-stu-id="8a6b8-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="8a6b8-109">En outre, un index d’entiers peut être ajouté à la sémantique pour distinguer les paramètres qui utilisent une sémantique similaire.</span><span class="sxs-lookup"><span data-stu-id="8a6b8-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="8a6b8-110">\[\_Centre de [gravité](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] est un modificateur d’instruction facultatif.</span><span class="sxs-lookup"><span data-stu-id="8a6b8-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="8a6b8-111">Il est pris en charge sur \_ les instructions d’utilisation de la liste DCL qui déclarent les registres d’entrée et sur les instructions de recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="8a6b8-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="8a6b8-112">Le centre de gravité est ajouté sans espace.</span><span class="sxs-lookup"><span data-stu-id="8a6b8-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="8a6b8-113">DST : Registre de destination.</span><span class="sxs-lookup"><span data-stu-id="8a6b8-113">dst: destination register.</span></span> <span data-ttu-id="8a6b8-114">Consultez [ \_ registres PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="8a6b8-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="8a6b8-115">\_masque d’écriture : le même registre de sortie peut être déclaré plusieurs fois, à chaque fois avec un masque d’écriture unique (une sémantique différente peut donc être appliquée à des composants individuels).</span><span class="sxs-lookup"><span data-stu-id="8a6b8-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="8a6b8-116">Toutefois, la même sémantique ne peut pas être utilisée plusieurs fois dans une déclaration.</span><span class="sxs-lookup"><span data-stu-id="8a6b8-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="8a6b8-117">Cela signifie que les vecteurs doivent avoir quatre composants ou moins, et ne peuvent pas traverser les limites d’un registre à quatre composants (registres de sortie individuels).</span><span class="sxs-lookup"><span data-stu-id="8a6b8-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="8a6b8-118">Lorsque la \_ sémantique psize est utilisée, elle doit avoir un masque d’écriture complet, car elle est considérée comme une scalaire.</span><span class="sxs-lookup"><span data-stu-id="8a6b8-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="8a6b8-119">Lorsque la \_ sémantique de position est utilisée, elle doit avoir un masque d’écriture complet, car les quatre composants doivent être écrits.</span><span class="sxs-lookup"><span data-stu-id="8a6b8-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a6b8-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a6b8-120">Remarks</span></span>



| <span data-ttu-id="8a6b8-121">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="8a6b8-121">Pixel shader versions</span></span> | <span data-ttu-id="8a6b8-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="8a6b8-122">1\_1</span></span> | <span data-ttu-id="8a6b8-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="8a6b8-123">1\_2</span></span> | <span data-ttu-id="8a6b8-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8a6b8-124">1\_3</span></span> | <span data-ttu-id="8a6b8-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="8a6b8-125">1\_4</span></span> | <span data-ttu-id="8a6b8-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8a6b8-126">2\_0</span></span> | <span data-ttu-id="8a6b8-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8a6b8-127">2\_x</span></span> | <span data-ttu-id="8a6b8-128">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8a6b8-128">2\_sw</span></span> | <span data-ttu-id="8a6b8-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8a6b8-129">3\_0</span></span> | <span data-ttu-id="8a6b8-130">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8a6b8-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8a6b8-131">utilisation de DCL \_</span><span class="sxs-lookup"><span data-stu-id="8a6b8-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="8a6b8-132">x</span><span class="sxs-lookup"><span data-stu-id="8a6b8-132">x</span></span>    | <span data-ttu-id="8a6b8-133">x</span><span class="sxs-lookup"><span data-stu-id="8a6b8-133">x</span></span>     |



 

<span data-ttu-id="8a6b8-134">Toutes les \_ instructions d’utilisation de la DCL doivent apparaître avant la première instruction exécutable.</span><span class="sxs-lookup"><span data-stu-id="8a6b8-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="8a6b8-135">Exemples de déclaration</span><span class="sxs-lookup"><span data-stu-id="8a6b8-135">Declaration Examples</span></span>


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a><span data-ttu-id="8a6b8-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a6b8-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a6b8-137">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="8a6b8-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="8a6b8-138">[Exemple d’anticrénelage](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="8a6b8-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
