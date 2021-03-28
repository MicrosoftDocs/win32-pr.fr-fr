---
title: Mise à l’échelle signée du Registre source
description: Soustrait 0,5 de chaque canal et met à l’échelle le résultat de 2,0. Le nom BX2 provient de Bias et Scale-Times-2, qui est l’opération qu’il effectue.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197463"
---
# <a name="source-register-signed-scaling"></a><span data-ttu-id="ac03c-104">Mise à l’échelle signée du Registre source</span><span class="sxs-lookup"><span data-stu-id="ac03c-104">Source Register Signed Scaling</span></span>

<span data-ttu-id="ac03c-105">Soustrait 0,5 de chaque canal et met à l’échelle le résultat de 2,0.</span><span class="sxs-lookup"><span data-stu-id="ac03c-105">Subtracts 0.5 from each channel and scales the result by 2.0.</span></span> <span data-ttu-id="ac03c-106">Le nom BX2 provient de Bias et Scale-Times-2, qui est l’opération qu’il effectue.</span><span class="sxs-lookup"><span data-stu-id="ac03c-106">The name bx2 comes from bias and scale-times-two, which is the operation it performs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac03c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac03c-107">Syntax</span></span>


```
source register_bx2
```



## <a name="register"></a><span data-ttu-id="ac03c-108">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="ac03c-108">Register</span></span>

<span data-ttu-id="ac03c-109">Registre source.</span><span class="sxs-lookup"><span data-stu-id="ac03c-109">Source Register.</span></span> <span data-ttu-id="ac03c-110">Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="ac03c-110">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac03c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ac03c-111">Remarks</span></span>

<span data-ttu-id="ac03c-112">Cette opération est couramment utilisée pour étendre \[ 1,0 les données de 0,0 à 1,0 à \] \[ 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="ac03c-112">This operation is commonly used to expand data from \[0.0 to 1.0\] to \[-1.0 to 1.0\].</span></span> <span data-ttu-id="ac03c-113">Ce modificateur est conçu pour être utilisé avec les instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="ac03c-113">This modifier is designed for use with the arithmetic instructions.</span></span> <span data-ttu-id="ac03c-114">Ce modificateur est couramment utilisé sur les entrées de l’instruction du produit scalaire ([DP3-PS](dp3---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="ac03c-114">This modifier is commonly used on inputs to the dot product instruction ([dp3 - ps](dp3---ps.md)).</span></span> <span data-ttu-id="ac03c-115">L’utilisation \_ de BX2 sur des données situées en dehors de la plage de 0 à 1 peut produire des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="ac03c-115">Using \_bx2 on data outside the range 0 to 1 may produce undefined results.</span></span>

<span data-ttu-id="ac03c-116">L’opération de mise à l’échelle signée est appliquée aux données lues à partir du Registre avant l’exécution de l’instruction suivante.</span><span class="sxs-lookup"><span data-stu-id="ac03c-116">The signed scaling operation is applied to the data read from the register before the next instruction is run.</span></span> <span data-ttu-id="ac03c-117">L’opération est appliquée aux quatre canaux de couleurs (RVBA) comme suit :</span><span class="sxs-lookup"><span data-stu-id="ac03c-117">The operation is applied to all four color channels (RGBA) as follows:</span></span>


```
y = 2(x - 0.5)
```



<span data-ttu-id="ac03c-118">Le contenu du Registre n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="ac03c-118">The contents of the register are not changed.</span></span> <span data-ttu-id="ac03c-119">Le modificateur est appliqué uniquement aux données lues à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="ac03c-119">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="ac03c-120">Ce modificateur s’exclut mutuellement avec le [Registre source inversé](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) , de sorte qu’il ne peut pas être appliqué au même registre.</span><span class="sxs-lookup"><span data-stu-id="ac03c-120">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="ac03c-121">Informations sur la version :</span><span class="sxs-lookup"><span data-stu-id="ac03c-121">Version information:</span></span>

-   <span data-ttu-id="ac03c-122">Pour PS \_ 1 \_ 0 et PS \_ 1 \_ 1, vous pouvez utiliser \_ BX2 sur n’importe quel Registre source pour les instructions de texture de la forme texm3x2 \* et texm3x3 \* .</span><span class="sxs-lookup"><span data-stu-id="ac03c-122">For ps\_1\_0 and ps\_1\_1, you can use \_bx2 on any source register for texture instructions of the form texm3x2\* and texm3x3\*.</span></span> <span data-ttu-id="ac03c-123">\_BX2 ne peut pas être utilisé sur une autre instruction de texture telle que [texreg2ar-PS](texreg2ar---ps.md) ou [texreg2gb-PS](texreg2gb---ps.md).</span><span class="sxs-lookup"><span data-stu-id="ac03c-123">\_bx2 cannot be used on any of the other texture instructions such as [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md).</span></span>
-   <span data-ttu-id="ac03c-124">Pour PS \_ 1 \_ 2 et PS \_ 1 \_ 3, vous pouvez utiliser \_ BX2 sur n’importe quel Registre source pour toute instruction Tex, \* à l’exception de : [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [texbem-PS](texbem---ps.md) ou [texbeml-PS](texbeml---ps.md).</span><span class="sxs-lookup"><span data-stu-id="ac03c-124">For ps\_1\_2 and ps\_1\_3, you can use \_bx2 on any source register for any tex\* instruction except: [texreg2ar - ps](texreg2ar---ps.md), [texreg2gb - ps](texreg2gb---ps.md), [texbem - ps](texbem---ps.md) or [texbeml - ps](texbeml---ps.md).</span></span>

## <a name="example"></a><span data-ttu-id="ac03c-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="ac03c-125">Example</span></span>

<span data-ttu-id="ac03c-126">Cet exemple échantillonne une texture, convertit les données dans la plage comprise entre-1 et + 1, puis calcule un produit scalaire.</span><span class="sxs-lookup"><span data-stu-id="ac03c-126">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a><span data-ttu-id="ac03c-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ac03c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac03c-128">Modificateurs de Registre source du nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ac03c-128">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




