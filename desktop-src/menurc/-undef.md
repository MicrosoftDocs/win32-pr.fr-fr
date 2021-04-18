---
title: " undef"
description: La directive \ undef supprime la définition actuelle du nom spécifié. Toutes les occurrences ultérieures du nom sont traitées sans remplacement.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512664"
---
# <a name="undef"></a><span data-ttu-id="f6f94-104">\#undef</span><span class="sxs-lookup"><span data-stu-id="f6f94-104">\#undef</span></span>

<span data-ttu-id="f6f94-105">La directive **\# undef** supprime la définition actuelle du nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="f6f94-105">The **\#undef** directive removes the current definition of the specified name.</span></span> <span data-ttu-id="f6f94-106">Toutes les occurrences ultérieures du nom sont traitées sans remplacement.</span><span class="sxs-lookup"><span data-stu-id="f6f94-106">All subsequent occurrences of the name are processed without replacement.</span></span>

``` syntax
#undef name
```

<dl> <dt>

<span data-ttu-id="f6f94-107"><span id="name"></span><span id="NAME"></span>*nomme*</span><span class="sxs-lookup"><span data-stu-id="f6f94-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="f6f94-108">Nom à supprimer.</span><span class="sxs-lookup"><span data-stu-id="f6f94-108">Name to be removed.</span></span> <span data-ttu-id="f6f94-109">Cette valeur correspond à toute combinaison de lettres, de chiffres et de signes de ponctuation valide pour le préprocesseur C/C++.</span><span class="sxs-lookup"><span data-stu-id="f6f94-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="f6f94-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="f6f94-110">Example</span></span>

<span data-ttu-id="f6f94-111">Cet exemple supprime les définitions pour les noms non nuls et USERCLASS :</span><span class="sxs-lookup"><span data-stu-id="f6f94-111">This example removes the definitions for the names nonzero and USERCLASS:</span></span>

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a><span data-ttu-id="f6f94-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6f94-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6f94-113">Directives de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="f6f94-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




