---
title: " undef (directive)"
description: Directive de préprocesseur qui supprime la définition actuelle d’une constante ou d’une macro précédemment définie à l’aide de la directive \ define.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- Directive undef (HLSL)
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312553"
---
# <a name="undef-directive"></a><span data-ttu-id="57e27-104">\#undef (directive)</span><span class="sxs-lookup"><span data-stu-id="57e27-104">\#undef Directive</span></span>

<span data-ttu-id="57e27-105">Directive de préprocesseur qui supprime la définition actuelle d’une constante ou d’une macro précédemment définie à l’aide de la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) .</span><span class="sxs-lookup"><span data-stu-id="57e27-105">Preprocessor directive that removes the current definition of a constant or macro that was previously defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive.</span></span>



| <span data-ttu-id="57e27-106">\#*identificateur* undef</span><span class="sxs-lookup"><span data-stu-id="57e27-106">\#undef *identifier*</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="57e27-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57e27-107">Parameters</span></span>



| <span data-ttu-id="57e27-108">Élément</span><span class="sxs-lookup"><span data-stu-id="57e27-108">Item</span></span>                                                                              | <span data-ttu-id="57e27-109">Description</span><span class="sxs-lookup"><span data-stu-id="57e27-109">Description</span></span>                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57e27-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificateur*</span><span class="sxs-lookup"><span data-stu-id="57e27-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="57e27-111">Identificateur de la constante ou de la macro dont la définition doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="57e27-111">Identifier of the constant or macro to remove the definition of.</span></span> <span data-ttu-id="57e27-112">Si vous ne définissez pas une macro, fournissez uniquement l’identificateur, et non la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="57e27-112">If you are undefining a macro, provide only the identifier, not the parameter list.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="57e27-113">Notes</span><span class="sxs-lookup"><span data-stu-id="57e27-113">Remarks</span></span>

<span data-ttu-id="57e27-114">Vous pouvez appliquer la \# directive undef à un identificateur qui n’a pas de définition précédente. cela garantit que l’identificateur n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="57e27-114">You can apply the \#undef directive to an identifier that has no previous definition; this ensures that the identifier is undefined.</span></span> <span data-ttu-id="57e27-115">Le remplacement de macro n’est pas effectué dans les \# instructions undef.</span><span class="sxs-lookup"><span data-stu-id="57e27-115">Macro replacement is not performed within \#undef statements.</span></span>

<span data-ttu-id="57e27-116">La \# directive undef est généralement associée à une directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) pour créer une région dans un programme source dans lequel un identificateur a une signification particulière.</span><span class="sxs-lookup"><span data-stu-id="57e27-116">The \#undef directive is typically paired with a [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive to create a region in a source program in which an identifier has a special meaning.</span></span> <span data-ttu-id="57e27-117">Par exemple, une fonction spécifique du programme source peut utiliser des constantes manifestes pour définir les valeurs spécifiques à l'environnement qui n'affectent pas le reste du programme.</span><span class="sxs-lookup"><span data-stu-id="57e27-117">For example, a specific function of the source program can use manifest constants to define environment-specific values that do not affect the rest of the program.</span></span> <span data-ttu-id="57e27-118">La \# directive undef fonctionne également avec la directive [) pour contrôler la compilation conditionnelle du programme source.</span><span class="sxs-lookup"><span data-stu-id="57e27-118">The \#undef directive also works with the [) directive to control conditional compilation of the source program.</span></span>

<span data-ttu-id="57e27-119">Les constantes et les macros peuvent être non définies à partir de la ligne de commande à l’aide de l’option/U, suivie des identificateurs à non définir.</span><span class="sxs-lookup"><span data-stu-id="57e27-119">Constants and macros can be undefined from the command line using the /U option, followed by the identifiers to be undefined.</span></span> <span data-ttu-id="57e27-120">Cela équivaut à ajouter une séquence de \# directives undef au début du fichier source.</span><span class="sxs-lookup"><span data-stu-id="57e27-120">This is equivalent to adding a sequence of \#undef directives at the beginning of the source file.</span></span>

## <a name="examples"></a><span data-ttu-id="57e27-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="57e27-121">Examples</span></span>

<span data-ttu-id="57e27-122">L’exemple suivant montre comment utiliser la \# directive undef pour supprimer les définitions d’une constante symbolique et une macro.</span><span class="sxs-lookup"><span data-stu-id="57e27-122">The following example shows how to use the \#undef directive to remove definitions of a symbolic constant and a macro.</span></span>


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a><span data-ttu-id="57e27-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57e27-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57e27-124">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57e27-124">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="57e27-125">\#define, directive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57e27-125">\#define Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="57e27-126">\#Si,)</span><span class="sxs-lookup"><span data-stu-id="57e27-126">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





