---
title: Array, attribut
description: Les tableaux sont des collections homogènes de données accessibles par un numéro d’index ou d’élément.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- attribut de tableau MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106527141"
---
# <a name="arrays-attribute"></a><span data-ttu-id="68cb6-104">Array, attribut</span><span class="sxs-lookup"><span data-stu-id="68cb6-104">arrays attribute</span></span>

<span data-ttu-id="68cb6-105">Les tableaux sont des collections homogènes de données accessibles par un numéro d’index ou d’élément.</span><span class="sxs-lookup"><span data-stu-id="68cb6-105">Arrays are homogenous collections of data accessed by an index or element number.</span></span>

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="68cb6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68cb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68cb6-107">*type-attr-List*</span><span class="sxs-lookup"><span data-stu-id="68cb6-107">*type-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="68cb6-108">Spécifie zéro, un ou plusieurs attributs qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="68cb6-108">Specifies zero or more attributes that apply to the type.</span></span> <span data-ttu-id="68cb6-109">Les attributs de type valides incluent [**\[ \] handle**](handle.md), [**\[ \_ \] type de commutateur**](switch-type.md), [**\[ transmettre \_ en tant que \]**](transmit-as.md); l’attribut de pointeur [**\[ Ref \]**](ref.md), [**\[ unique \]**](unique.md)ou [**\[ ptr \]**](ptr.md); et les attributs d’utilisation [**\[ \_ handle \] de contexte**](context-handle.md), [**\[ chaîne \]**](string.md)et [**\[ Ignorer \]**](ignore.md).</span><span class="sxs-lookup"><span data-stu-id="68cb6-109">Valid type attributes include [**\[handle\]**](handle.md), [**\[switch\_type\]**](switch-type.md), [**\[transmit\_as\]**](transmit-as.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md), [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md).</span></span> <span data-ttu-id="68cb6-110">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="68cb6-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="68cb6-111">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="68cb6-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="68cb6-112">Spécifie l’identificateur de type, le type de base, le [**struct**](struct.md), l' [**Union**](union.md)ou le type [**enum**](enum.md) .</span><span class="sxs-lookup"><span data-stu-id="68cb6-112">Specifies the type identifier, base type, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type.</span></span> <span data-ttu-id="68cb6-113">La spécification de type peut inclure une spécification de stockage facultative.</span><span class="sxs-lookup"><span data-stu-id="68cb6-113">The type specification can include an optional storage specification.</span></span>

</dd> <dt>

<span data-ttu-id="68cb6-114">*pointeur-decl*</span><span class="sxs-lookup"><span data-stu-id="68cb6-114">*pointer-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="68cb6-115">Spécifie zéro ou plusieurs déclarateurs de pointeur.</span><span class="sxs-lookup"><span data-stu-id="68cb6-115">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="68cb6-116">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé en C, construit à partir de l' **\*** indicateur, modificateurs tels que **Far** et le qualificateur [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="68cb6-116">A pointer declarator is the same as the pointer declarator used in C, constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="68cb6-117">*déclarateur de tableau*</span><span class="sxs-lookup"><span data-stu-id="68cb6-117">*array-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="68cb6-118">Spécifie le nom du tableau, suivi de l’une des constructions suivantes pour chaque dimension du tableau : «**\[ \]**», « **\[\*\]** », «**\[ ***Const1*** \]**» ou «**\[ ***Lower...*** Upper \]**», où *Lower* et *Upper* sont des valeurs constantes qui représentent les limites inférieure et supérieure.</span><span class="sxs-lookup"><span data-stu-id="68cb6-118">Specifies the name of the array, followed by one of the following constructs for each dimension of the array: "**\[ \]**", "**\[\*\]**", "**\[***const1***\]**", or "**\[***lower...upper***\]**" where *lower* and *upper* are constant values that represent the lower and upper bounds.</span></span> <span data-ttu-id="68cb6-119">La constante *inférieure* doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="68cb6-119">The constant *lower* must evaluate to zero.</span></span>

</dd> <dt>

<span data-ttu-id="68cb6-120">*tag*</span><span class="sxs-lookup"><span data-stu-id="68cb6-120">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="68cb6-121">Spécifie une balise facultative pour la structure ou l’Union.</span><span class="sxs-lookup"><span data-stu-id="68cb6-121">Specifies an optional tag for the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="68cb6-122">*Field-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="68cb6-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="68cb6-123">Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent à la structure, au membre d’Union ou au paramètre de fonction.</span><span class="sxs-lookup"><span data-stu-id="68cb6-123">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="68cb6-124">Les attributs de champ valides sont [**\[ First \_ \]**](first-is.md)is, [**\[ Last \_ is \]**](last-is.md), [**\[ Length \_ \]**](length-is.md)is, [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md), the usage Attributes [**\[ String \]**](string.md)et [**\[ ignore \]**](ignore.md); les attributs de pointeur [**\[ Ref \]**](ref.md), [**\[ unique \]**](unique.md)et [**\[ ptr \]**](ptr.md); et le [**\[ \_ type \] de commutateur**](switch-type.md)d’Union.</span><span class="sxs-lookup"><span data-stu-id="68cb6-124">Valid field attributes include [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md); the usage attributes [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), and [**\[ptr\]**](ptr.md); and the union attribute [**\[switch\_type\]**](switch-type.md).</span></span> <span data-ttu-id="68cb6-125">Séparez plusieurs attributs de champ par des virgules.</span><span class="sxs-lookup"><span data-stu-id="68cb6-125">Separate multiple field attributes with commas.</span></span> <span data-ttu-id="68cb6-126">Notez que les attributs répertoriés ci-dessus, le **\[ premier \_ \]** est, le **\[ dernier \_ est \]**, et [**\[ Ignorer \]**](ignore.md) ne sont pas valides pour les unions.</span><span class="sxs-lookup"><span data-stu-id="68cb6-126">Note that of the attributes listed above, **\[first\_is\]**, **\[last\_is\]**, and [**\[ignore\]**](ignore.md) are not valid for unions.</span></span>

</dd> <dt>

<span data-ttu-id="68cb6-127">*Limited-expression*</span><span class="sxs-lookup"><span data-stu-id="68cb6-127">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="68cb6-128">Spécifie une expression de langage C.</span><span class="sxs-lookup"><span data-stu-id="68cb6-128">Specifies a C-language expression.</span></span> <span data-ttu-id="68cb6-129">Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="68cb6-129">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="68cb6-130">MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation.</span><span class="sxs-lookup"><span data-stu-id="68cb6-130">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="68cb6-131">*function-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="68cb6-131">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="68cb6-132">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="68cb6-132">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="68cb6-133">Les attributs de fonction valides sont [**\[ callback \]**](callback.md), [**\[ \] local**](local.md), l’attribut de pointeur [**\[ Ref \]**](ref.md), [**\[ unique \]**](unique.md)ou [**\[ ptr \]**](ptr.md); et la [**\[ chaîne \]**](string.md)d’attributs d’utilisation et le [**\[ \_ handle \] de contexte**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="68cb6-133">Valid function attributes are [**\[callback\]**](callback.md), [**\[local\]**](local.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), and [**\[context\_handle\]**](context-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="68cb6-134">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="68cb6-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="68cb6-135">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="68cb6-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="68cb6-136">*Param-attr-List*</span><span class="sxs-lookup"><span data-stu-id="68cb6-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="68cb6-137">Spécifie les attributs directionnels et un ou plusieurs attributs de champ facultatifs qui s’appliquent au paramètre de tableau.</span><span class="sxs-lookup"><span data-stu-id="68cb6-137">Specifies the directional attributes and one or more optional field attributes that apply to the array parameter.</span></span> <span data-ttu-id="68cb6-138">Les attributs de champ valides incluent [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ \] is**](size-is.md), [**\[ Length \_ is \]**](length-is.md), [**\[ First \_ is \]**](first-is.md)et [**\[ Last \_ is \]**](last-is.md).</span><span class="sxs-lookup"><span data-stu-id="68cb6-138">Valid field attributes include [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), [**\[length\_is\]**](length-is.md), [**\[first\_is\]**](first-is.md), and [**\[last\_is\]**](last-is.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68cb6-139">Notes</span><span class="sxs-lookup"><span data-stu-id="68cb6-139">Remarks</span></span>

<span data-ttu-id="68cb6-140">Les tableaux dans MIDL utilisent un style semblable à, mais pas exactement identiques à C et C++.</span><span class="sxs-lookup"><span data-stu-id="68cb6-140">Arrays in MIDL use a style similar to but not exactly the same as C and C++.</span></span> <span data-ttu-id="68cb6-141">Pour plus d’informations, consultez [tableaux MIDL](midl-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="68cb6-141">For more information, see [MIDL Arrays](midl-arrays.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="68cb6-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68cb6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68cb6-143">**rappel**</span><span class="sxs-lookup"><span data-stu-id="68cb6-143">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="68cb6-144">**const**</span><span class="sxs-lookup"><span data-stu-id="68cb6-144">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="68cb6-145">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="68cb6-145">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="68cb6-146">**variables**</span><span class="sxs-lookup"><span data-stu-id="68cb6-146">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="68cb6-147">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="68cb6-147">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="68cb6-148">**traitée**</span><span class="sxs-lookup"><span data-stu-id="68cb6-148">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="68cb6-149">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="68cb6-149">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="68cb6-150">**tenir**</span><span class="sxs-lookup"><span data-stu-id="68cb6-150">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="68cb6-151">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="68cb6-151">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="68cb6-152">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="68cb6-152">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="68cb6-153">**localisé**</span><span class="sxs-lookup"><span data-stu-id="68cb6-153">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="68cb6-154">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="68cb6-154">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="68cb6-155">**ptr**</span><span class="sxs-lookup"><span data-stu-id="68cb6-155">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="68cb6-156">**ref**</span><span class="sxs-lookup"><span data-stu-id="68cb6-156">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="68cb6-157">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="68cb6-157">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="68cb6-158">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="68cb6-158">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="68cb6-159">**modélis**</span><span class="sxs-lookup"><span data-stu-id="68cb6-159">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="68cb6-160">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="68cb6-160">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="68cb6-161">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="68cb6-161">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="68cb6-162">**UE**</span><span class="sxs-lookup"><span data-stu-id="68cb6-162">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="68cb6-163">**unique**</span><span class="sxs-lookup"><span data-stu-id="68cb6-163">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




