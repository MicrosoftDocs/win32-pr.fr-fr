---
title: switch_type (attribut)
description: L’attribut \ Switch \_ type \ identifie le type de la variable utilisée en tant qu’Union discriminante. Le type de commutateur peut être un type entier, caractère, booléen ou énumération.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type MIDL de l’attribut
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841338"
---
# <a name="switch_type-attribute"></a><span data-ttu-id="a8532-105">\_attribut type de commutateur</span><span class="sxs-lookup"><span data-stu-id="a8532-105">switch\_type attribute</span></span>

<span data-ttu-id="a8532-106">L’attribut **\[ \_ type \] de commutateur** identifie le type de la variable utilisée en tant qu’Union discriminante.</span><span class="sxs-lookup"><span data-stu-id="a8532-106">The **\[switch\_type\]** attribute identifies the type of the variable used as the union discriminant.</span></span> <span data-ttu-id="a8532-107">Le type de commutateur peut être un type entier, caractère, booléen ou énumération.</span><span class="sxs-lookup"><span data-stu-id="a8532-107">The switch type can be an integer, character, Boolean, or enumeration type.</span></span>

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a><span data-ttu-id="a8532-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8532-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8532-109">*spécificateur de type Switch*</span><span class="sxs-lookup"><span data-stu-id="a8532-109">*switch-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a8532-110">Spécifie un type [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md)ou [**enum**](enum.md) , ou un identificateur de ce type.</span><span class="sxs-lookup"><span data-stu-id="a8532-110">Specifies an [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md), or [**enum**](enum.md) type, or an identifier of such a type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8532-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a8532-111">Remarks</span></span>

<span data-ttu-id="a8532-112">Tandis que l’attribut **\[ \_ type \] de commutateur** identifie le type de variable, le **\[** [**commutateur \_ est**](switch-is.md) **\]** attribute spécifie le nom du paramètre qui est l’Union discriminante.</span><span class="sxs-lookup"><span data-stu-id="a8532-112">While the **\[switch\_type\]** attribute identifies the variable type, the **\[**[**switch\_is**](switch-is.md)**\]** attribute specifies the name of the parameter that is the union discriminant.</span></span> <span data-ttu-id="a8532-113">L’attribut **\[ \_ type \] de commutateur** s’applique aux paramètres ou aux membres de structures ou d’unions.</span><span class="sxs-lookup"><span data-stu-id="a8532-113">The **\[switch\_type\]** attribute applies to parameters or members of structures or unions.</span></span>

<span data-ttu-id="a8532-114">L’Union et son discriminante doivent être spécifiés au même niveau logique.</span><span class="sxs-lookup"><span data-stu-id="a8532-114">The union and its discriminant must be specified at the same logical level.</span></span> <span data-ttu-id="a8532-115">Lorsque l’Union est un paramètre, l’Union discriminante doit être un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="a8532-115">When the union is a parameter, the union discriminant must be another parameter.</span></span> <span data-ttu-id="a8532-116">Lorsque l’Union est un champ d’une structure, discriminante doit être un autre champ de la structure au même niveau que le champ Union.</span><span class="sxs-lookup"><span data-stu-id="a8532-116">When the union is a field of a structure, the discriminant must be another field of the structure at the same level as the union field.</span></span>

## <a name="examples"></a><span data-ttu-id="a8532-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="a8532-117">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="a8532-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8532-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8532-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8532-119">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="a8532-120">**Char**</span><span class="sxs-lookup"><span data-stu-id="a8532-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="a8532-121">Unions encapsulées</span><span class="sxs-lookup"><span data-stu-id="a8532-121">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="a8532-122">**variables**</span><span class="sxs-lookup"><span data-stu-id="a8532-122">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="a8532-123">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="a8532-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a8532-124">**int**</span><span class="sxs-lookup"><span data-stu-id="a8532-124">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="a8532-125">Unions qui ne sont pas encapsulées</span><span class="sxs-lookup"><span data-stu-id="a8532-125">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="a8532-126">**le commutateur \_ est**</span><span class="sxs-lookup"><span data-stu-id="a8532-126">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="a8532-127">**UE**</span><span class="sxs-lookup"><span data-stu-id="a8532-127">**union**</span></span>](union.md)
</dt> </dl>

 

 




