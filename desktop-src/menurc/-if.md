---
title: " if"
description: La directive \ if contrôle la compilation conditionnelle du fichier de ressources en vérifiant l’expression constante spécifiée.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364d6f5eb818813f61f6428446effb4793b96b2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510609"
---
# <a name="if"></a><span data-ttu-id="1c18b-103">\#que</span><span class="sxs-lookup"><span data-stu-id="1c18b-103">\#if</span></span>

<span data-ttu-id="1c18b-104">La directive **\# If** contrôle la compilation conditionnelle du fichier de ressources en vérifiant l’expression constante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1c18b-104">The **\#if** directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="1c18b-105">Si l’expression constante est différente de zéro, **\# si** demande au compilateur de poursuivre le traitement des instructions jusqu’à la directive **\# endif**, **\# else** ou **\# Elif** suivante, puis d’ignorer l’instruction après la directive **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="1c18b-105">If the constant expression is nonzero, **\#if** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="1c18b-106">Si l’expression constante est égale à zéro, **\# si** demande au compilateur d’ignorer la directive **\# endif**, **\# else** ou **\# Elif** suivante.</span><span class="sxs-lookup"><span data-stu-id="1c18b-106">If the constant expression is zero, **\#if** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#if constant-expression
```

<dl> <dt>

<span data-ttu-id="1c18b-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span><span class="sxs-lookup"><span data-stu-id="1c18b-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="1c18b-108">Expression à vérifier.</span><span class="sxs-lookup"><span data-stu-id="1c18b-108">Expression to be checked.</span></span> <span data-ttu-id="1c18b-109">Cette valeur est un nom défini, une constante entière ou une expression comprenant des noms, des entiers et des opérateurs arithmétiques et relationnels.</span><span class="sxs-lookup"><span data-stu-id="1c18b-109">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="1c18b-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="1c18b-110">Example</span></span>

<span data-ttu-id="1c18b-111">Cet exemple compile l’instruction [**bitmap**](bitmap-resource.md) uniquement si la valeur affectée à la valeur est inférieure à 3 :</span><span class="sxs-lookup"><span data-stu-id="1c18b-111">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if the value assigned Version is less than 3:</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="1c18b-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1c18b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c18b-113">Directives de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="1c18b-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




