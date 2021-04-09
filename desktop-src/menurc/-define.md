---
title: " define"
description: La directive \ define assigne la valeur donnée au nom spécifié. Toutes les occurrences ultérieures du nom sont remplacées par la valeur.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674166"
---
# <a name="define"></a><span data-ttu-id="206fd-104">\#définition</span><span class="sxs-lookup"><span data-stu-id="206fd-104">\#define</span></span>

<span data-ttu-id="206fd-105">La directive **\# define** assigne la valeur donnée au nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="206fd-105">The **\#define** directive assigns the given value to the specified name.</span></span> <span data-ttu-id="206fd-106">Toutes les occurrences ultérieures du nom sont remplacées par la valeur.</span><span class="sxs-lookup"><span data-stu-id="206fd-106">All subsequent occurrences of the name are replaced by the value.</span></span>

``` syntax
#define name value
```

<dl> <dt>

<span data-ttu-id="206fd-107"><span id="name"></span><span id="NAME"></span>*nomme*</span><span class="sxs-lookup"><span data-stu-id="206fd-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="206fd-108">Nom à définir.</span><span class="sxs-lookup"><span data-stu-id="206fd-108">Name to be defined.</span></span> <span data-ttu-id="206fd-109">Cette valeur correspond à toute combinaison de lettres, de chiffres et de signes de ponctuation valide pour le préprocesseur C/C++.</span><span class="sxs-lookup"><span data-stu-id="206fd-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="206fd-110"><span id="value"></span><span id="VALUE"></span>*ajoutée*</span><span class="sxs-lookup"><span data-stu-id="206fd-110"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="206fd-111">Entier, chaîne de caractères ou ligne de texte.</span><span class="sxs-lookup"><span data-stu-id="206fd-111">Integer, character string, or line of text.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="206fd-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="206fd-112">Example</span></span>

<span data-ttu-id="206fd-113">Cet exemple assigne des valeurs à des noms non nuls et USERCLASS :</span><span class="sxs-lookup"><span data-stu-id="206fd-113">This example assigns values to the names NONZERO and USERCLASS:</span></span>

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a><span data-ttu-id="206fd-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="206fd-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="206fd-115">Directives de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="206fd-115">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




