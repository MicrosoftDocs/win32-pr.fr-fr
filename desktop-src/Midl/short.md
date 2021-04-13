---
title: attribut Short
description: Le mot clé Short désigne un entier 16 bits.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- attribut MIDL Short
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312742"
---
# <a name="short-attribute"></a><span data-ttu-id="60b31-104">attribut Short</span><span class="sxs-lookup"><span data-stu-id="60b31-104">short attribute</span></span>

<span data-ttu-id="60b31-105">Le mot clé **short** désigne un entier 16 bits.</span><span class="sxs-lookup"><span data-stu-id="60b31-105">The **short** keyword designates a 16-bit integer.</span></span>

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="60b31-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60b31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b31-107">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="60b31-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="60b31-108">Spécifie un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="60b31-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="60b31-109">(Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les structures transmises dans les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="60b31-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="60b31-110">Ces déclarateurs sont autorisés dans les structures qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="60b31-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60b31-111">Notes</span><span class="sxs-lookup"><span data-stu-id="60b31-111">Remarks</span></span>

<span data-ttu-id="60b31-112">Le mot clé **short** peut être précédé du mot [**clé signed ou du**](signed.md) mot clé [**unsigned**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="60b31-112">The **short** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="60b31-113">Le mot clé [**int**](int.md) est facultatif et peut être omis.</span><span class="sxs-lookup"><span data-stu-id="60b31-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="60b31-114">Pour le compilateur MIDL, un entier Short est signé par défaut et est synonyme de **short int signé**.</span><span class="sxs-lookup"><span data-stu-id="60b31-114">To the MIDL compiler, a short integer is signed by default and is synonymous with **signed short int**.</span></span>

<span data-ttu-id="60b31-115">Le type d’entier **short** est l’un des types de base du langage IDL.</span><span class="sxs-lookup"><span data-stu-id="60b31-115">The **short** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="60b31-116">Le type entier **short** peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type fonction-retour et spécificateur de type de paramètre).</span><span class="sxs-lookup"><span data-stu-id="60b31-116">The **short** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="60b31-117">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="60b31-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="60b31-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60b31-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b31-119">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="60b31-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="60b31-120">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="60b31-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="60b31-121">**int**</span><span class="sxs-lookup"><span data-stu-id="60b31-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="60b31-122">**long**</span><span class="sxs-lookup"><span data-stu-id="60b31-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="60b31-123">**abonné**</span><span class="sxs-lookup"><span data-stu-id="60b31-123">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="60b31-124">**Small**</span><span class="sxs-lookup"><span data-stu-id="60b31-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="60b31-125">**non signé**</span><span class="sxs-lookup"><span data-stu-id="60b31-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




