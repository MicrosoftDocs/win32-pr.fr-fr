---
title: " ifdef"
description: La directive \ ifdef contrôle la compilation conditionnelle du fichier de ressources en vérifiant le nom spécifié.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379976"
---
# <a name="ifdef"></a><span data-ttu-id="47274-103">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="47274-103">\#ifdef</span></span>

<span data-ttu-id="47274-104">La directive **\# ifdef** contrôle la compilation conditionnelle du fichier de ressources en vérifiant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="47274-104">The **\#ifdef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="47274-105">Si le nom a été défini à l’aide d’une directive de **\# définition** ou à l’aide de l’option de ligne de commande **/d** avec le compilateur de ressources, **\# ifdef** demande au compilateur de continuer avec l’instruction qui suit immédiatement la directive **\# ifdef** .</span><span class="sxs-lookup"><span data-stu-id="47274-105">If the name has been defined by using a **\#define** directive or by using the **/d** command-line option with the resource compiler, **\#ifdef** directs the compiler to continue with the statement immediately after the **\#ifdef** directive.</span></span> <span data-ttu-id="47274-106">Si le nom n’a pas été défini, **\# ifdef** demande au compilateur d’ignorer toutes les instructions jusqu’à la directive **\# endif** suivante.</span><span class="sxs-lookup"><span data-stu-id="47274-106">If the name has not been defined, **\#ifdef** directs the compiler to skip all statements up to the next **\#endif** directive.</span></span>

``` syntax
#ifdef name
```

<dl> <dt>

<span data-ttu-id="47274-107"><span id="name"></span><span id="NAME"></span>*nomme*</span><span class="sxs-lookup"><span data-stu-id="47274-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="47274-108">Nom à vérifier par la directive.</span><span class="sxs-lookup"><span data-stu-id="47274-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="47274-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="47274-109">Example</span></span>

<span data-ttu-id="47274-110">Cet exemple compile l’instruction [**bitmap**](bitmap-resource.md) uniquement si debug est défini :</span><span class="sxs-lookup"><span data-stu-id="47274-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Debug is defined:</span></span>

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="47274-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47274-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47274-112">Directives de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="47274-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




