---
title: attribut signé
description: Le mot clé signed indique que le bit le plus significatif d’une variable de type entier représente un bit de signe plutôt qu’un bit de données.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- MIDL d’attribut signé
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103840969"
---
# <a name="signed-attribute"></a><span data-ttu-id="eec18-104">attribut signé</span><span class="sxs-lookup"><span data-stu-id="eec18-104">signed attribute</span></span>

<span data-ttu-id="eec18-105">Le mot clé **signed** indique que le bit le plus significatif d’une variable de type entier représente un bit de signe plutôt qu’un bit de données.</span><span class="sxs-lookup"><span data-stu-id="eec18-105">The **signed** keyword indicates the most significant bit of an integer variable represents a sign bit rather than a data bit.</span></span>

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="eec18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eec18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec18-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="eec18-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="eec18-108">Peut être de [**type char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)et [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="eec18-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="eec18-109">*identificateur-nom*</span><span class="sxs-lookup"><span data-stu-id="eec18-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="eec18-110">Spécifie un identificateur MIDL valide.</span><span class="sxs-lookup"><span data-stu-id="eec18-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="eec18-111">Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="eec18-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eec18-112">Notes</span><span class="sxs-lookup"><span data-stu-id="eec18-112">Remarks</span></span>

<span data-ttu-id="eec18-113">Ce mot clé est facultatif et peut être utilisé avec l’un des types caractère et entier [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)et [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="eec18-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="eec18-114">Vous pouvez éventuellement inclure le mot clé [**int**](int.md) après les qualificateurs de type **long**, **short** et **Small**.</span><span class="sxs-lookup"><span data-stu-id="eec18-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="eec18-115">Lorsque vous utilisez le commutateur de compilateur MIDL, les types [**de caractères et**](char-idl.md)d’entiers qui apparaissent dans le fichier IDL sans mots clés de signe explicite peuvent apparaître avec les mots clés **signés** ou [**non signés**](unsigned.md) dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="eec18-115">When you use the MIDL compiler switch [**char**](char-idl.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the **signed** or [**unsigned**](unsigned.md) keywords in the generated header file.</span></span> <span data-ttu-id="eec18-116">Pour éviter toute confusion, spécifiez le signe de l’entier et des types de caractères.</span><span class="sxs-lookup"><span data-stu-id="eec18-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="eec18-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eec18-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec18-118">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="eec18-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="eec18-119">**/Char**</span><span class="sxs-lookup"><span data-stu-id="eec18-119">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="eec18-120">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="eec18-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="eec18-121">**int**</span><span class="sxs-lookup"><span data-stu-id="eec18-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="eec18-122">**long**</span><span class="sxs-lookup"><span data-stu-id="eec18-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="eec18-123">**short**</span><span class="sxs-lookup"><span data-stu-id="eec18-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="eec18-124">**Small**</span><span class="sxs-lookup"><span data-stu-id="eec18-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="eec18-125">**non signé**</span><span class="sxs-lookup"><span data-stu-id="eec18-125">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="eec18-126">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="eec18-126">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




