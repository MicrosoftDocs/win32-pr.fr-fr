---
title: switch_is (attribut)
description: L’attribut \ Switch \_ est \ spécifie l’expression ou l’identificateur agissant comme le discriminante d’Union qui sélectionne le membre Union.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940470"
---
# <a name="switch_is-attribute"></a><span data-ttu-id="9d3f6-104">le commutateur \_ est un attribut</span><span class="sxs-lookup"><span data-stu-id="9d3f6-104">switch\_is attribute</span></span>

<span data-ttu-id="9d3f6-105">L’attribut **\[ Switch \_ is \]** spécifie l’expression ou l’identificateur agissant en tant que discriminante d’Union qui sélectionne le membre Union.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-105">The **\[switch\_is\]** attribute specifies the expression or identifier acting as the union discriminant that selects the union member.</span></span>

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="9d3f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d3f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d3f6-107">*struct-tag*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-108">Spécifie une balise facultative pour une structure.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-108">Specifies an optional tag for a structure.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f6-109">*Limited-expr*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-109">*limited-expr*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-110">Spécifie une expression de langage C prise en charge par MIDL.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-110">Specifies a C-language expression supported by MIDL.</span></span> <span data-ttu-id="9d3f6-111">Presque toutes les expressions en langage C sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-111">Almost all C-language expressions are supported.</span></span> <span data-ttu-id="9d3f6-112">Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="9d3f6-113">MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs de pré-et post-incrémentation et de prédécrémentation.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-113">MIDL does not allow function invocations in expressions and does not allow pre- and post-increment and pre- and post-decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f6-114">*Field-attr-List*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-114">*field-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-115">Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent à un membre Union.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-115">Specifies zero or more field attributes that apply to a union member.</span></span> <span data-ttu-id="9d3f6-116">Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; the usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**ignore**](ignore.md) **\]** et **\[** [**Context \_ handle**](context-handle.md) **\]** ; The pointer **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et pour les membres qui sont eux-mêmes unions, le **\[** [**\_ type de commutateur**](switch-type.md)d’attribut Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="9d3f6-116">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and for members that are themselves unions, the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="9d3f6-117">Séparez plusieurs attributs de champ par des virgules.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-117">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f6-118">*type d’Union*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-118">*union-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-119">Spécifie l’identificateur de type d' [**Union**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="9d3f6-119">Specifies the [**union**](union.md) type identifier.</span></span> <span data-ttu-id="9d3f6-120">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-120">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f6-121">*déclarateur et déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-122">Spécifie un déclarateur C standard, tel qu’un identificateur, un déclarateur de pointeur et un déclarateur de tableau.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-122">Specifies a standard C declarator, such as an identifier, pointer declarator, and array declarator.</span></span> <span data-ttu-id="9d3f6-123">(Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les unions transmises dans les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-123">(Function declarators and bit-field declarations are not allowed in unions that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="9d3f6-124">Ces déclarateurs sont autorisés dans les unions qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-124">These declarators are allowed in unions that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f6-125">*function-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-126">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="9d3f6-127">Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l’attribut de pointeur **\[ \] ref**, **\[ unique \]** ou **\[ ptr \]**; et les attributs d’utilisation **\[ chaîne \]**, **\[ Ignorer \]** et **\[ \_ \] handle de contexte**.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f6-128">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-128">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-129">Spécifie un [type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-129">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="9d3f6-130">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-130">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f6-131">*pointeur-déclarateur*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-131">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-132">Spécifie zéro ou plusieurs déclarateurs de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-132">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="9d3f6-133">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="9d3f6-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d3f6-134">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-135">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f6-136">*Param-attr-List*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-137">Spécifie zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-137">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="9d3f6-138">Les attributs de paramètres peuvent accepter et **\[ \] sortir** les attributs directionnels, les attributs **\[ \] de** **\[ \_ \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]** **\[ \]** **\[ \_ \]** champ en **\[ premier \_ \]**,, le nom, la longueur, la valeur maximale, la taille et le **\[ \_ type \] de commutateur**, l’attribut de pointeur **\[ Ref \]**, unique ou PTR ; et le **\[ \_ handle \] de contexte** et la chaîne des attributs d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-138">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**, the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="9d3f6-139">L’attribut d’utilisation **\[ ignore \]** ne peut pas être utilisé en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-139">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="9d3f6-140">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-140">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="9d3f6-141">*type d’Union*</span><span class="sxs-lookup"><span data-stu-id="9d3f6-141">*union-type*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3f6-142">Identifie le spécificateur de type d' [**Union**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="9d3f6-142">Identifies the [**union**](union.md) type specifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d3f6-143">Notes</span><span class="sxs-lookup"><span data-stu-id="9d3f6-143">Remarks</span></span>

<span data-ttu-id="9d3f6-144">Le discriminante associé au **\[ commutateur \_ est \]** l’attribut doit être défini au même niveau logique que l’Union :</span><span class="sxs-lookup"><span data-stu-id="9d3f6-144">The discriminant associated with the **\[switch\_is\]** attribute must be defined at the same logical level as the union:</span></span>

-   <span data-ttu-id="9d3f6-145">Lorsque l’Union est un paramètre, l’Union discriminante doit être un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-145">When the union is a parameter, the union discriminant must be another parameter.</span></span>
-   <span data-ttu-id="9d3f6-146">Lorsque l’Union est un champ d’une structure, discriminante doit être un autre champ de la même structure.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-146">When the union is a field of a structure, the discriminant must be another field of the same structure.</span></span>

<span data-ttu-id="9d3f6-147">La séquence dans une structure ou une liste de paramètres de fonction n’est pas significative.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-147">The sequence in a structure or a function parameter list is not significant.</span></span> <span data-ttu-id="9d3f6-148">L’Union peut soit précéder ou suivre le discriminante.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-148">The union can either precede or follow the discriminant.</span></span>

<span data-ttu-id="9d3f6-149">Le **\[ commutateur \_ est \]** l’attribut peut apparaître en tant qu’attribut de champ ou en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="9d3f6-149">The **\[switch\_is\]** attribute can appear as a field attribute or as a parameter attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="9d3f6-150">Exemples</span><span class="sxs-lookup"><span data-stu-id="9d3f6-150">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="9d3f6-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d3f6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d3f6-152">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="9d3f6-152">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-153">**rappel**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-153">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-154">**const**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-155">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-156">Unions encapsulées</span><span class="sxs-lookup"><span data-stu-id="9d3f6-156">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-157">**variables**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-157">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-158">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-158">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-159">**tenir**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-159">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-160">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-160">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-161">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-161">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-162">**localisé**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-162">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-163">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-163">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-164">Unions qui ne sont pas encapsulées</span><span class="sxs-lookup"><span data-stu-id="9d3f6-164">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-165">**ptr**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-165">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-166">**ref**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-166">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-167">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-167">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-168">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-168">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-169">**modélis**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-170">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-171">**UE**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-171">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="9d3f6-172">**unique**</span><span class="sxs-lookup"><span data-stu-id="9d3f6-172">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




