---
title: " elif"
description: La directive \ Elif marque une clause facultative d’un bloc de compilation conditionnelle défini par une directive \ ifdef, \ ifndef ou \ if.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029345"
---
# <a name="elif"></a><span data-ttu-id="d83c4-103">\#elif</span><span class="sxs-lookup"><span data-stu-id="d83c4-103">\#elif</span></span>

<span data-ttu-id="d83c4-104">La directive **\# Elif** marque une clause facultative d’un bloc de compilation conditionnelle définie par une directive **\# ifdef**, **\# ifndef** ou **\# If** .</span><span class="sxs-lookup"><span data-stu-id="d83c4-104">The **\#elif** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="d83c4-105">La directive contrôle la compilation conditionnelle du fichier de ressources en vérifiant l’expression constante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d83c4-105">The directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="d83c4-106">Si l’expression constante est différente de zéro, **\# Elif** demande au compilateur de poursuivre le traitement des instructions jusqu’à la directive **\# endif**, **\# else** ou **\# Elif** suivante, puis d’ignorer l’instruction après **\# endif**.</span><span class="sxs-lookup"><span data-stu-id="d83c4-106">If the constant expression is nonzero, **\#elif** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after **\#endif**.</span></span> <span data-ttu-id="d83c4-107">Si l’expression constante est égale à zéro, **\# Elif** demande au compilateur d’ignorer la directive **\# endif**, **\# else** ou **\# Elif** suivante.</span><span class="sxs-lookup"><span data-stu-id="d83c4-107">If the constant expression is zero, **\#elif** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span> <span data-ttu-id="d83c4-108">Vous pouvez utiliser n’importe quel nombre de directives **\# Elif** dans un bloc conditionnel.</span><span class="sxs-lookup"><span data-stu-id="d83c4-108">You can use any number of **\#elif** directives in a conditional block.</span></span>

``` syntax
#elif constant-expression
```

<dl> <dt>

<span data-ttu-id="d83c4-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span><span class="sxs-lookup"><span data-stu-id="d83c4-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="d83c4-110">Expression à vérifier.</span><span class="sxs-lookup"><span data-stu-id="d83c4-110">Expression to be checked.</span></span> <span data-ttu-id="d83c4-111">Cette valeur est un nom défini, une constante entière ou une expression comprenant des noms, des entiers et des opérateurs arithmétiques et relationnels.</span><span class="sxs-lookup"><span data-stu-id="d83c4-111">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="d83c4-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="d83c4-112">Example</span></span>

<span data-ttu-id="d83c4-113">Dans cet exemple, **\# Elif** demande au compilateur de traiter la deuxième instruction [**bitmap**](bitmap-resource.md) uniquement si la valeur assignée à la version de nom est inférieure à 7.</span><span class="sxs-lookup"><span data-stu-id="d83c4-113">In this example, **\#elif** directs the compiler to process the second [**BITMAP**](bitmap-resource.md) statement only if the value assigned to the name Version is less than 7.</span></span> <span data-ttu-id="d83c4-114">La directive **\# Elif** elle-même est traitée uniquement si la version est supérieure ou égale à 3.</span><span class="sxs-lookup"><span data-stu-id="d83c4-114">The **\#elif** directive itself is processed only if Version is greater than or equal to 3.</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="d83c4-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d83c4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d83c4-116">Directives de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="d83c4-116">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




