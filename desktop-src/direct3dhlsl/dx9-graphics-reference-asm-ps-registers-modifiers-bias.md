---
title: Décalage du Registre source
description: Soustraire 0,5 de tous les composants.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940335"
---
# <a name="source-register-bias"></a><span data-ttu-id="7d753-103">Décalage du Registre source</span><span class="sxs-lookup"><span data-stu-id="7d753-103">Source Register Bias</span></span>

<span data-ttu-id="7d753-104">Soustraire 0,5 de tous les composants.</span><span class="sxs-lookup"><span data-stu-id="7d753-104">Subtract 0.5 from all components.</span></span>

## <a name="registers"></a><span data-ttu-id="7d753-105">Registres</span><span class="sxs-lookup"><span data-stu-id="7d753-105">Registers</span></span>

<span data-ttu-id="7d753-106">Registre source.</span><span class="sxs-lookup"><span data-stu-id="7d753-106">Source register.</span></span> <span data-ttu-id="7d753-107">Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="7d753-107">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d753-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7d753-108">Remarks</span></span>

<span data-ttu-id="7d753-109">Le contenu du Registre n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="7d753-109">The contents of the register are not changed.</span></span> <span data-ttu-id="7d753-110">Le modificateur est appliqué uniquement aux données lues à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="7d753-110">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="7d753-111">Le biais est appliqué aux quatre canaux de couleurs (RVBA) comme suit :</span><span class="sxs-lookup"><span data-stu-id="7d753-111">The bias is applied to all four color channels (RGBA) as follows:</span></span>


```
output = (input - 0.5)
```



<span data-ttu-id="7d753-112">L’effet est de modifier les données comprises dans la plage de 0 à 1 pour qu’elles se trouvent dans la plage comprise entre-0,5 et 0,5.</span><span class="sxs-lookup"><span data-stu-id="7d753-112">The effect is to modify data that was in the range 0 to 1 to be in the range -0.5 to 0.5.</span></span> <span data-ttu-id="7d753-113">L’application d’un décalage aux données en dehors de cette plage peut produire des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="7d753-113">Applying bias to data outside this range may produce undefined results.</span></span>

> [!Note]  
> <span data-ttu-id="7d753-114">Ce modificateur s’exclut mutuellement avec le [Registre source inversé](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), donc il ne peut pas être appliqué au même registre.</span><span class="sxs-lookup"><span data-stu-id="7d753-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

 

<span data-ttu-id="7d753-115">Ce modificateur est destiné à être utilisé avec les instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="7d753-115">This modifier is for use with the arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="7d753-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="7d753-116">Example</span></span>

<span data-ttu-id="7d753-117">Cet exemple effectue la même opération que D3DTOP \_ ADDSIGNED dans DirectX 6,0 et 7,0 syntaxe de texture multiple.</span><span class="sxs-lookup"><span data-stu-id="7d753-117">This example performs the same operation as D3DTOP\_ADDSIGNED in DirectX 6.0 and 7.0 multiple texture syntax.</span></span>


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a><span data-ttu-id="7d753-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d753-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d753-119">Modificateurs de Registre source du nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="7d753-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




