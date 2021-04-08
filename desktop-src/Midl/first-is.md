---
title: first_is (attribut)
description: L’attribut \ First \_ is \ spécifie l’index du premier élément de tableau à transmettre.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842290"
---
# <a name="first_is-attribute"></a><span data-ttu-id="33cdc-104">First \_ est l’attribut</span><span class="sxs-lookup"><span data-stu-id="33cdc-104">first\_is attribute</span></span>

<span data-ttu-id="33cdc-105">Le \[ **premier attribut \_ est** \] spécifie l’index du premier élément de tableau à transmettre.</span><span class="sxs-lookup"><span data-stu-id="33cdc-105">The \[**first\_is**\] attribute specifies the index of the first array element to be transmitted.</span></span>

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a><span data-ttu-id="33cdc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33cdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33cdc-107">*Limited-expression-List*</span><span class="sxs-lookup"><span data-stu-id="33cdc-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="33cdc-108">Spécifie une ou plusieurs expressions en langage C.</span><span class="sxs-lookup"><span data-stu-id="33cdc-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="33cdc-109">Chaque expression prend la valeur d’un entier qui représente l’index de tableau du premier élément de tableau à transmettre.</span><span class="sxs-lookup"><span data-stu-id="33cdc-109">Each expression evaluates to an integer that represents the array index of the first array element to be transmitted.</span></span> <span data-ttu-id="33cdc-110">Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="33cdc-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="33cdc-111">MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation.</span><span class="sxs-lookup"><span data-stu-id="33cdc-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="33cdc-112">Séparez plusieurs expressions par des virgules.</span><span class="sxs-lookup"><span data-stu-id="33cdc-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33cdc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="33cdc-113">Remarks</span></span>

<span data-ttu-id="33cdc-114">Si le **\[ premier \_ est \]** un attribut n’est pas présent, ou si l’index spécifié est un nombre négatif, l’élément de tableau zéro est le premier élément transmis.</span><span class="sxs-lookup"><span data-stu-id="33cdc-114">If the **\[first\_is\]** attribute is not present, or if the specified index is a negative number, array element zero is the first element transmitted.</span></span>

<span data-ttu-id="33cdc-115">La **\[ première \_ est \]** l’attribut peut également aider à déterminer les valeurs des index de tableau correspondant au **\[** [**dernier \_ is**](last-is.md) **\]** ou **\[** [**Length \_ est**](length-is.md) **\]** attribute quand ces attributs ne sont pas spécifiés.</span><span class="sxs-lookup"><span data-stu-id="33cdc-115">The **\[first\_is\]** attribute can also help determine the values of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** or **\[**[**length\_is**](length-is.md)**\]** attribute when these attributes are not specified.</span></span> <span data-ttu-id="33cdc-116">La relation entre ces index de tableau est la suivante :</span><span class="sxs-lookup"><span data-stu-id="33cdc-116">The relationship between these array indexes is:</span></span>

``` syntax
length = last - first + 1
```

<span data-ttu-id="33cdc-117">La relation suivante doit également contenir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="33cdc-117">The following relationship must also hold:</span></span>

``` syntax
0 <= first_is <= max_is
```

<span data-ttu-id="33cdc-118">La relation suivante doit contenir lorsque **\[** [**Max \_ est**](max-is.md) **\] <= 0 :**</span><span class="sxs-lookup"><span data-stu-id="33cdc-118">The following relationship must hold when **\[**[**max\_is**](max-is.md)**\] <= 0:**</span></span>

``` syntax
first_is == 0
```

<span data-ttu-id="33cdc-119">La **\[ première \_ est \]** l’attribut ne peut pas être utilisé en même temps que l’attribut de **\[** [**chaîne**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="33cdc-119">The **\[first\_is\]** attribute cannot be used at the same time as the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="33cdc-120">L’utilisation d’une expression constante avec la **\[ première \_ est \]** l’attribut est une utilisation inappropriée de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="33cdc-120">Using a constant expression with the **\[first\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="33cdc-121">Il est légal, mais inefficace, et se traduira par un code de marshaling plus lent.</span><span class="sxs-lookup"><span data-stu-id="33cdc-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

## <a name="examples"></a><span data-ttu-id="33cdc-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="33cdc-122">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a><span data-ttu-id="33cdc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33cdc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33cdc-124">attributs de champ \_</span><span class="sxs-lookup"><span data-stu-id="33cdc-124">field\_attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="33cdc-125">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="33cdc-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="33cdc-126">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="33cdc-126">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="33cdc-127">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="33cdc-127">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="33cdc-128">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="33cdc-128">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="33cdc-129">**min \_ est**</span><span class="sxs-lookup"><span data-stu-id="33cdc-129">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="33cdc-130">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="33cdc-130">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="33cdc-131">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="33cdc-131">**string**</span></span>](string.md)
</dt> </dl>

 

 