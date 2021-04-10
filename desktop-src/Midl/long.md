---
title: attribut long
description: Le mot clé long désigne un entier 32 bits.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- long, attribut MIDL
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940413"
---
# <a name="long-attribute"></a><span data-ttu-id="f3684-104">attribut long</span><span class="sxs-lookup"><span data-stu-id="f3684-104">long attribute</span></span>

<span data-ttu-id="f3684-105">Le mot clé **long** désigne un entier 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f3684-105">The **long** keyword designates a 32-bit integer.</span></span>

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="f3684-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3684-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3684-107">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="f3684-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f3684-108">Spécifie un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="f3684-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="f3684-109">(Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les structures transmises dans les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="f3684-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="f3684-110">Ces déclarateurs sont autorisés dans les structures qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="f3684-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3684-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f3684-111">Remarks</span></span>

<span data-ttu-id="f3684-112">Le mot clé **long** peut être précédé du mot [**clé signed ou du**](signed.md) mot clé [**unsigned**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="f3684-112">The **long** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="f3684-113">Le mot clé [**int**](int.md) est facultatif et peut être omis.</span><span class="sxs-lookup"><span data-stu-id="f3684-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="f3684-114">Pour le compilateur MIDL, un entier long est signé par défaut et est synonyme de **long int signé**. Sur les plateformes 32 bits, **long** est synonyme de **int**.</span><span class="sxs-lookup"><span data-stu-id="f3684-114">To the MIDL compiler, a long integer is signed by default and is synonymous with **signed long int**. On 32-bit platforms, **long** is synonymous with **int**.</span></span>

<span data-ttu-id="f3684-115">Le type entier **long** est l’un des types de base du langage IDL.</span><span class="sxs-lookup"><span data-stu-id="f3684-115">The **long** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="f3684-116">Le type entier **long** peut apparaître en tant que spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type Return-Function et en tant que spécificateur de type paramètre).</span><span class="sxs-lookup"><span data-stu-id="f3684-116">The **long** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="f3684-117">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="f3684-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f3684-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3684-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3684-119">**const**</span><span class="sxs-lookup"><span data-stu-id="f3684-119">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="f3684-120">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="f3684-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="f3684-121">**consolidation**</span><span class="sxs-lookup"><span data-stu-id="f3684-121">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="f3684-122">**int**</span><span class="sxs-lookup"><span data-stu-id="f3684-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="f3684-123">**short**</span><span class="sxs-lookup"><span data-stu-id="f3684-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="f3684-124">**abonné**</span><span class="sxs-lookup"><span data-stu-id="f3684-124">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="f3684-125">**Small**</span><span class="sxs-lookup"><span data-stu-id="f3684-125">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="f3684-126">**typedef**</span><span class="sxs-lookup"><span data-stu-id="f3684-126">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="f3684-127">**non signé**</span><span class="sxs-lookup"><span data-stu-id="f3684-127">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




