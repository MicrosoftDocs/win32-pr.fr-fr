---
title: attribut non signé
description: Le mot clé unsigned indique que le bit le plus significatif d’une variable de type entier représente un bit de données plutôt qu’un bit signé.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- MIDL d’attribut non signé
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106545734"
---
# <a name="unsigned-attribute"></a><span data-ttu-id="30921-104">attribut non signé</span><span class="sxs-lookup"><span data-stu-id="30921-104">unsigned attribute</span></span>

<span data-ttu-id="30921-105">Le mot clé **unsigned** indique que le bit le plus significatif d’une variable de type entier représente un bit de données plutôt qu’un bit signé.</span><span class="sxs-lookup"><span data-stu-id="30921-105">The **unsigned** keyword indicates that the most significant bit of an integer variable represents a data bit rather than a signed bit.</span></span>

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="30921-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30921-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30921-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="30921-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="30921-108">Peut être de [**type char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md)et [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="30921-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="30921-109">*identificateur-nom*</span><span class="sxs-lookup"><span data-stu-id="30921-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="30921-110">Spécifie un identificateur MIDL valide.</span><span class="sxs-lookup"><span data-stu-id="30921-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="30921-111">Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="30921-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30921-112">Notes</span><span class="sxs-lookup"><span data-stu-id="30921-112">Remarks</span></span>

<span data-ttu-id="30921-113">Ce mot clé est facultatif et peut être utilisé avec l’un des types caractère et entier [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)et [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="30921-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="30921-114">Vous pouvez éventuellement inclure le mot clé [**int**](int.md) après les qualificateurs de type **long**, **short** et **Small**.</span><span class="sxs-lookup"><span data-stu-id="30921-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="30921-115">Quand vous utilisez le commutateur de compilateur MIDL [**/char**](-char.md), les types caractère et entier qui apparaissent dans le fichier IDL sans mots clés de signe explicite peuvent apparaître avec le mot clé [**signé**](signed.md) ou **non signé** dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="30921-115">When you use the MIDL compiler switch [**/char**](-char.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the [**signed**](signed.md) or **unsigned** keyword in the generated header file.</span></span> <span data-ttu-id="30921-116">Pour éviter toute confusion, spécifiez le signe de l’entier et des types de caractères.</span><span class="sxs-lookup"><span data-stu-id="30921-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="30921-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30921-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30921-118">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="30921-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="30921-119">**Char**</span><span class="sxs-lookup"><span data-stu-id="30921-119">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="30921-120">**/Char**</span><span class="sxs-lookup"><span data-stu-id="30921-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="30921-121">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="30921-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="30921-122">**int**</span><span class="sxs-lookup"><span data-stu-id="30921-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="30921-123">**long**</span><span class="sxs-lookup"><span data-stu-id="30921-123">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="30921-124">**short**</span><span class="sxs-lookup"><span data-stu-id="30921-124">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="30921-125">**abonné**</span><span class="sxs-lookup"><span data-stu-id="30921-125">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="30921-126">**Small**</span><span class="sxs-lookup"><span data-stu-id="30921-126">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="30921-127">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="30921-127">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




