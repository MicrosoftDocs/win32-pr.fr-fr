---
title: " else"
description: La directive \ else marque une clause facultative d’un bloc de compilation conditionnelle défini par une directive \ ifdef, \ ifndef ou \ if. La directive \ else doit être la dernière directive avant la directive \ endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673474"
---
# <a name="else"></a><span data-ttu-id="14b96-104">\#else</span><span class="sxs-lookup"><span data-stu-id="14b96-104">\#else</span></span>

<span data-ttu-id="14b96-105">La directive **\# else** marque une clause facultative d’un bloc de compilation conditionnelle définie par une directive **\# ifdef**, **\# ifndef** ou **\# If** .</span><span class="sxs-lookup"><span data-stu-id="14b96-105">The **\#else** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="14b96-106">La directive **\# else** doit être la dernière directive avant la directive **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="14b96-106">The **\#else** directive must be the last directive before the **\#endif** directive.</span></span>

``` syntax
#else
```

<span data-ttu-id="14b96-107">Cette directive n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="14b96-107">This directive has no parameters.</span></span>

## <a name="example"></a><span data-ttu-id="14b96-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="14b96-108">Example</span></span>

<span data-ttu-id="14b96-109">Cet exemple compile la deuxième instruction [**bitmap**](bitmap-resource.md) uniquement si debug n’est pas défini :</span><span class="sxs-lookup"><span data-stu-id="14b96-109">This example compiles the second [**BITMAP**](bitmap-resource.md) statement only if DEBUG is not defined:</span></span>

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="14b96-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14b96-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14b96-111">Directives de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="14b96-111">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




