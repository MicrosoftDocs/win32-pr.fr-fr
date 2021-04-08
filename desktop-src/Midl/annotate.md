---
title: annoter l’attribut
description: L’attribut \ Annotate \ vous permet de spécifier une chaîne d’annotation SAL pour la méthode, le paramètre ou le champ de structure spécifié.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- annoter l’attribut MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732085"
---
# <a name="annotate-attribute"></a><span data-ttu-id="e114a-104">annoter l’attribut</span><span class="sxs-lookup"><span data-stu-id="e114a-104">annotate attribute</span></span>

<span data-ttu-id="e114a-105">L’attribut **\[ annotation \]** vous permet de spécifier une chaîne d’annotation SAL pour la méthode, le paramètre ou le champ de structure spécifié.</span><span class="sxs-lookup"><span data-stu-id="e114a-105">The **\[annotate\]** attribute allows you to specify a SAL annotation string for the specified method, parameter, or structure field.</span></span>

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="e114a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e114a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e114a-107">*string*</span><span class="sxs-lookup"><span data-stu-id="e114a-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="e114a-108">Chaîne d’annotation SAL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e114a-108">Specified SAL annotation string.</span></span>

</dd> <dt>

<span data-ttu-id="e114a-109">*function-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e114a-109">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e114a-110">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="e114a-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="e114a-111">Les attributs de fonction valides incluent le [**\[ \] rappel**](callback.md); les attributs de pointeur [**\[ Ref \]**](ref.md), [**\[ unique \]**](unique.md)ou [**\[ ptr \]**](ptr.md); et les attributs d’utilisation [**\[ chaîne \]**](string.md), [**\[ Ignorer \]**](ignore.md)et [**\[ \_ handle \] de contexte**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="e114a-111">Valid function attributes include [**\[callback\]**](callback.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), [**\[ignore\]**](ignore.md), and [**\[context\_handle\]**](context-handle.md).</span></span> <span data-ttu-id="e114a-112">Plusieurs attributs doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="e114a-112">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="e114a-113">*déclarateur de fonction*</span><span class="sxs-lookup"><span data-stu-id="e114a-113">*function-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e114a-114">Spécifie le spécificateur de type, le nom de fonction et la liste de paramètres pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="e114a-114">Specifies the type specifier, function name, and parameter list for the function.</span></span>

</dd> <dt>

<span data-ttu-id="e114a-115">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="e114a-115">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e114a-116">Spécifie un type de **base \_**, un [**\[ struct \]**](struct.md), une [**Union**](union.md)ou un type [**\[ enum \]**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="e114a-116">Specifies a **base\_type**, [**\[struct\]**](struct.md), [**union**](union.md), or [**\[enum\]**](enum.md) type or type identifier.</span></span> <span data-ttu-id="e114a-117">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="e114a-117">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e114a-118">*pointeur-déclarateur*</span><span class="sxs-lookup"><span data-stu-id="e114a-118">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e114a-119">Spécifie zéro ou plusieurs déclarateurs de pointeur.</span><span class="sxs-lookup"><span data-stu-id="e114a-119">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="e114a-120">Un déclarateur de pointeur est identique à un déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**\[ const \]**](const.md).</span><span class="sxs-lookup"><span data-stu-id="e114a-120">A pointer declarator is the same as a pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**\[const\]**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="e114a-121">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="e114a-121">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e114a-122">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="e114a-122">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e114a-123">*Parameter-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e114a-123">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e114a-124">Spécifie zéro, un ou plusieurs attributs appropriés pour le type de paramètre.</span><span class="sxs-lookup"><span data-stu-id="e114a-124">Specifies zero or more attributes appropriate for the parameter type.</span></span> <span data-ttu-id="e114a-125">Les attributs de paramètre avec l’attribut in peuvent également prendre l' [**\[ attribut \] directionnel. les**](out-idl.md)attributs de champ [**\[ \_ sont \]**](first-is.md), [**\[ Last \_ \] is**](last-is.md), [**\[ Length \_ is \]**](length-is.md), [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md)et [**\[ Switch \_ type \]**](switch-type.md); les attributs [**\[ de \]**](in.md) pointeur [**\[ Ref \]**](ref.md), [**\[ unique \]**](unique.md)ou [**\[ ptr \]**](ptr.md); et les attributs d’utilisation [**\[ \_ handle \] de contexte**](context-handle.md) et [**\[ chaîne \]**](string.md).</span><span class="sxs-lookup"><span data-stu-id="e114a-125">Parameter attributes with the [**\[in\]**](in.md) attribute can also take the directional attribute [**\[out\]**](out-idl.md); the field attributes [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), and [**\[switch\_type\]**](switch-type.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md) and [**\[string\]**](string.md).</span></span> <span data-ttu-id="e114a-126">L’attribut d’utilisation [**\[ ignore \]**](ignore.md) ne peut pas être utilisé en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="e114a-126">The usage attribute [**\[ignore\]**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="e114a-127">Plusieurs attributs doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="e114a-127">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="e114a-128">*declarator*</span><span class="sxs-lookup"><span data-stu-id="e114a-128">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e114a-129">Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="e114a-129">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e114a-130">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**\[ tableaux \]**](../rpc/arrays.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="e114a-130">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**\[arrays\]**](../rpc/arrays.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="e114a-131">Le déclarateur de paramètre dans le déclarateur de fonction, tel que le nom du paramètre, est facultatif.</span><span class="sxs-lookup"><span data-stu-id="e114a-131">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e114a-132">Notes</span><span class="sxs-lookup"><span data-stu-id="e114a-132">Remarks</span></span>

<span data-ttu-id="e114a-133">L’attribut **\[ annoter \]** permet de remplacer les annotations SAL générées par MIDL ou de les ajouter à des endroits où MIDL ne génère pas explicitement d’annotation.</span><span class="sxs-lookup"><span data-stu-id="e114a-133">The **\[annotate\]** attribute allows overriding MIDL-generated SAL annotations or adding them in places where MIDL does not explicitly generate an annotation.</span></span> <span data-ttu-id="e114a-134">Si [**/SAL**](-sal.md) n’est pas spécifié sur la ligne de commande, cet attribut est ignoré.</span><span class="sxs-lookup"><span data-stu-id="e114a-134">If [**/sal**](-sal.md) is not specified on the command line, this attribute is ignored.</span></span>

## <a name="see-also"></a><span data-ttu-id="e114a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e114a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e114a-136">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="e114a-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="e114a-137">**/sal**</span><span class="sxs-lookup"><span data-stu-id="e114a-137">**/sal**</span></span>](-sal.md)
</dt> <dt>

[<span data-ttu-id="e114a-138">**/SAL \_ local**</span><span class="sxs-lookup"><span data-stu-id="e114a-138">**/sal\_local**</span></span>](-sal-local.md)
</dt> </dl>

 

 