---
title: last_is (attribut)
description: L’attribut de champ \ Last \_ is \ spécifie l’index du dernier élément de tableau à transmettre. Lorsque l’index spécifié est égal à zéro ou négatif, aucun élément de tableau n’est transmis.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- last_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507906"
---
# <a name="last_is-attribute"></a><span data-ttu-id="8b758-105">le dernier \_ attribut est</span><span class="sxs-lookup"><span data-stu-id="8b758-105">last\_is attribute</span></span>

<span data-ttu-id="8b758-106">L’attribut Field **\[ Last \_ \]** spécifie l’index du dernier élément de tableau à transmettre.</span><span class="sxs-lookup"><span data-stu-id="8b758-106">The field attribute **\[last\_is\]** specifies the index of the last array element to be transmitted.</span></span> <span data-ttu-id="8b758-107">Lorsque l’index spécifié est égal à zéro ou négatif, aucun élément de tableau n’est transmis.</span><span class="sxs-lookup"><span data-stu-id="8b758-107">When the specified index is zero or negative, no array elements are transmitted.</span></span>

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="8b758-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b758-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b758-109">*Limited-expression-List*</span><span class="sxs-lookup"><span data-stu-id="8b758-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8b758-110">Spécifie une ou plusieurs expressions en langage C.</span><span class="sxs-lookup"><span data-stu-id="8b758-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="8b758-111">Chaque expression prend la valeur d’un entier qui représente l’index de tableau du dernier élément de tableau à transmettre.</span><span class="sxs-lookup"><span data-stu-id="8b758-111">Each expression evaluates to an integer that represents the array index of the last array element to be transmitted.</span></span> <span data-ttu-id="8b758-112">Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="8b758-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="8b758-113">MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation.</span><span class="sxs-lookup"><span data-stu-id="8b758-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="8b758-114">Séparez plusieurs expressions par des virgules.</span><span class="sxs-lookup"><span data-stu-id="8b758-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b758-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8b758-115">Remarks</span></span>

<span data-ttu-id="8b758-116">Le **\[ dernier \_ attribut \] est** détermine que la valeur de l’index de tableau correspondant à la **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** longueur est attribut lorsque la longueur n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8b758-116">The **\[last\_is\]** attribute determines the value of the array index corresponding to the **\[**[**length\_is**](length-is.md)**\]** attribute when **\[length\_is\]** is not specified.</span></span> <span data-ttu-id="8b758-117">La relation entre ces index de tableau est la suivante : longueur = Last-First + 1.</span><span class="sxs-lookup"><span data-stu-id="8b758-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="8b758-118">Si la valeur de l’index de tableau spécifié par la **\[** [**première \_ est**](first-is.md) supérieure **\]** à la valeur spécifiée par le **\[ dernier \_ \] est**, aucun élément n’est transmis.</span><span class="sxs-lookup"><span data-stu-id="8b758-118">If the value of the array index specified by **\[**[**first\_is**](first-is.md)**\]** is larger than the value specified by **\[last\_is\]**, zero elements are transmitted.</span></span>

<span data-ttu-id="8b758-119">Le **\[ dernier \_ attribut \] is** ne peut pas être utilisé en tant qu’attribut de champ en même temps que la **\[** [**longueur \_ est**](length-is.md) **\]** attribute ou l’attribut de **\[** [**chaîne**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="8b758-119">The **\[last\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**length\_is**](length-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="8b758-120">L’utilisation d’une expression constante avec le **\[ dernier attribut \_ est \]** une utilisation inappropriée de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="8b758-120">Using a constant expression with the **\[last\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="8b758-121">Il est légal, mais inefficace, et se traduira par un code de marshaling plus lent.</span><span class="sxs-lookup"><span data-stu-id="8b758-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="8b758-122">Quand la valeur spécifiée par **\[** [**Max \_ est**](max-is.md) **\]** supérieure ou égale à zéro, la relation suivante doit être vraie : 0 <= Last \_ est <= Max \_ est.</span><span class="sxs-lookup"><span data-stu-id="8b758-122">When the value specified by **\[**[**max\_is**](max-is.md)**\]** is equal to or greater than zero, the following relationship must be true: 0 <= last\_is <= max\_is.</span></span>

## <a name="examples"></a><span data-ttu-id="8b758-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="8b758-123">Examples</span></span>

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a><span data-ttu-id="8b758-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b758-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b758-125">Attributs de champ</span><span class="sxs-lookup"><span data-stu-id="8b758-125">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="8b758-126">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="8b758-126">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="8b758-127">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="8b758-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="8b758-128">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="8b758-128">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="8b758-129">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="8b758-129">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="8b758-130">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="8b758-130">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 