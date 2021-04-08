---
title: Descripteurs de paramètre
description: Comme mentionné précédemment, les descripteurs de paramètre de style de type d’environnement de ligne de 8211, OI et \ 8211 ; existent.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729412"
---
# <a name="parameter-descriptors"></a><span data-ttu-id="13b59-103">Descripteurs de paramètre</span><span class="sxs-lookup"><span data-stu-id="13b59-103">Parameter Descriptors</span></span>

<span data-ttu-id="13b59-104">Comme nous l’avons vu précédemment, les descripteurs de paramètre de style [**-OI**](/windows/desktop/Midl/-oi) et **-** de type d’environnement de ligne de fonction existent.</span><span class="sxs-lookup"><span data-stu-id="13b59-104">As mentioned previously, [**–Oi**](/windows/desktop/Midl/-oi) and **–Oif** style parameter descriptors exist.</span></span>

## <a name="the-oi-parameter-descriptors"></a><span data-ttu-id="13b59-105">Descripteurs de paramètre – OI</span><span class="sxs-lookup"><span data-stu-id="13b59-105">The –Oi Parameter Descriptors</span></span>

<span data-ttu-id="13b59-106">Les stubs entièrement interprétés requièrent des informations supplémentaires pour chacun des paramètres d’un appel RPC.</span><span class="sxs-lookup"><span data-stu-id="13b59-106">Fully interpreted stubs require additional information for each of the parameters in an RPC call.</span></span> <span data-ttu-id="13b59-107">Les descriptions de paramètres d’une procédure suivent immédiatement la description de la procédure.</span><span class="sxs-lookup"><span data-stu-id="13b59-107">The parameter descriptions of a procedure follow immediately after the description of the procedure.</span></span>

[<span data-ttu-id="13b59-108">**Simple – OI**</span><span class="sxs-lookup"><span data-stu-id="13b59-108">**Simple –Oi**</span></span>](/windows/desktop/Midl/-oi)

<span data-ttu-id="13b59-109">**Descripteurs de paramètre**</span><span class="sxs-lookup"><span data-stu-id="13b59-109">**Parameter Descriptors**</span></span>

<span data-ttu-id="13b59-110">Le format de la description d’un \[  \] paramètre de type simple dans ou retourne est :</span><span class="sxs-lookup"><span data-stu-id="13b59-110">The format for the description of an \[**in**\] or return simple type parameter is:</span></span>

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="13b59-111">–ou–</span><span class="sxs-lookup"><span data-stu-id="13b59-111">–or–</span></span>

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="13b59-112">Où le \_ type simple<1> est le jeton FC indiquant le type simple.</span><span class="sxs-lookup"><span data-stu-id="13b59-112">Where simple\_type<1> is the FC token indicating the simple type.</span></span> <span data-ttu-id="13b59-113">Les codes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="13b59-113">The codes are as follows:</span></span>

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

<span data-ttu-id="13b59-114">**Autre – OI**</span><span class="sxs-lookup"><span data-stu-id="13b59-114">**Other –Oi**</span></span>

<span data-ttu-id="13b59-115">**Descripteurs de paramètre**</span><span class="sxs-lookup"><span data-stu-id="13b59-115">**Parameter Descriptors**</span></span>

<span data-ttu-id="13b59-116">Le format de la description de tous les autres types de paramètres est le suivant :</span><span class="sxs-lookup"><span data-stu-id="13b59-116">The format for the description for all other parameter types is:</span></span>

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

<span data-ttu-id="13b59-117">Où la \_ direction param<1> champ pour chacune de ces descriptions doit être l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="13b59-117">Where the param\_direction<1> field for each of these descriptions must be one of those shown in the following table.</span></span>



| <span data-ttu-id="13b59-118">Hex</span><span class="sxs-lookup"><span data-stu-id="13b59-118">Hex</span></span> | <span data-ttu-id="13b59-119">Indicateur</span><span class="sxs-lookup"><span data-stu-id="13b59-119">Flag</span></span>                          | <span data-ttu-id="13b59-120">Signification</span><span class="sxs-lookup"><span data-stu-id="13b59-120">Meaning</span></span>                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="13b59-121">4d</span><span class="sxs-lookup"><span data-stu-id="13b59-121">4d</span></span>  | <span data-ttu-id="13b59-122">FC \_ dans \_ param</span><span class="sxs-lookup"><span data-stu-id="13b59-122">FC\_IN\_PARAM</span></span>                 | <span data-ttu-id="13b59-123">Paramètre in.</span><span class="sxs-lookup"><span data-stu-id="13b59-123">An in parameter.</span></span>                                            |
| <span data-ttu-id="13b59-124">50</span><span class="sxs-lookup"><span data-stu-id="13b59-124">50</span></span>  | <span data-ttu-id="13b59-125">Param. FC \_ en \_ sortie \_</span><span class="sxs-lookup"><span data-stu-id="13b59-125">FC\_IN\_OUT\_PARAM</span></span>            | <span data-ttu-id="13b59-126">Paramètre in/out.</span><span class="sxs-lookup"><span data-stu-id="13b59-126">An in/out parameter.</span></span>                                        |
| <span data-ttu-id="13b59-127">51</span><span class="sxs-lookup"><span data-stu-id="13b59-127">51</span></span>  | <span data-ttu-id="13b59-128">\_paramètre de sortie FC \_</span><span class="sxs-lookup"><span data-stu-id="13b59-128">FC\_OUT\_PARAM</span></span>                | <span data-ttu-id="13b59-129">Paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="13b59-129">An out parameter.</span></span>                                           |
| <span data-ttu-id="13b59-130">52</span><span class="sxs-lookup"><span data-stu-id="13b59-130">52</span></span>  | <span data-ttu-id="13b59-131">\_param de retour FC \_</span><span class="sxs-lookup"><span data-stu-id="13b59-131">FC\_RETURN\_PARAM</span></span>             | <span data-ttu-id="13b59-132">Valeur de retour de procédure.</span><span class="sxs-lookup"><span data-stu-id="13b59-132">A procedure return value.</span></span>                                   |
| <span data-ttu-id="13b59-133">4F</span><span class="sxs-lookup"><span data-stu-id="13b59-133">4f</span></span>  | <span data-ttu-id="13b59-134">FC \_ dans \_ param \_ pas \_ d' \_ inst gratuit</span><span class="sxs-lookup"><span data-stu-id="13b59-134">FC\_IN\_PARAM\_NO\_FREE\_INST</span></span> | <span data-ttu-id="13b59-135">Dans le port de transmission/REP en tant que paramètre pour lequel aucune libération n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="13b59-135">An in xmit/rep as a parameter for which no freeing is made.</span></span> |



 

<span data-ttu-id="13b59-136">La \_ taille de la pile<1> correspond à la taille du paramètre sur la pile, exprimée sous la forme du nombre d’entiers que le paramètre occupe sur la pile.</span><span class="sxs-lookup"><span data-stu-id="13b59-136">The stack\_size<1> is the size of the parameter on the stack, expressed as the number of integers the parameter occupies on the stack.</span></span>

> [!Note]  
> <span data-ttu-id="13b59-137">Le mode [**– OI**](/windows/desktop/Midl/-oi) n’est pas pris en charge sur les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="13b59-137">The [**–Oi**](/windows/desktop/Midl/-oi) mode is not supported on 64-bit platforms.</span></span>

 

<span data-ttu-id="13b59-138">Le \_ champ décalage de type<2> est l’offset dans le type table de chaînes de format, indiquant le descripteur de type pour l’argument.</span><span class="sxs-lookup"><span data-stu-id="13b59-138">The type\_offset<2> field is the offset in the type format string table, indicating the type descriptor for the argument.</span></span>

## <a name="the-oif-parameter-descriptors"></a><span data-ttu-id="13b59-139">Descripteurs de paramètre – de l’environnement d’exécution</span><span class="sxs-lookup"><span data-stu-id="13b59-139">The –Oif Parameter Descriptors</span></span>

<span data-ttu-id="13b59-140">Il existe deux formats possibles pour une description de paramètre, un pour les types de base, un autre pour tous les autres types.</span><span class="sxs-lookup"><span data-stu-id="13b59-140">There are two possible formats for a parameter description, one for base types, another for all other types.</span></span>

<span data-ttu-id="13b59-141">Types de base :</span><span class="sxs-lookup"><span data-stu-id="13b59-141">Base types:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

<span data-ttu-id="13b59-142">Autres :</span><span class="sxs-lookup"><span data-stu-id="13b59-142">Other:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

<span data-ttu-id="13b59-143">Dans les deux \_ décalages de pile<2> indique le décalage sur la pile d’arguments virtuels, en octets.</span><span class="sxs-lookup"><span data-stu-id="13b59-143">In both stack\_offset<2> indicates the offset on the virtual argument stack, in bytes.</span></span> <span data-ttu-id="13b59-144">Pour les types de base, le type d’argument est fourni directement par le caractère de format correspondant au type.</span><span class="sxs-lookup"><span data-stu-id="13b59-144">For base types, the argument type is given directly by the format character corresponding to the type.</span></span> <span data-ttu-id="13b59-145">Pour les autres types, le \_ champ décalage de type<2> indique le décalage au sein de la table de chaînes de format de type où se trouve le descripteur de type de l’argument.</span><span class="sxs-lookup"><span data-stu-id="13b59-145">For other types, the type\_offset<2> field gives the offset in the type format string table where the type descriptor for the argument is located.</span></span>

<span data-ttu-id="13b59-146">Le champ attribut de paramètre est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="13b59-146">The parameter attribute field is defined as follows:</span></span>

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   <span data-ttu-id="13b59-147">Le bit **MustSize** est défini uniquement si le paramètre doit être dimensionné.</span><span class="sxs-lookup"><span data-stu-id="13b59-147">The **MustSize** bit is set only if the parameter must be sized.</span></span>
-   <span data-ttu-id="13b59-148">Le bit **MustFree** est défini si le serveur doit appeler la routine NdrFree du paramètre \* .</span><span class="sxs-lookup"><span data-stu-id="13b59-148">The **MustFree** bit is set if the server must call the parameter's NdrFree\* routine.</span></span>
-   <span data-ttu-id="13b59-149">Le bit **IsSimpleRef** est défini pour un paramètre qui est un pointeur de référence vers tout autre pointeur, et qui n’a pas d’attribut d’allocation.</span><span class="sxs-lookup"><span data-stu-id="13b59-149">The **IsSimpleRef** bit is set for a parameter that is a reference pointer to anything other than another pointer, and which has no allocate attributes.</span></span> <span data-ttu-id="13b59-150">Pour un tel type, l’offset de type de la description du paramètre \_<> champ, à l’exception d’un pointeur de référence vers un type de base, fournit l’offset au type du référent ; le pointeur de référence est simplement ignoré.</span><span class="sxs-lookup"><span data-stu-id="13b59-150">For such a type, the parameter description's type\_offset<> field, except for a reference pointer to a base type, provides the offset to the referent's type; the reference pointer is simply skipped.</span></span>
-   <span data-ttu-id="13b59-151">Le bit **IsDontCallFreeInst** est défini pour certains \_ paramètres, dont les routines d’instance gratuite ne doivent pas être appelées.</span><span class="sxs-lookup"><span data-stu-id="13b59-151">The **IsDontCallFreeInst** bit is set for certain represent\_as parameters whose free instance routines should not be called.</span></span>
-   <span data-ttu-id="13b59-152">Les bits **ServerAllocSize** sont non nuls si le paramètre a la valeur \[ **out** \] , \[ **in** \] , ou \[ **in, out** pointeur \] vers le pointeur, ou pointeur vers enum16, et seront initialisés sur la pile de l’interpréteur de serveur, au lieu d’utiliser un appel à **I \_ RpcAllocate**.</span><span class="sxs-lookup"><span data-stu-id="13b59-152">The **ServerAllocSize** bits are nonzero if the parameter is \[**out**\], \[**in**\], or \[**in,out**\] pointer to pointer, or pointer to enum16, and will be initialized on the server interpreter's stack, rather than using a call to **I\_RpcAllocate**.</span></span> <span data-ttu-id="13b59-153">Si la valeur est différente de zéro, cette valeur est multipliée par 8 pour obtenir le nombre d’octets pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="13b59-153">If nonzero, this value is multiplied by 8 to get the number of bytes for the parameter.</span></span> <span data-ttu-id="13b59-154">Notez que cela signifie qu’au moins 8 octets sont toujours alloués pour un pointeur.</span><span class="sxs-lookup"><span data-stu-id="13b59-154">Note that doing so means at least 8 bytes are always allocated for a pointer.</span></span>
-   <span data-ttu-id="13b59-155">Le bit **IsBasetype** est défini pour les types simples qui sont marshalés par la boucle de l’interpréteur main [**-**](/windows/desktop/Midl/-oi) out.</span><span class="sxs-lookup"><span data-stu-id="13b59-155">The **IsBasetype** bit is set for simple types that are being marshaled by the main [**–Oif**](/windows/desktop/Midl/-oi) interpreter loop.</span></span> <span data-ttu-id="13b59-156">En particulier, un type simple avec un attribut de plage sur celui-ci n’est pas marqué comme type de base afin de forcer le marshaling de routines de la routine de plage via la distribution à l’aide d’un \_ jeton de plage FC.</span><span class="sxs-lookup"><span data-stu-id="13b59-156">In particular, a simple type with a range attribute on it is not flagged as a base type in order to force the range routine marshaling through dispatching using an FC\_RANGE token.</span></span>
-   <span data-ttu-id="13b59-157">Le bit **IsByValue** est défini pour les types composés qui sont envoyés par valeur, mais n’est pas défini pour les types simples, que l’argument soit ou non un pointeur.</span><span class="sxs-lookup"><span data-stu-id="13b59-157">The **IsByValue** bit is set for compound types being sent by value, but is not set for simple types, regardless of whether the argument is a pointer.</span></span> <span data-ttu-id="13b59-158">Les types composés pour lesquels il est défini sont les structures, les unions, [**les transmissions \_ en tant que**](/windows/desktop/Midl/transmit-as) [**, le \_**](/windows/desktop/Midl/represent-as) [**\_ marshaleur de câble**](/windows/desktop/Midl/wire-marshal) et SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="13b59-158">The compound types for which it is set are structures, unions, [**transmit\_as**](/windows/desktop/Midl/transmit-as), [**represent\_as**](/windows/desktop/Midl/represent-as), [**wire\_marshal**](/windows/desktop/Midl/wire-marshal) and SAFEARRAY.</span></span> <span data-ttu-id="13b59-159">En général, le bit a été introduit pour l’avantage de la boucle de l’interpréteur principale dans l’interpréteur [**– Oicf**](/windows/desktop/Midl/-oi) , pour s’assurer que les arguments non simples (appelés arguments de type composé) sont correctement déréférencés.</span><span class="sxs-lookup"><span data-stu-id="13b59-159">In general, the bit was introduced for the benefit of the main interpreter loop in the [**–Oicf**](/windows/desktop/Midl/-oi) interpreter, to ensure the nonsimple arguments (referred to as compound type arguments) are properly dereferenced.</span></span> <span data-ttu-id="13b59-160">Ce bit n’a jamais été utilisé dans les versions précédentes de l’interpréteur.</span><span class="sxs-lookup"><span data-stu-id="13b59-160">This bit was never used in previous versions of the interpreter.</span></span>

 

 