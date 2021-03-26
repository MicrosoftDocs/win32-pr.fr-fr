---
title: Mise à l’échelle du Registre source x 2
description: Multipliez la valeur par deux avant de l’utiliser dans l’instruction.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971454"
---
# <a name="source-register-scale-x-2"></a><span data-ttu-id="3f567-103">Mise à l’échelle du Registre source x 2</span><span class="sxs-lookup"><span data-stu-id="3f567-103">Source Register Scale x 2</span></span>

<span data-ttu-id="3f567-104">Multipliez la valeur par deux avant de l’utiliser dans l’instruction.</span><span class="sxs-lookup"><span data-stu-id="3f567-104">Multiply the value by two before using it in the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f567-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f567-105">Syntax</span></span>


```
register_x2
```



## <a name="register"></a><span data-ttu-id="3f567-106">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="3f567-106">Register</span></span>

<span data-ttu-id="3f567-107">Registre source.</span><span class="sxs-lookup"><span data-stu-id="3f567-107">Source register.</span></span> <span data-ttu-id="3f567-108">Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="3f567-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f567-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3f567-109">Remarks</span></span>

<span data-ttu-id="3f567-110">Le contenu du Registre n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="3f567-110">The contents of the register are not changed.</span></span> <span data-ttu-id="3f567-111">Le modificateur est appliqué uniquement aux données lues à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="3f567-111">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="3f567-112">Ce modificateur s’exclut mutuellement avec le [Registre source inversé](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), donc il ne peut pas être appliqué au même registre.</span><span class="sxs-lookup"><span data-stu-id="3f567-112">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

<span data-ttu-id="3f567-113">Ce modificateur est uniquement disponible pour les instructions arithmétiques dans la version 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="3f567-113">This modifier is only available to arithmetic instructions in version 1\_4.</span></span>

## <a name="example"></a><span data-ttu-id="3f567-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f567-114">Example</span></span>

<span data-ttu-id="3f567-115">Cet exemple échantillonne une texture, convertit les données dans la plage comprise entre-1 et + 1, puis calcule un produit scalaire.</span><span class="sxs-lookup"><span data-stu-id="3f567-115">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a><span data-ttu-id="3f567-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f567-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f567-117">Modificateurs de Registre source du nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3f567-117">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




