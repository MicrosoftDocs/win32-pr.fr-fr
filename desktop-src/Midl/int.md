---
title: int (attribut)
description: Le mot clé int spécifie un entier signé 32 bits sur les plateformes 32 bits. Sur les plateformes 16 bits, le mot clé int est un mot clé facultatif qui peut accompagner les mots clés Small, Short et long.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- MIDL d’attribut int
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678242"
---
# <a name="int-attribute"></a><span data-ttu-id="48181-105">int (attribut)</span><span class="sxs-lookup"><span data-stu-id="48181-105">int attribute</span></span>

<span data-ttu-id="48181-106">Le mot clé **int** spécifie un entier signé 32 bits sur les plateformes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="48181-106">The keyword **int** specifies a 32-bit signed integer on 32-bit platforms.</span></span> <span data-ttu-id="48181-107">Sur les plateformes 16 bits, le mot clé **int** est un mot clé facultatif qui peut accompagner les mots clés [**Small**](small.md), [**short**](short.md)et [**long**](long.md).</span><span class="sxs-lookup"><span data-stu-id="48181-107">On 16-bit platforms, the keyword **int** is an optional keyword that can accompany the keywords [**small**](small.md), [**short**](short.md), and [**long**](long.md).</span></span>

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="48181-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48181-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48181-109">*modificateur entier*</span><span class="sxs-lookup"><span data-stu-id="48181-109">*integer-modifier*</span></span> 
</dt> <dd>

<span data-ttu-id="48181-110">Spécifie le mot clé [**Small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)ou [**\_ \_ Int64**](--int64.md), qui sélectionne la taille des données de type entier.</span><span class="sxs-lookup"><span data-stu-id="48181-110">Specifies the keyword [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_\_int3264**](--int3264.md), or [**\_\_int64**](--int64.md),which selects the size of the integer data.</span></span> <span data-ttu-id="48181-111">Sur les plateformes 16 bits, le qualificateur de taille doit être présent.</span><span class="sxs-lookup"><span data-stu-id="48181-111">On 16-bit platforms, the size qualifier must be present.</span></span>

</dd> <dt>

<span data-ttu-id="48181-112">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="48181-112">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="48181-113">Spécifie un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="48181-113">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="48181-114">(Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les structures transmises dans les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="48181-114">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="48181-115">Ces déclarateurs sont autorisés dans les structures qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="48181-115">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48181-116">Notes</span><span class="sxs-lookup"><span data-stu-id="48181-116">Remarks</span></span>

<span data-ttu-id="48181-117">Les types d’entiers sont parmi les types de base du langage IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="48181-117">Integer types are among the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="48181-118">Ils peuvent apparaître en tant que spécificateurs de type dans les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type de retour de fonction et en tant que spécificateur de type de paramètre).</span><span class="sxs-lookup"><span data-stu-id="48181-118">They can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="48181-119">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="48181-119">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="48181-120">Si aucune spécification de signe entier n’est fournie, le type entier est [**signé**](signed.md)par défaut.</span><span class="sxs-lookup"><span data-stu-id="48181-120">If no integer sign specification is provided, the integer type defaults to [**signed**](signed.md).</span></span>

<span data-ttu-id="48181-121">Les compilateurs IDL DCE n’autorisent pas le [**mot clé signed**](signed.md) à spécifier le signe des types entiers.</span><span class="sxs-lookup"><span data-stu-id="48181-121">DCE IDL compilers do not allow the keyword [**signed**](signed.md) to specify the sign of integer types.</span></span> <span data-ttu-id="48181-122">Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur [**/OSF**](-osf.md) du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="48181-122">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="48181-123">Microsoft ne recommande pas l’utilisation de \_ \_ int3264 pour la communication à distance si cela peut être évité.</span><span class="sxs-lookup"><span data-stu-id="48181-123">Microsoft does not recommend the use of \_\_int3264 for remoting if it can be avoided.</span></span> <span data-ttu-id="48181-124">Pour plus d’informations sur l’utilisation et les limitations, consultez la rubrique sur [**\_ \_ int3264**](--int3264.md) .</span><span class="sxs-lookup"><span data-stu-id="48181-124">Please see the topic on [**\_\_int3264**](--int3264.md) for more information regarding it's use and limitations.</span></span>

## <a name="examples"></a><span data-ttu-id="48181-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="48181-125">Examples</span></span>

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a><span data-ttu-id="48181-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48181-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48181-127">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="48181-127">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="48181-128">**variables**</span><span class="sxs-lookup"><span data-stu-id="48181-128">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="48181-129">**consolidation**</span><span class="sxs-lookup"><span data-stu-id="48181-129">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="48181-130">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="48181-130">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="48181-131">**long**</span><span class="sxs-lookup"><span data-stu-id="48181-131">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="48181-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="48181-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="48181-133">**short**</span><span class="sxs-lookup"><span data-stu-id="48181-133">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="48181-134">**abonné**</span><span class="sxs-lookup"><span data-stu-id="48181-134">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="48181-135">**Small**</span><span class="sxs-lookup"><span data-stu-id="48181-135">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="48181-136">**modélis**</span><span class="sxs-lookup"><span data-stu-id="48181-136">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="48181-137">**typedef**</span><span class="sxs-lookup"><span data-stu-id="48181-137">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="48181-138">**UE**</span><span class="sxs-lookup"><span data-stu-id="48181-138">**union**</span></span>](union.md)
</dt> </dl>

 

 




