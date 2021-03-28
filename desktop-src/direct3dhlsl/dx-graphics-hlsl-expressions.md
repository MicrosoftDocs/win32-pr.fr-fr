---
title: Expressions
description: Une expression est une séquence de variables et de littéraux, avec des signes de ponctuation par opérateur. Un littéral est une valeur de données explicite, telle que 1 pour un entier ou 2,1 pour un nombre à virgule flottante. Les littéraux sont souvent utilisés pour assigner une valeur à une variable.
ms.assetid: b9ba1c1f-3338-45f3-9901-38eaf00278cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6149968cff0d38f6bff47d61c7e3b9c569bbe3cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196597"
---
# <a name="expressions"></a><span data-ttu-id="345ec-105">Expressions</span><span class="sxs-lookup"><span data-stu-id="345ec-105">Expressions</span></span>

<span data-ttu-id="345ec-106">Une expression est une séquence de [variables](dx-graphics-hlsl-variable-syntax.md) et de littéraux, avec des signes de ponctuation par [opérateur](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="345ec-106">An expression is a sequence of [variables](dx-graphics-hlsl-variable-syntax.md) and literals, punctuated by [operators](dx-graphics-hlsl-statement-blocks.md).</span></span> <span data-ttu-id="345ec-107">Un littéral est une valeur de données explicite, telle que 1 pour un entier ou 2,1 pour un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="345ec-107">A literal is an explicit data value, such as 1 for an integer or 2.1 for a floating-point number.</span></span> <span data-ttu-id="345ec-108">Les littéraux sont souvent utilisés pour assigner une valeur à une variable.</span><span class="sxs-lookup"><span data-stu-id="345ec-108">Literals are often used to assign a value to a variable.</span></span>

<span data-ttu-id="345ec-109">Expression suivie d’un point-virgule (;) est appelée une instruction.</span><span class="sxs-lookup"><span data-stu-id="345ec-109">An expression followed by a semicolon (;) is called a statement.</span></span> <span data-ttu-id="345ec-110">Les instructions vont de la complexité des expressions simples aux blocs d’instructions qui accomplissent une séquence d’actions.</span><span class="sxs-lookup"><span data-stu-id="345ec-110">Statements range in complexity from simple expressions to blocks of statements that accomplish a sequence of actions.</span></span> <span data-ttu-id="345ec-111">Les instructions de contrôle de Flow déterminent l’exécution des instructions de commande.</span><span class="sxs-lookup"><span data-stu-id="345ec-111">Flow-control statements determine the order statements are executed.</span></span>

<span data-ttu-id="345ec-112">Un bloc d’instructions indique également la sous-étendue.</span><span class="sxs-lookup"><span data-stu-id="345ec-112">A statement block also indicates subscope.</span></span> <span data-ttu-id="345ec-113">Les variables déclarées dans un bloc d’instructions sont uniquement reconnues dans le bloc.</span><span class="sxs-lookup"><span data-stu-id="345ec-113">Variables declared within a statement block are only recognized within the block.</span></span> <span data-ttu-id="345ec-114">Les instructions HLSL déterminent l’ordre dans lequel les expressions sont évaluées.</span><span class="sxs-lookup"><span data-stu-id="345ec-114">HLSL statements determine the order in which expressions are evaluated.</span></span> <span data-ttu-id="345ec-115">Chaque expression peut être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="345ec-115">Each expression can be one of the following.</span></span>

-   <span data-ttu-id="345ec-116">Une expression</span><span class="sxs-lookup"><span data-stu-id="345ec-116">An expression</span></span>
-   <span data-ttu-id="345ec-117">Un [bloc d’instructions](dx-graphics-hlsl-statement-blocks.md)</span><span class="sxs-lookup"><span data-stu-id="345ec-117">A [statement block](dx-graphics-hlsl-statement-blocks.md)</span></span>
-   <span data-ttu-id="345ec-118">[Instruction return](dx-graphics-hlsl-return.md)</span><span class="sxs-lookup"><span data-stu-id="345ec-118">A [return statement](dx-graphics-hlsl-return.md)</span></span>
-   <span data-ttu-id="345ec-119">Une [instruction Flow-Control](dx-graphics-hlsl-flow-control.md)</span><span class="sxs-lookup"><span data-stu-id="345ec-119">A [flow-control statement](dx-graphics-hlsl-flow-control.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="345ec-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="345ec-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="345ec-121">Instructions (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="345ec-121">Statements (DirectX HLSL)</span></span>](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




