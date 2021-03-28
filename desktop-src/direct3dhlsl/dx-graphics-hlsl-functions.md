---
title: Fonctions (référence HLSL)
description: Les fonctions encapsulent les instructions HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313774"
---
# <a name="functions-hlsl-reference"></a><span data-ttu-id="d0c4a-103">Fonctions (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0c4a-103">Functions (HLSL reference)</span></span>

<span data-ttu-id="d0c4a-104">Les fonctions encapsulent les instructions HLSL.</span><span class="sxs-lookup"><span data-stu-id="d0c4a-104">Functions encapsulate HLSL statements.</span></span> <span data-ttu-id="d0c4a-105">Cela vous permet de déboguer un ensemble de fonctions, puis de les réutiliser dans les nuanceurs ou les effets.</span><span class="sxs-lookup"><span data-stu-id="d0c4a-105">This enables you to debug a set of functions and then reuse them across shaders or effects.</span></span> <span data-ttu-id="d0c4a-106">Vous pouvez créer une fonction qui encapsule les fonctionnalités d’un nuanceur de sommets, d’un nuanceur de pixels ou d’un nuanceur de texture.</span><span class="sxs-lookup"><span data-stu-id="d0c4a-106">You may want to create a function that encapsulates the functionality of a vertex shader, pixel shader or texture shader.</span></span> <span data-ttu-id="d0c4a-107">Dans d’autres cas, vous pouvez écrire une fonction d’assistance qui exécute une tâche couramment utilisée, puis appeler cette fonction d’assistance à partir de votre fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="d0c4a-107">Other times, you may want to write a helper function that performs some commonly used task, and then call that helper function from your shader function.</span></span> <span data-ttu-id="d0c4a-108">Les règles d’écriture des fonctions de nuanceur pour le langage HLSL sont très similaires à celles de l’écriture de fonctions C.</span><span class="sxs-lookup"><span data-stu-id="d0c4a-108">The rules for writing shader functions for HLSL are very similar to writing C functions.</span></span>

-   [<span data-ttu-id="d0c4a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0c4a-109">Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
-   [<span data-ttu-id="d0c4a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0c4a-110">Parameters</span></span>](dx-graphics-hlsl-function-parameters.md)
-   [<span data-ttu-id="d0c4a-111">Instruction return</span><span class="sxs-lookup"><span data-stu-id="d0c4a-111">Return Statement</span></span>](dx-graphics-hlsl-return.md)
-   [<span data-ttu-id="d0c4a-112">Signatures</span><span class="sxs-lookup"><span data-stu-id="d0c4a-112">Signatures</span></span>](dx-graphics-hlsl-signatures.md)

<span data-ttu-id="d0c4a-113">Le langage HLSL possède également un certain nombre de [**fonctions intrinsèques intégrées (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d0c4a-113">HLSL also has a number of built-in [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span></span> <span data-ttu-id="d0c4a-114">Étant donné que toutes les fonctions intrinsèques sont testées et optimisées pour les performances, il est recommandé d’utiliser une fonction intrinsèque lorsque cela est possible au lieu de créer votre propre fonction.</span><span class="sxs-lookup"><span data-stu-id="d0c4a-114">Because all intrinsic functions are tested and performance optimized, it is good practice to use an intrinsic function where possible instead of creating your own function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0c4a-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d0c4a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0c4a-116">Syntaxe du langage (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d0c4a-116">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




