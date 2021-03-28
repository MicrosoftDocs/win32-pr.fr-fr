---
title: Négation du Registre source
description: Effectue une négation (y-x) sur tous les composants du Registre.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029100"
---
# <a name="source-register-negate"></a><span data-ttu-id="db020-103">Négation du Registre source</span><span class="sxs-lookup"><span data-stu-id="db020-103">Source Register Negate</span></span>

<span data-ttu-id="db020-104">Effectue une négation (y =-x) sur tous les composants du Registre.</span><span class="sxs-lookup"><span data-stu-id="db020-104">Performs a negate (y = -x), on all register components.</span></span>

## <a name="syntax"></a><span data-ttu-id="db020-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db020-105">Syntax</span></span>


```
- register
```



## <a name="registers"></a><span data-ttu-id="db020-106">Registres</span><span class="sxs-lookup"><span data-stu-id="db020-106">Registers</span></span>

<span data-ttu-id="db020-107">Registre source.</span><span class="sxs-lookup"><span data-stu-id="db020-107">Source Register.</span></span> <span data-ttu-id="db020-108">Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="db020-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db020-109">Notes</span><span class="sxs-lookup"><span data-stu-id="db020-109">Remarks</span></span>

<span data-ttu-id="db020-110">Le contenu du Registre n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="db020-110">The contents of the register are not changed.</span></span> <span data-ttu-id="db020-111">Le modificateur est appliqué uniquement aux données lues à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="db020-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="db020-112">L’opération de négation est appliquée aux quatre canaux de couleurs (RVBA).</span><span class="sxs-lookup"><span data-stu-id="db020-112">The negate operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="db020-113">Cette opération est effectuée après tout autre modificateur présent sur le même argument.</span><span class="sxs-lookup"><span data-stu-id="db020-113">This operation is performed after any other modifiers present on the same argument.</span></span>

<span data-ttu-id="db020-114">Ce modificateur s’exclut mutuellement avec le [Registre source inversé](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) , de sorte qu’il ne peut pas être appliqué au même registre.</span><span class="sxs-lookup"><span data-stu-id="db020-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="db020-115">Ce modificateur est destiné à être utilisé uniquement avec des instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="db020-115">This modifier is for use only with arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="db020-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="db020-116">Example</span></span>

<span data-ttu-id="db020-117">L’exemple suivant montre comment utiliser ce modificateur.</span><span class="sxs-lookup"><span data-stu-id="db020-117">The following example shows how to use this modifier.</span></span>


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a><span data-ttu-id="db020-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db020-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db020-119">Modificateurs de Registre source du nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="db020-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




