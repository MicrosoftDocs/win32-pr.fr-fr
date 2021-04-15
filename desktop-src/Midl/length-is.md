---
title: length_is (attribut)
description: L’attribut \ Length \_ est \ spécifie le nombre d’éléments de tableau à transmettre. Vous devez spécifier une valeur non négative.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463107"
---
# <a name="length_is-attribute"></a><span data-ttu-id="fd6a7-105">la longueur \_ est Attribute</span><span class="sxs-lookup"><span data-stu-id="fd6a7-105">length\_is attribute</span></span>

<span data-ttu-id="fd6a7-106">La **\[ longueur \_ est \]** attribute spécifie le nombre d’éléments de tableau à transmettre.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-106">The **\[length\_is\]** attribute specifies the number of array elements to be transmitted.</span></span> <span data-ttu-id="fd6a7-107">Vous devez spécifier une valeur non négative.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-107">You must specify a non-negative value.</span></span>

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="fd6a7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd6a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6a7-109">*Limited-expression-List*</span><span class="sxs-lookup"><span data-stu-id="fd6a7-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fd6a7-110">Spécifie une ou plusieurs expressions en langage C.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="fd6a7-111">Chaque expression prend la valeur d’un entier qui représente le nombre d’éléments de tableau à transmettre.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-111">Each expression evaluates to an integer that represents the number of array elements to be transmitted.</span></span> <span data-ttu-id="fd6a7-112">Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="fd6a7-113">MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="fd6a7-114">Séparez plusieurs expressions par des virgules.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd6a7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fd6a7-115">Remarks</span></span>

<span data-ttu-id="fd6a7-116">La **\[ longueur \_ est \]** un attribut qui détermine la valeur des index de tableau correspondant au **\[** [**\_**](last-is.md) **\]** **\[ \_ \]** dernier attribut is lorsque l’argument Last n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-116">The **\[length\_is\]** attribute determines the value of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** attribute when **\[last\_is\]** is not specified.</span></span> <span data-ttu-id="fd6a7-117">La relation entre ces index de tableau est la suivante : longueur = Last-First + 1.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="fd6a7-118">La **\[ longueur \_ est \]** l’attribut ne peut pas être utilisé en même temps que le **\[** [**dernier attribut \_ est**](last-is.md) **\]** ou l’attribut de **\[** [**chaîne**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fd6a7-118">The **\[length\_is\]** attribute cannot be used at the same time as the **\[**[**last\_is**](last-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="fd6a7-119">Pour définir une chaîne comptée avec une **\[ longueur égale \_ \]** à ou **\[** [**Last \_ est**](last-is.md) **\]** attribute, utilisez un tableau de caractères ou un pointeur sans l’attribut de **\[** [**chaîne**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fd6a7-119">To define a counted string with a **\[length\_is\]** or **\[**[**last\_is**](last-is.md)**\]** attribute, use a character array or pointer without the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="fd6a7-120">L’utilisation d’une expression constante avec la **\[ longueur \_ est \]** l’attribut est une utilisation inappropriée de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-120">Using a constant expression with the **\[length\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="fd6a7-121">Il est légal, mais inefficace, et se traduira par un code de marshaling plus lent.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="fd6a7-122">Vous pouvez utiliser la **\[** [**taille \_**](size-is.md) **\]** **\[ \_ et \]** les attributs en même temps.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-122">You can use the **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** attributes together.</span></span> <span data-ttu-id="fd6a7-123">Dans ce cas, la **\[ taille \_ est \]** l’attribut qui contrôle la quantité de mémoire allouée pour les données.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-123">When you do, the **\[size\_is\]** attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="fd6a7-124">La **\[ longueur \_ est \]** attribute spécifie le nombre d’éléments transmis.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-124">The **\[length\_is\]** attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="fd6a7-125">La quantité de mémoire spécifiée par la **\[ taille \_ est \]** et la **\[ longueur \_ est \]** que les attributs n’ont pas besoin d’être identiques.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-125">The amount of memory specified by the **\[size\_is\]** and **\[length\_is\]** attributes need not be the same.</span></span> <span data-ttu-id="fd6a7-126">Par exemple, votre client peut passer un paramètre **\[ in**, **out \]** à un serveur et spécifier une allocation de mémoire importante avec **\[ size \_ is \]**, bien qu’il spécifie un petit **\[ \_ \]** nombre d’éléments de données à passer avec length.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-126">For instance, your client may pass an **\[in**, **out\]** parameter to a server and specify a large memory allocation with **\[size\_is\]**, even though it specifies a small number of data elements to be passed with **\[length\_is\]**.</span></span> <span data-ttu-id="fd6a7-127">Cela permet au serveur de remplir le tableau avec plus de données qu’il n’en a reçu, qu’il peut ensuite renvoyer au client.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-127">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="fd6a7-128">En général, il n’est pas utile de spécifier à la fois la **\[** [**taille \_**](size-is.md) **\]** **\[ \_ \]** et les **\[** paramètres [**in**](in.md) **\]** ou **\[** [**out**](out-idl.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fd6a7-128">In general, it isn't useful to specify both **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** on **\[**[**in**](in.md)**\]** or **\[**[**out**](out-idl.md)**\]** parameters.</span></span> <span data-ttu-id="fd6a7-129">Dans les deux cas, la **\[ taille \_ est \]** le contrôle de l’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-129">In both cases, **\[size\_is\]** controls memory allocation.</span></span> <span data-ttu-id="fd6a7-130">Votre application peut utiliser la **\[ taille \_ \]** pour allouer plus d’éléments de tableau qu’elle ne le transmet (comme **\[ \_ \]** spécifié par Length).</span><span class="sxs-lookup"><span data-stu-id="fd6a7-130">Your application could use **\[size\_is\]** to allocate more array elements than it transmits (as specified by **\[length\_is\]**).</span></span> <span data-ttu-id="fd6a7-131">Toutefois, cela serait inefficace.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-131">However, this would be inefficient.</span></span> <span data-ttu-id="fd6a7-132">Il serait également inefficace de spécifier des valeurs identiques pour la **\[ taille \_ \]** , et la **\[ longueur \_ est \]**.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-132">It would also be inefficient to specify identical values for **\[size\_is\]** and **\[length\_is\]**.</span></span> <span data-ttu-id="fd6a7-133">Car cela entraînerait une surcharge supplémentaire pendant le marshaling des paramètres.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-133">Because it would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="fd6a7-134">Lorsque les valeurs de **\[ taille \_ \]** sont et que la **\[ longueur \_ est \]** toujours la même, omettez la **\[ longueur \_ est \]** attribut.</span><span class="sxs-lookup"><span data-stu-id="fd6a7-134">When the values of **\[size\_is\]** and **\[length\_is\]** are always the same, omit the **\[length\_is\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="fd6a7-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="fd6a7-135">Examples</span></span>

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a><span data-ttu-id="fd6a7-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd6a7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6a7-137">Attributs de champ</span><span class="sxs-lookup"><span data-stu-id="fd6a7-137">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="fd6a7-138">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="fd6a7-138">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="fd6a7-139">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="fd6a7-139">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="fd6a7-140">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="fd6a7-140">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="fd6a7-141">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="fd6a7-141">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="fd6a7-142">**min \_ est**</span><span class="sxs-lookup"><span data-stu-id="fd6a7-142">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="fd6a7-143">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="fd6a7-143">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="fd6a7-144">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd6a7-144">**string**</span></span>](string.md)
</dt> </dl>

 

 