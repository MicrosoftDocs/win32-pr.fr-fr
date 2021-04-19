---
title: " ifndef"
description: La directive \ ifndef contrôle la compilation conditionnelle du fichier de ressources en vérifiant le nom spécifié.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509592"
---
# <a name="ifndef"></a><span data-ttu-id="dd271-103">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="dd271-103">\#ifndef</span></span>

<span data-ttu-id="dd271-104">La directive **\# ifndef** contrôle la compilation conditionnelle du fichier de ressources en vérifiant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd271-104">The **\#ifndef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="dd271-105">Si le nom n’a pas été défini ou si sa définition a été supprimée à l’aide de la directive **\# undef** , **\# ifndef** indique au compilateur de poursuivre le traitement des instructions jusqu’à la directive **\# endif**, **\# else** ou **\# Elif** suivante, puis d’ignorer l’instruction après la directive **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="dd271-105">If the name has not been defined or if its definition has been removed by using the **\#undef** directive, **\#ifndef** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="dd271-106">Si le nom est défini, **\# ifndef** indique au compilateur d’ignorer la directive **\# endif**, **\# else** ou **\# Elif** suivante.</span><span class="sxs-lookup"><span data-stu-id="dd271-106">If the name is defined, **\#ifndef** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#ifndef name
```

<dl> <dt>

<span data-ttu-id="dd271-107"><span id="name"></span><span id="NAME"></span>*nomme*</span><span class="sxs-lookup"><span data-stu-id="dd271-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="dd271-108">Nom à vérifier par la directive.</span><span class="sxs-lookup"><span data-stu-id="dd271-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="dd271-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="dd271-109">Example</span></span>

<span data-ttu-id="dd271-110">Cet exemple compile l’instruction [**bitmap**](bitmap-resource.md) uniquement si l’optimisation n’est pas définie :</span><span class="sxs-lookup"><span data-stu-id="dd271-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Optimize is not defined:</span></span>

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="dd271-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd271-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd271-112">Directives de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="dd271-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




