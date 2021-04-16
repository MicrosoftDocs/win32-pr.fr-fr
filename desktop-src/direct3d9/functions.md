---
description: Une fonction est le bloc de construction d’un nuanceur créé dans le langage de haut niveau. Si vous préférez écrire des nuanceurs dans un langage de style C plutôt que dans un langage assembleur, vous souhaiterez peut-être écrire des fonctions.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Syntaxe des fonctions Effect (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520908"
---
# <a name="effect-function-syntax-direct3d-9"></a><span data-ttu-id="a413c-104">Syntaxe des fonctions Effect (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a413c-104">Effect Function Syntax (Direct3D 9)</span></span>

<span data-ttu-id="a413c-105">Une fonction est le bloc de construction d’un nuanceur créé dans le langage de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="a413c-105">A function is the building block for a shader created in the high-level language.</span></span> <span data-ttu-id="a413c-106">Si vous préférez écrire des nuanceurs dans un langage de style C plutôt que dans un langage assembleur, vous souhaiterez peut-être écrire des fonctions.</span><span class="sxs-lookup"><span data-stu-id="a413c-106">If you prefer to write shaders in a C-style language instead of in assembly language, you will want to write functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a413c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a413c-107">Syntax</span></span>


```
type id ( [ parameters ] )  
    { body }
```



<span data-ttu-id="a413c-108">Les fonctions ne modifient pas les valeurs de paramètre dans un effet.</span><span class="sxs-lookup"><span data-stu-id="a413c-108">Functions do not change parameter values in an effect.</span></span>

-   <span data-ttu-id="a413c-109">type : toute [référence valide pour](../direct3dhlsl/dx-graphics-hlsl-reference.md) le type HLSL.</span><span class="sxs-lookup"><span data-stu-id="a413c-109">type - Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span>
-   <span data-ttu-id="a413c-110">ID : nom unique.</span><span class="sxs-lookup"><span data-stu-id="a413c-110">id - A unique name.</span></span>
-   <span data-ttu-id="a413c-111">paramètres : paramètres de fonction.</span><span class="sxs-lookup"><span data-stu-id="a413c-111">parameters - Function parameters.</span></span>
-   <span data-ttu-id="a413c-112">Body : corps de la fonction.</span><span class="sxs-lookup"><span data-stu-id="a413c-112">body - The body of the function.</span></span>

<span data-ttu-id="a413c-113">Les fonctions sont générées à partir du langage de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="a413c-113">Functions are built from the high-level language.</span></span> <span data-ttu-id="a413c-114">Consultez [référence pour le langage HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a413c-114">See [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a413c-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a413c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a413c-116">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="a413c-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
