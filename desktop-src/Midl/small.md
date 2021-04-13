---
title: attribut de petite taille
description: Le mot clé Small désigne un nombre entier 8 bits.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- MIDL d’attribut de petite taille
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380635"
---
# <a name="small-attribute"></a><span data-ttu-id="7cc39-104">attribut de petite taille</span><span class="sxs-lookup"><span data-stu-id="7cc39-104">small attribute</span></span>

<span data-ttu-id="7cc39-105">Le mot clé **Small** désigne un nombre entier 8 bits.</span><span class="sxs-lookup"><span data-stu-id="7cc39-105">The **small** keyword designates an 8-bit integer number.</span></span>

``` syntax
small identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="7cc39-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cc39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cc39-107">*identificateur-nom*</span><span class="sxs-lookup"><span data-stu-id="7cc39-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7cc39-108">Spécifie un identificateur MIDL valide.</span><span class="sxs-lookup"><span data-stu-id="7cc39-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="7cc39-109">Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="7cc39-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cc39-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7cc39-110">Remarks</span></span>

<span data-ttu-id="7cc39-111">Le mot clé **Small** peut être précédé [**du mot clé signed ou du**](signed.md) mot clé [**unsigned**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="7cc39-111">The **small** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="7cc39-112">Le mot clé [**int**](int.md) est facultatif et peut être omis.</span><span class="sxs-lookup"><span data-stu-id="7cc39-112">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="7cc39-113">Pour le compilateur MIDL, un petit entier est **signé** par défaut et est synonyme de **Small int signé**.</span><span class="sxs-lookup"><span data-stu-id="7cc39-113">To the MIDL compiler, a small integer is **signed** by default and is synonymous with **signed small int**.</span></span>

<span data-ttu-id="7cc39-114">Le type d’entier **petit** est l’un des types de base du langage IDL.</span><span class="sxs-lookup"><span data-stu-id="7cc39-114">The **small** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="7cc39-115">Le **petit** type entier peut apparaître en tant que spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type Return-Function et en tant que spécificateur de type paramètre).</span><span class="sxs-lookup"><span data-stu-id="7cc39-115">The **small** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="7cc39-116">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="7cc39-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="7cc39-117">Le signe du **petit** type peut être modifié par le commutateur du compilateur MIDL [**/char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="7cc39-117">The sign of the **small** type can be modified by the MIDL compiler switch [**/char**](-char.md).</span></span> <span data-ttu-id="7cc39-118">Pour éviter toute confusion, spécifiez le signe du type entier avec les [**Mots clés signed**](signed.md) et [**unsigned**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="7cc39-118">To avoid confusion, specify the sign of the integer type with the keywords [**signed**](signed.md) and [**unsigned**](unsigned.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7cc39-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cc39-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cc39-120">**/Char**</span><span class="sxs-lookup"><span data-stu-id="7cc39-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="7cc39-121">**const**</span><span class="sxs-lookup"><span data-stu-id="7cc39-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="7cc39-122">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="7cc39-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7cc39-123">**int**</span><span class="sxs-lookup"><span data-stu-id="7cc39-123">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="7cc39-124">**long**</span><span class="sxs-lookup"><span data-stu-id="7cc39-124">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="7cc39-125">**short**</span><span class="sxs-lookup"><span data-stu-id="7cc39-125">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="7cc39-126">**abonné**</span><span class="sxs-lookup"><span data-stu-id="7cc39-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="7cc39-127">**non signé**</span><span class="sxs-lookup"><span data-stu-id="7cc39-127">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="7cc39-128">**typedef**</span><span class="sxs-lookup"><span data-stu-id="7cc39-128">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




