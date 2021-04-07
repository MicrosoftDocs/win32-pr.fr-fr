---
title: size_is (attribut)
description: Utilisez l’attribut \ size \_ is \ pour spécifier la taille de la mémoire, en éléments, allouée aux pointeurs dimensionnés, aux pointeurs dimensionnés aux pointeurs dimensionnés et aux tableaux à une ou plusieurs dimensions.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724948"
---
# <a name="size_is-attribute"></a><span data-ttu-id="4505d-104">la taille \_ est un attribut</span><span class="sxs-lookup"><span data-stu-id="4505d-104">size\_is attribute</span></span>

<span data-ttu-id="4505d-105">Utilisez l' \[ **attribut \_ Size** \] pour spécifier la taille de la mémoire, en éléments, allouée aux pointeurs dimensionnés, aux pointeurs dimensionnés aux pointeurs dimensionnés et aux tableaux à une ou plusieurs dimensions.</span><span class="sxs-lookup"><span data-stu-id="4505d-105">Use the \[**size\_is**\] attribute to specify the size of memory, in elements, allocated for sized pointers, sized pointers to sized pointers, and single- or multidimensional arrays.</span></span>

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a><span data-ttu-id="4505d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4505d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4505d-107">*Limited-expression-List*</span><span class="sxs-lookup"><span data-stu-id="4505d-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4505d-108">Spécifie une ou plusieurs expressions en langage C.</span><span class="sxs-lookup"><span data-stu-id="4505d-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="4505d-109">Chaque expression prend la valeur d’un entier non négatif qui représente la quantité de mémoire allouée à un pointeur dimensionné ou à un tableau.</span><span class="sxs-lookup"><span data-stu-id="4505d-109">Each expression evaluates to a non-negative integer that represents the amount of memory allocated to a sized pointer or an array.</span></span> <span data-ttu-id="4505d-110">Dans le cas d’un tableau, spécifie une expression unique qui représente la taille d’allocation, en éléments, de la première dimension de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="4505d-110">In the case of an array, specifies a single expression that represents the allocation size, in elements, of the first dimension of that array.</span></span> <span data-ttu-id="4505d-111">Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="4505d-111">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="4505d-112">MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation.</span><span class="sxs-lookup"><span data-stu-id="4505d-112">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="4505d-113">Utilisez des virgules comme espaces réservés pour les paramètres implicites ou pour séparer plusieurs expressions.</span><span class="sxs-lookup"><span data-stu-id="4505d-113">Use commas as placeholders for implicit parameters, or to separate multiple expressions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4505d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4505d-114">Remarks</span></span>

<span data-ttu-id="4505d-115">Si vous utilisez l’attribut \[ **size \_ is** \] pour allouer de la mémoire pour un tableau multidimensionnel et que vous utilisez la notation de tableau \[ \] , gardez à l’esprit que seule la première dimension d’un tableau multidimensionnel peut être déterminée dynamiquement au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4505d-115">If you are using the \[**size\_is**\] attribute to allocate memory for a multidimensional array and you are using array \[ \] notation, keep in mind that only the first dimension of a multidimensional array can be dynamically determined at run time.</span></span> <span data-ttu-id="4505d-116">Les autres dimensions doivent être spécifiées de manière statique.</span><span class="sxs-lookup"><span data-stu-id="4505d-116">The other dimensions must be statically specified.</span></span> <span data-ttu-id="4505d-117">Pour plus d’informations sur l’utilisation de l' \[ attribut **size \_** \] avec plusieurs niveaux de pointeurs pour permettre à un serveur de retourner un tableau de données de taille dynamique à un client, comme illustré dans l’exemple Proc7, consultez [plusieurs niveaux de pointeurs](/windows/desktop/Rpc/multiple-levels-of-pointers).</span><span class="sxs-lookup"><span data-stu-id="4505d-117">For more information on using the \[**size\_is**\] attribute with multiple levels of pointers to enable a server to return a dynamically-sized array of data to a client, as shown in the example Proc7, see [Multiple Levels of Pointers](/windows/desktop/Rpc/multiple-levels-of-pointers).</span></span>

<span data-ttu-id="4505d-118">Vous pouvez utiliser l’une ou l’autre \[ **taille \_** est \] ou [**Max \_ est**](max-is.md) (mais pas les deux dans la même liste d’attributs) pour spécifier la taille d’un tableau dont les limites supérieures sont déterminées au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4505d-118">You can use either \[**size\_is**\] or [**max\_is**](max-is.md) (but not both in the same attribute list) to specify the size of an array whose upper bounds are determined at run time.</span></span> <span data-ttu-id="4505d-119">Notez, toutefois, que l' \[ attribut **size \_ is** \] ne peut pas être utilisé sur des dimensions de tableau fixes.</span><span class="sxs-lookup"><span data-stu-id="4505d-119">Note, however, that the \[**size\_is**\] attribute cannot be used on array dimensions that are fixed.</span></span> <span data-ttu-id="4505d-120">L' \[ attribut **Max \_ is** \] spécifie l’index de tableau valide maximal.</span><span class="sxs-lookup"><span data-stu-id="4505d-120">The \[**max\_is**\] attribute specifies the maximum valid array index.</span></span> <span data-ttu-id="4505d-121">Par conséquent, la spécification de \[ Size a la valeur \_ (n) \] équivaut à spécifier \[ Max \_ is (n-1) \] .</span><span class="sxs-lookup"><span data-stu-id="4505d-121">As a result, specifying \[size\_is(n)\] is equivalent to specifying \[max\_is(n-1)\].</span></span>

<span data-ttu-id="4505d-122">Un \[ paramètre de tableau conforme [**dans**](in.md) \] ou \[ dans, [**out**](out-idl.md) \] avec l’attribut de \[ [**chaîne**](string.md) n' \] a pas besoin de l' \[ attribut **size \_ is** \] ou \[ [**Max \_ is**](max-is.md) \] .</span><span class="sxs-lookup"><span data-stu-id="4505d-122">An \[ [**in**](in.md)\] or \[in, [**out**](out-idl.md)\] conformant-array parameter with the \[ [**string**](string.md)\] attribute need not have the \[**size\_is**\] or \[[**max\_is**](max-is.md)\] attribute.</span></span> <span data-ttu-id="4505d-123">Dans ce cas, la taille de l’allocation est déterminée à partir de la marque de fin NULL de la chaîne d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4505d-123">In this case, the size of the allocation is determined from the NULL terminator of the input string.</span></span> <span data-ttu-id="4505d-124">Tous les autres tableaux conformes avec l’attribut de \[ chaîne \] doivent avoir une \[ **taille \_** \] ou un attribut \[ **Max \_ est** un \] attribut.</span><span class="sxs-lookup"><span data-stu-id="4505d-124">All other conformant arrays with the \[string\] attribute must have a \[**size\_is**\] or \[**max\_is**\] attribute.</span></span>

<span data-ttu-id="4505d-125">Bien qu’il soit possible d’utiliser l' \[ attribut **\_ Size** \] avec une constante, cette opération est inefficace et inutile.</span><span class="sxs-lookup"><span data-stu-id="4505d-125">While it is legal to use the \[**size\_is**\] attribute with a constant, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="4505d-126">Par exemple, utilisez un tableau de taille fixe :</span><span class="sxs-lookup"><span data-stu-id="4505d-126">For example, use a fixed size array:</span></span>

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

<span data-ttu-id="4505d-127">plutôt que :</span><span class="sxs-lookup"><span data-stu-id="4505d-127">instead of:</span></span>

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

<span data-ttu-id="4505d-128">Vous pouvez utiliser la \[ **taille \_** \] et les \[ [**\_**](length-is.md) \] attributs en même temps.</span><span class="sxs-lookup"><span data-stu-id="4505d-128">You can use the \[**size\_is**\] and \[[**length\_is**](length-is.md)\] attributes together.</span></span> <span data-ttu-id="4505d-129">Dans ce cas, la \[ **taille \_ est** l' \] attribut qui contrôle la quantité de mémoire allouée pour les données.</span><span class="sxs-lookup"><span data-stu-id="4505d-129">When you do, the \[**size\_is**\] attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="4505d-130">La \[ **longueur \_ est** \] attribute spécifie le nombre d’éléments transmis.</span><span class="sxs-lookup"><span data-stu-id="4505d-130">The \[**length\_is**\] attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="4505d-131">La quantité de mémoire spécifiée par la \[ **taille \_ est** \] et la \[ **longueur \_ est** que \] les attributs n’ont pas besoin d’être identiques.</span><span class="sxs-lookup"><span data-stu-id="4505d-131">The amount of memory specified by the \[**size\_is**\] and \[**length\_is**\] attributes need not be the same.</span></span> <span data-ttu-id="4505d-132">Par exemple, votre client peut passer un \[ paramètre in, out \] à un serveur et spécifier une allocation de mémoire importante avec \[ **size \_ is**, bien qu' \] il spécifie un petit nombre d’éléments de données à passer avec \[ **Length \_** \] .</span><span class="sxs-lookup"><span data-stu-id="4505d-132">For instance, your client may pass an \[in,out\] parameter to a server and specify a large memory allocation with \[**size\_is**\], even though it specifies a small number of data elements to be passed with \[**length\_is**\].</span></span> <span data-ttu-id="4505d-133">Cela permet au serveur de remplir le tableau avec plus de données qu’il n’en a reçu, qu’il peut ensuite renvoyer au client.</span><span class="sxs-lookup"><span data-stu-id="4505d-133">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="4505d-134">En général, il n’est pas utile de spécifier à la fois la \[ **taille \_** \] et les \[ [**\_**](length-is.md) \] \[ \] paramètres in ou \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="4505d-134">In general, it isn't useful to specify both \[**size\_is**\] and \[[**length\_is**](length-is.md)\] on \[in\] or \[out\] parameters.</span></span> <span data-ttu-id="4505d-135">Dans les deux cas, la \[ **taille \_ est** le contrôle de l' \] allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="4505d-135">In both cases, \[**size\_is**\] controls memory allocation.</span></span> <span data-ttu-id="4505d-136">Votre application peut utiliser la \[ **taille \_** \] pour allouer plus d’éléments de tableau qu’elle ne le transmet (comme spécifié par \[ **Length \_** \] ).</span><span class="sxs-lookup"><span data-stu-id="4505d-136">Your application could use \[**size\_is**\] to allocate more array elements than it transmits (as specified by \[**length\_is**\]).</span></span> <span data-ttu-id="4505d-137">Toutefois, cela serait inefficace.</span><span class="sxs-lookup"><span data-stu-id="4505d-137">However, this would be inefficient.</span></span> <span data-ttu-id="4505d-138">Il serait également inefficace de spécifier des valeurs identiques pour la \[ **taille \_** \] , et la \[ **longueur \_ est** \] .</span><span class="sxs-lookup"><span data-stu-id="4505d-138">It would also be inefficient to specify identical values for \[**size\_is**\] and \[**length\_is**\].</span></span> <span data-ttu-id="4505d-139">Cela créerait une surcharge supplémentaire pendant le marshaling de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4505d-139">It would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="4505d-140">Si les valeurs de \[ **size \_ is** \] et \[ **Length \_** \] sont toujours les mêmes, omettez la \[ **longueur \_ est** \] attribute.</span><span class="sxs-lookup"><span data-stu-id="4505d-140">If the values of \[**size\_is**\] and \[**length\_is**\] are always the same, omit the \[**length\_is**\] attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="4505d-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="4505d-141">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a><span data-ttu-id="4505d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4505d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4505d-143">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="4505d-143">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="4505d-144">Attributs de champ</span><span class="sxs-lookup"><span data-stu-id="4505d-144">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="4505d-145">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="4505d-145">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="4505d-146">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="4505d-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4505d-147">**in**</span><span class="sxs-lookup"><span data-stu-id="4505d-147">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="4505d-148">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="4505d-148">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="4505d-149">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="4505d-149">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="4505d-150">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="4505d-150">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="4505d-151">**min \_ est**</span><span class="sxs-lookup"><span data-stu-id="4505d-151">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="4505d-152">**à**</span><span class="sxs-lookup"><span data-stu-id="4505d-152">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="4505d-153">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="4505d-153">**string**</span></span>](string.md)
</dt> </dl>

 

 