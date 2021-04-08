---
title: Descripteurs de corrélation
description: Un descripteur de corrélation est une chaîne de format qui décrit une expression basée sur un argument lié à un autre argument.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842666"
---
# <a name="correlation-descriptors"></a><span data-ttu-id="80cdd-103">Descripteurs de corrélation</span><span class="sxs-lookup"><span data-stu-id="80cdd-103">Correlation Descriptors</span></span>

<span data-ttu-id="80cdd-104">Un descripteur de corrélation est une chaîne de format qui décrit une expression basée sur un argument lié à un autre argument.</span><span class="sxs-lookup"><span data-stu-id="80cdd-104">A correlation descriptor is a format string that describes an expression based on one argument related to another argument.</span></span> <span data-ttu-id="80cdd-105">Un descripteur de corrélation est nécessaire pour gérer la sémantique liée à des attributs tels que la \[ **taille \_ est ()** \] , la \[ **longueur \_ est ()** \] , le \[ **commutateur \_ est ()** \] et \[ **IID \_ est ()** \] .</span><span class="sxs-lookup"><span data-stu-id="80cdd-105">A correlation descriptor is needed for handling semantics related to attributes like \[**size\_is()**\], \[**length\_is()**\], \[**switch\_is()**\] and \[**iid\_is()**\].</span></span> <span data-ttu-id="80cdd-106">Les descripteurs de corrélation sont utilisés avec les tableaux, les pointeurs dimensionnés, les unions et les pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="80cdd-106">Correlation descriptors are used with arrays, sized pointers, unions, and interface pointers.</span></span> <span data-ttu-id="80cdd-107">La valeur de l’expression finale peut être une taille, une longueur, un discriminante d’Union ou un pointeur vers un IID, respectivement.</span><span class="sxs-lookup"><span data-stu-id="80cdd-107">The eventual expression value can be a size, a length, a union discriminant, or a pointer to an IID, respectively.</span></span> <span data-ttu-id="80cdd-108">En termes de chaînes de format, les descripteurs de corrélation sont utilisés avec les tableaux, les unions et les pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="80cdd-108">In terms of format strings, correlation descriptors are used with arrays, unions, and interface pointers.</span></span> <span data-ttu-id="80cdd-109">Un pointeur dimensionné est décrit dans chaînes de format en tant que pointeur vers un tableau.</span><span class="sxs-lookup"><span data-stu-id="80cdd-109">A sized pointer is described in format strings as a pointer to an array.</span></span>

<span data-ttu-id="80cdd-110">Il existe deux routines effectuant des calculs d’expressions de base : NdrpComputeConformance est utilisé pour les tailles, commutateurs et IID, \* tandis que NdrpComputeVariance est utilisé pour les longueurs.</span><span class="sxs-lookup"><span data-stu-id="80cdd-110">There are two routines performing basic expression calculations: NdrpComputeConformance is used for sizes, switches and IID\* while NdrpComputeVariance is used for lengths.</span></span> <span data-ttu-id="80cdd-111">Il existe également une routine unique pour effectuer une validation de valeur de corrélation pour les fonctionnalités de déni d’attaque.</span><span class="sxs-lookup"><span data-stu-id="80cdd-111">There is also a single routine to perform a correlation value validation for denial-of-attack functionality.</span></span>

<span data-ttu-id="80cdd-112">Les descripteurs de corrélation ont été conçus pour prendre en charge uniquement des expressions très limitées.</span><span class="sxs-lookup"><span data-stu-id="80cdd-112">Correlation descriptors have been designed to support only very limited expressions.</span></span> <span data-ttu-id="80cdd-113">Pour les situations complexes, le compilateur génère une routine d’évaluation d’expression qui doit être appelée par le moteur quand cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="80cdd-113">For complicated situations, the compiler generates an expression evaluation routine to be called by the engine when needed.</span></span>

<span data-ttu-id="80cdd-114">Un descripteur de corrélation a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="80cdd-114">A correlation descriptor has the following format:</span></span>

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

<span data-ttu-id="80cdd-115">Le type de corrélation du descripteur \_ de corrélation<1> se compose de deux quartets : les 4 bits de poids fort décrivent où l’expression peut être trouvée et les 4 bits inférieurs décrivent le type de la valeur de l’expression.</span><span class="sxs-lookup"><span data-stu-id="80cdd-115">The correlation descriptor correlation\_type<1> consists of two nibbles: the upper 4 bits describe where the expression can be found and the lower 4 bits describe the type of the expression value.</span></span>

<span data-ttu-id="80cdd-116">Le Quartet supérieur peut avoir l’une des cinq valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="80cdd-116">The upper nibble can have one of these five values:</span></span>

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span data-ttu-id="80cdd-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>\_conformité normale \_ FC</span><span class="sxs-lookup"><span data-stu-id="80cdd-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>FC\_NORMAL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="80cdd-118">Une situation normale de conformité, telle que celle décrite dans un champ d’une structure.</span><span class="sxs-lookup"><span data-stu-id="80cdd-118">A normal case of conformance, such as that described in a field of a structure.</span></span>

</dd> <dt>

<span data-ttu-id="80cdd-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>\_conformité du pointeur FC \_</span><span class="sxs-lookup"><span data-stu-id="80cdd-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC\_POINTER\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="80cdd-120">Pour les pointeurs avec attributs (la **taille \_ est ()**, la **longueur \_ est ()**) qui sont des champs dans une structure.</span><span class="sxs-lookup"><span data-stu-id="80cdd-120">For attributed pointers (**size\_is()**, **length\_is()**) which are fields in a structure.</span></span> <span data-ttu-id="80cdd-121">Cela affecte la façon dont le pointeur de la mémoire de base est défini.</span><span class="sxs-lookup"><span data-stu-id="80cdd-121">This affects the way the base memory pointer is set.</span></span>

</dd> <dt>

<span data-ttu-id="80cdd-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>\_ \_ conformité au niveau supérieur FC \_</span><span class="sxs-lookup"><span data-stu-id="80cdd-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC\_TOP\_LEVEL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="80cdd-123">Pour la conformité de niveau supérieur décrite par un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="80cdd-123">For top-level conformance described by another parameter.</span></span>

</dd> <dt>

<span data-ttu-id="80cdd-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>\_ \_ conformité multithread à niveau supérieur \_ FC \_</span><span class="sxs-lookup"><span data-stu-id="80cdd-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>FC\_TOP\_LEVEL\_MULTID\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="80cdd-125">Pour la conformité de niveau supérieur d’un tableau multidimensionnel décrit par un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="80cdd-125">For top-level conformance of a multidimensional array described by another parameter.</span></span>

> [!Note]  
> <span data-ttu-id="80cdd-126">Les pointeurs et les tableaux de taille multidimensionnelle déclenchent un commutateur à [**– Oicf**](/windows/desktop/Midl/-oi).</span><span class="sxs-lookup"><span data-stu-id="80cdd-126">Multidimensional sized arrays and pointers trigger a switch to [**–Oicf**](/windows/desktop/Midl/-oi).</span></span>

 

</dd> <dt>

<span data-ttu-id="80cdd-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>CONFORMITÉ de la \_ constante FC \_</span><span class="sxs-lookup"><span data-stu-id="80cdd-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC\_CONSTANT\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="80cdd-128">Pour une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="80cdd-128">For a constant value.</span></span> <span data-ttu-id="80cdd-129">Le compilateur Précalcule la valeur à partir d’une expression constante fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="80cdd-129">The compiler precalculates the value from a constant expression supplied by the user.</span></span> <span data-ttu-id="80cdd-130">Dans ce cas, les 3 octets suivants dans la description de conformité contiennent les 3 octets inférieurs d’une longue qui décrivent la taille de la conformité.</span><span class="sxs-lookup"><span data-stu-id="80cdd-130">When this is the case, the subsequent 3 bytes in the conformance description contain the lower 3 bytes of a long describing the conformance size.</span></span> <span data-ttu-id="80cdd-131">Aucun calcul supplémentaire n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="80cdd-131">No further computation is required.</span></span>

</dd> </dl>

<span data-ttu-id="80cdd-132">Le Quartet inférieur donne le type de la valeur qui doit être extraite de la mémoire :</span><span class="sxs-lookup"><span data-stu-id="80cdd-132">The lower nibble gives the type of the value that needs to be extracted from memory:</span></span>

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> <span data-ttu-id="80cdd-133">les expressions 64 bits ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="80cdd-133">64-bit expressions are not supported.</span></span> <span data-ttu-id="80cdd-134">FC \_ hyper est utilisé uniquement pour **IID \_ est ()** sur les plateformes 64 bits pour extraire la valeur de pointeur pour IID \* .</span><span class="sxs-lookup"><span data-stu-id="80cdd-134">FC\_HYPER is used only for **iid\_is()** on 64-bit platforms to extract the pointer value for IID\*.</span></span>
>
> <span data-ttu-id="80cdd-135">Le compilateur définit le Quartet de type sur zéro dans les cas suivants : expression constante mentionnée ci-dessus et lorsque la routine d’expression d’évaluation doit être appelée, par exemple, lorsque la conformité à la \_ constante FC \_ et le \_ rappel FC sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="80cdd-135">The compiler sets the type nibble to zero for the following cases: constant expression mentioned above and when evaluation expression routine needs to be called, for example, when FC\_CONSTANT\_CONFORMANCE and FC\_CALLBACK are used.</span></span>

 

<span data-ttu-id="80cdd-136">La taille \_ est le \_ champ op<1> permet d’appliquer l’une des opérations suivantes à la variable de conformité :</span><span class="sxs-lookup"><span data-stu-id="80cdd-136">The size\_is\_op<1> field allows for one of the following operations to be applied to the conformance variable:</span></span>

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

<span data-ttu-id="80cdd-137">La \_ constante de DÉréférencement FC est utilisée pour que la corrélation soit un point, comme pour la **\[ taille \_ est ( \* pl) \]**.</span><span class="sxs-lookup"><span data-stu-id="80cdd-137">The FC\_DEREFERENCE constant is used for correlation being a pointee, like for **\[size\_is(\*pL)\]**.</span></span> <span data-ttu-id="80cdd-138">Les opérateurs arithmétiques utilisent simplement la constante indiquée.</span><span class="sxs-lookup"><span data-stu-id="80cdd-138">Arithmetic operators just use the indicated constant.</span></span> <span data-ttu-id="80cdd-139">La \_ constante de rappel FC indique qu’une routine d’évaluation de l’expression doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="80cdd-139">The FC\_CALLBACK constant indicates that an expression evaluation routine needs to be called.</span></span>

<span data-ttu-id="80cdd-140">Le champ décalage<2> correspond généralement à un décalage de mémoire relatif à la variable d’argument expression.</span><span class="sxs-lookup"><span data-stu-id="80cdd-140">The offset<2> field is typically a relative memory offset to the expression argument variable.</span></span> <span data-ttu-id="80cdd-141">Il peut également s’agir d’une évaluation d’expression – index de routine.</span><span class="sxs-lookup"><span data-stu-id="80cdd-141">It can also be an expression evaluation–routine index.</span></span> <span data-ttu-id="80cdd-142">Comme mentionné précédemment dans ce document, pour les expressions constantes, il fait partie de la valeur de l’expression finale réelle.</span><span class="sxs-lookup"><span data-stu-id="80cdd-142">As mentioned previously in this document, for constant expressions it is a part of actual, final expression value.</span></span>

<span data-ttu-id="80cdd-143">L’interprétation du champ offset<2> en tant que décalage de la mémoire dépend de la complexité de l’expression, de l’emplacement de la variable d’expression et, dans le cas d’un tableau, du fait que le tableau est effectivement un pointeur avec attributs.</span><span class="sxs-lookup"><span data-stu-id="80cdd-143">The interpretation of the offset<2> field as memory offset depends on the complexity of the expression, the location of the expression variable, and in the case of an array, whether the array is actually an attributed pointer.</span></span>

<span data-ttu-id="80cdd-144">Si le tableau est un pointeur avec attributs et que la variable de conformité est un champ dans une structure, le champ de décalage contient le décalage entre le début de la structure et le champ de description de la conformité.</span><span class="sxs-lookup"><span data-stu-id="80cdd-144">If the array is an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the beginning of the structure to the conformance-describing field.</span></span> <span data-ttu-id="80cdd-145">Si le tableau n’est pas un pointeur attribué et que la variable de conformité est un champ dans une structure, le champ de décalage contient le décalage entre la fin de la partie non conforme de la structure et le champ de description de la conformité.</span><span class="sxs-lookup"><span data-stu-id="80cdd-145">If the array is not an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the end of the nonconformant part of the structure to the conformance-describing field.</span></span> <span data-ttu-id="80cdd-146">En règle générale, le tableau conforme se trouve à la fin de la structure.</span><span class="sxs-lookup"><span data-stu-id="80cdd-146">Typically, the conformant array is at the end of the structure.</span></span>

<span data-ttu-id="80cdd-147">Pour la conformité de niveau supérieur, le champ de décalage contient le décalage à partir de l’emplacement du premier paramètre du stub sur la pile jusqu’au paramètre qui décrit la conformité.</span><span class="sxs-lookup"><span data-stu-id="80cdd-147">For top-level conformance, the offset field contains the offset from the stub's first parameter's location on the stack to the parameter that describes the conformance.</span></span> <span data-ttu-id="80cdd-148">Cela n’est pas utilisé en mode **– système d’exploitation** .</span><span class="sxs-lookup"><span data-stu-id="80cdd-148">This is not used in **–Os** mode.</span></span> <span data-ttu-id="80cdd-149">Il existe d’autres exceptions à l’interprétation du champ de décalage ; de telles exceptions sont décrites dans la description de ces types.</span><span class="sxs-lookup"><span data-stu-id="80cdd-149">There are other exceptions to the interpretation of the offset field; such exceptions are described in the description of those types.</span></span>

<span data-ttu-id="80cdd-150">Lorsque l’offset<2> est utilisé avec \_ le rappel FC, il contient un index dans la table de routine d’évaluation d’expression générée par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="80cdd-150">When offset<2> is used with FC\_CALLBACK, it contains an index in the expression evaluation routine table generated by the compiler.</span></span> <span data-ttu-id="80cdd-151">Le message stub est passé à la routine d’évaluation, qui calcule ensuite la valeur de conformité et l’assigne au champ MaxCount du message stub.</span><span class="sxs-lookup"><span data-stu-id="80cdd-151">The stub message is passed to the evaluation routine, which then computes the conformance value and assigns it to the MaxCount field of the stub message.</span></span>

<span data-ttu-id="80cdd-152">Le \_ champ indicateurs robustes<2> a été ajouté pour Windows 2000 afin de prendre en charge [**/Robust**](/windows/desktop/Midl/-robust), par exemple la fonctionnalité de refus d’attaques.</span><span class="sxs-lookup"><span data-stu-id="80cdd-152">The robust\_flags<2> field has been added for Windows 2000 to support [**/robust**](/windows/desktop/Midl/-robust), such as the denial-of-attacks feature.</span></span> <span data-ttu-id="80cdd-153">Les indicateurs suivants sont définis sur le premier octet :</span><span class="sxs-lookup"><span data-stu-id="80cdd-153">The following flags are defined on the first byte:</span></span>

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

<span data-ttu-id="80cdd-154">L’indicateur précoce indique une corrélation précoce et tardive.</span><span class="sxs-lookup"><span data-stu-id="80cdd-154">The Early flag indicates early versus late correlation.</span></span> <span data-ttu-id="80cdd-155">Une corrélation précoce est lorsque l’argument expression précède l’argument décrit, par exemple un argument de taille est avant un argument de pointeur de taille.</span><span class="sxs-lookup"><span data-stu-id="80cdd-155">An early correlation is when the expression argument precedes the described argument, for example a size argument is before a sized pointer argument.</span></span> <span data-ttu-id="80cdd-156">Une corrélation tardive est lorsque l’argument d’expression vient après l’argument associé.</span><span class="sxs-lookup"><span data-stu-id="80cdd-156">A late correlation is when the expression argument comes after the related argument.</span></span> <span data-ttu-id="80cdd-157">Le moteur effectue immédiatement la validation des valeurs de corrélation précoces, les valeurs de corrélation tardives sont stockées pour vérification une fois le démarshaling effectué.</span><span class="sxs-lookup"><span data-stu-id="80cdd-157">The engine performs validation of early correlation values right away, the late correlation values are stored for checking after unmarshaling is done.</span></span>

<span data-ttu-id="80cdd-158">L’indicateur Split indique un fractionnement asynchrone entre les \[ \] arguments in et \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="80cdd-158">The Split flag indicates an async split among \[in\] and \[out\] arguments.</span></span> <span data-ttu-id="80cdd-159">Par exemple, un argument de taille peut être \[ dans \] alors que le pointeur dimensionné peut être en \[ sortie \] .</span><span class="sxs-lookup"><span data-stu-id="80cdd-159">For example, a size argument may be \[in\] while the sized pointer may be \[out\].</span></span> <span data-ttu-id="80cdd-160">Dans le contexte asynchrone DCOM, ces arguments se trouvent sur des piles différentes ; le moteur doit donc en être conscient.</span><span class="sxs-lookup"><span data-stu-id="80cdd-160">In the DCOM async context, these arguments happen to be on different stacks, so the engine must be aware of this.</span></span>

<span data-ttu-id="80cdd-161">L’indicateur IsIidIs indique que la corrélation **IID \_ est ()** .</span><span class="sxs-lookup"><span data-stu-id="80cdd-161">The IsIidIs flag indicates an **iid\_is()** correlation.</span></span> <span data-ttu-id="80cdd-162">La routine NdrComputeConformance est confrontée à l’obtention d’un pointeur vers IID en tant que valeur d’expression, mais la routine de validation ne peut pas comparer ces valeurs (il s’agit de pointeurs) et l’indicateur indique donc que les IID réels doivent être comparés.</span><span class="sxs-lookup"><span data-stu-id="80cdd-162">The NdrComputeConformance routine is tricked to obtain a pointer to IID as an expression value, but the validation routine cannot compare such values (they would be pointers) and so the flag indicates that actual IIDs need to be compared.</span></span>

### <a name="variance-description-and-other-array-attributes"></a><span data-ttu-id="80cdd-163">Description de l’écart et autres attributs du tableau</span><span class="sxs-lookup"><span data-stu-id="80cdd-163">Variance Description and Other Array Attributes</span></span>

<span data-ttu-id="80cdd-164">Le format du champ Description de l’écart est identique au champ Description de la conformité.</span><span class="sxs-lookup"><span data-stu-id="80cdd-164">The variance description field format is identical to the conformance description field.</span></span> <span data-ttu-id="80cdd-165">La différence réside dans le fait qu’un autre champ de message stub est utilisé par le moteur de NDR comme une variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="80cdd-165">The difference is that a different stub message field is used by the NDR engine as a temporary variable.</span></span> <span data-ttu-id="80cdd-166">Dans le cas de la description de l’écart, il s’agit de la longueur qui est évaluée et le champ correspondant est appelé ActualLength.</span><span class="sxs-lookup"><span data-stu-id="80cdd-166">In the case of variance description, it is the length that is evaluated and the corresponding field is called ActualLength.</span></span>

<span data-ttu-id="80cdd-167">Avec la variance, le décalage de départ est généralement égal à zéro et le moteur est réglé en conséquence.</span><span class="sxs-lookup"><span data-stu-id="80cdd-167">With variance, the starting offset is typically zero and the engine is tuned accordingly.</span></span> <span data-ttu-id="80cdd-168">Si le **premier attribut \_ est ()** est appliqué à un tableau variable conforme, un rappel à une routine d’évaluation d’expression est forcé.</span><span class="sxs-lookup"><span data-stu-id="80cdd-168">If the **first\_is()** attribute is applied to a conformant varying array, a callback to an expression evaluation routine is forced.</span></span>

 

 