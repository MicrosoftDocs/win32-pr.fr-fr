---
title: max_is (attribut)
description: L’attribut \ Max \_ is \ désigne la valeur maximale d’un index de tableau valide.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314813"
---
# <a name="max_is-attribute"></a><span data-ttu-id="c47bd-104">Max \_ is (attribut)</span><span class="sxs-lookup"><span data-stu-id="c47bd-104">max\_is attribute</span></span>

<span data-ttu-id="c47bd-105">L’attribut **\[ Max \_ is \]** désigne la valeur maximale d’un index de tableau valide.</span><span class="sxs-lookup"><span data-stu-id="c47bd-105">The **\[max\_is\]** attribute designates the maximum value for a valid array index.</span></span>

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="c47bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c47bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c47bd-107">*Limited-expression-List*</span><span class="sxs-lookup"><span data-stu-id="c47bd-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c47bd-108">Spécifie une ou plusieurs expressions en langage C.</span><span class="sxs-lookup"><span data-stu-id="c47bd-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="c47bd-109">Chaque expression prend la valeur d’un entier qui représente l’index de tableau valide le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="c47bd-109">Each expression evaluates to an integer that represents the highest valid array index.</span></span> <span data-ttu-id="c47bd-110">Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="c47bd-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="c47bd-111">MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation.</span><span class="sxs-lookup"><span data-stu-id="c47bd-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="c47bd-112">Séparez plusieurs expressions par des virgules.</span><span class="sxs-lookup"><span data-stu-id="c47bd-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c47bd-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c47bd-113">Remarks</span></span>

<span data-ttu-id="c47bd-114">L’attribut **\[ Max \_ is \]** ne correspond pas nécessairement au nombre d’éléments du tableau.</span><span class="sxs-lookup"><span data-stu-id="c47bd-114">The **\[max\_is\]** attribute does not necessarily correspond to the number of elements in the array.</span></span> <span data-ttu-id="c47bd-115">Pour un tableau de taille *n* en C, où le premier élément du tableau est l’élément numéro zéro, la valeur maximale pour un index de tableau valide est *n*– 1.</span><span class="sxs-lookup"><span data-stu-id="c47bd-115">For an array of size *n* in C, where the first array element is element number zero, the maximum value for a valid array index is *n*–1.</span></span>

<span data-ttu-id="c47bd-116">L’attribut **\[ Max \_ is \]** ne peut pas être utilisé en tant qu’attribut de champ en même temps que la **\[** [**taille \_ est**](size-is.md) un **\]** attribut.</span><span class="sxs-lookup"><span data-stu-id="c47bd-116">The **\[max\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**size\_is**](size-is.md)**\]** attribute.</span></span>

<span data-ttu-id="c47bd-117">Bien qu’il soit légal d’utiliser l’attribut **\[ Max \_ is \]** avec une expression constante, cette opération est inefficace et inutile.</span><span class="sxs-lookup"><span data-stu-id="c47bd-117">While it is legal to use the **\[max\_is\]** attribute with a constant expression, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="c47bd-118">Par exemple, utilisez un tableau de taille fixe :</span><span class="sxs-lookup"><span data-stu-id="c47bd-118">For example, use a fixed size array:</span></span>

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

<span data-ttu-id="c47bd-119">plutôt que :</span><span class="sxs-lookup"><span data-stu-id="c47bd-119">instead of:</span></span>

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a><span data-ttu-id="c47bd-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="c47bd-120">Examples</span></span>

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a><span data-ttu-id="c47bd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c47bd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47bd-122">Attributs de champ</span><span class="sxs-lookup"><span data-stu-id="c47bd-122">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="c47bd-123">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="c47bd-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c47bd-124">**min \_ est**</span><span class="sxs-lookup"><span data-stu-id="c47bd-124">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="c47bd-125">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="c47bd-125">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 