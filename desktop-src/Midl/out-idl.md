---
title: out (attribut)
description: L’attribut \ out \ identifie les paramètres de pointeur retournés de la procédure appelée à la procédure appelante (du serveur au client).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- MIDL, attribut de sortie
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509652"
---
# <a name="out-attribute"></a><span data-ttu-id="e6be9-104">out (attribut)</span><span class="sxs-lookup"><span data-stu-id="e6be9-104">out attribute</span></span>

<span data-ttu-id="e6be9-105">L' \[ attribut **out** \] identifie les paramètres de pointeur retournés de la procédure appelée à la procédure appelante (du serveur au client).</span><span class="sxs-lookup"><span data-stu-id="e6be9-105">The \[**out**\] attribute identifies pointer parameters that are returned from the called procedure to the calling procedure (from the server to the client).</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a><span data-ttu-id="e6be9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6be9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6be9-107">*function-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e6be9-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e6be9-108">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="e6be9-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="e6be9-109">Les attributs de fonction valides sont \[ [**callback**](callback.md) \] , \[ [**local**](local.md), \] l’attribut de pointeur \[ [**ref**](ref.md) \] , \[ [**unique**](unique.md) \] ou \[ [**ptr**](ptr.md) \] ; et les attributs d’utilisation \[ [**chaîne**](string.md) \] , \[ [**Ignorer**](ignore.md) \] et \[ [**\_ handle de contexte**](context-handle.md) \] .</span><span class="sxs-lookup"><span data-stu-id="e6be9-109">Valid function attributes are \[[**callback**](callback.md)\], \[[**local**](local.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**string**](string.md)\], \[[**ignore**](ignore.md)\], and \[[**context\_handle**](context-handle.md)\].</span></span>

</dd> <dt>

<span data-ttu-id="e6be9-110">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="e6be9-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e6be9-111">Spécifie un type de [base \_](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md)ou un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="e6be9-111">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="e6be9-112">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="e6be9-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e6be9-113">*pointeur-déclarateur*</span><span class="sxs-lookup"><span data-stu-id="e6be9-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e6be9-114">Spécifie zéro ou plusieurs déclarateurs de pointeur.</span><span class="sxs-lookup"><span data-stu-id="e6be9-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="e6be9-115">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="e6be9-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6be9-116">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="e6be9-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e6be9-117">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="e6be9-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e6be9-118">*Parameter-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="e6be9-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e6be9-119">Spécifie zéro, un ou plusieurs attributs appropriés pour un type de paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="e6be9-119">Specifies zero or more attributes appropriate for a specified parameter type.</span></span> <span data-ttu-id="e6be9-120">Les attributs de paramètre avec l' \[  \] attribut out peuvent également prendre l’attribut directionnel \[  \] . les attributs de champ \[ [**\_ sont**](first-is.md) \] , \[ [**Last \_ is**](last-is.md), \] \[ [**Length \_ is**](length-is.md) \] , \[ [**Max \_ is**](max-is.md), \] \[ [**size \_ is**](size-is.md) \] et \[ [**\_ type de commutateur**](switch-type.md) \] ; le pointeur attribute \[ [**ref**](ref.md) \] , \[ [**unique**](unique.md) \] ou \[ [**ptr**](ptr.md) \] ; et les attributs d’utilisation \[ [**\_ handle de contexte**](context-handle.md) \] et \[ [**String**](string.md) \] .</span><span class="sxs-lookup"><span data-stu-id="e6be9-120">Parameter attributes with the \[**out**\] attribute can also take the directional attribute \[**out**\]; the field attributes \[[**first\_is**](first-is.md)\], \[[**last\_is**](last-is.md)\], \[[**length\_is**](length-is.md)\], \[[**max\_is**](max-is.md)\], \[[**size\_is**](size-is.md)\], and \[[**switch\_type**](switch-type.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**context\_handle**](context-handle.md)\] and \[[**string**](string.md)\].</span></span> <span data-ttu-id="e6be9-121">L’attribut d’utilisation \[ [**ignore**](ignore.md) \] ne peut pas être utilisé en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="e6be9-121">The usage attribute \[[**ignore**](ignore.md)\] cannot be used as a parameter attribute.</span></span> <span data-ttu-id="e6be9-122">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="e6be9-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e6be9-123">*declarator*</span><span class="sxs-lookup"><span data-stu-id="e6be9-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e6be9-124">Spécifie les déclarateurs standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="e6be9-124">Specifies the standard declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e6be9-125">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="e6be9-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="e6be9-126">Le déclarateur de paramètre dans le déclarateur de fonction, tel que le nom du paramètre, est facultatif.</span><span class="sxs-lookup"><span data-stu-id="e6be9-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6be9-127">Notes</span><span class="sxs-lookup"><span data-stu-id="e6be9-127">Remarks</span></span>

<span data-ttu-id="e6be9-128">L' \[ attribut **out** \] indique qu’un paramètre qui agit comme un pointeur et ses données associées en mémoire doit être repassé de la procédure appelée à la procédure d’appel.</span><span class="sxs-lookup"><span data-stu-id="e6be9-128">The \[**out**\] attribute indicates that a parameter that acts as a pointer and its associated data in memory are to be passed back from the called procedure to the calling procedure.</span></span>

<span data-ttu-id="e6be9-129">L' \[ attribut **out** \] doit être un pointeur.</span><span class="sxs-lookup"><span data-stu-id="e6be9-129">The \[**out**\] attribute must be a pointer.</span></span> <span data-ttu-id="e6be9-130">Les compilateurs IDL DCE nécessitent la présence d’un Explicit \* comme déclarateur de pointeur dans la déclaration du paramètre.</span><span class="sxs-lookup"><span data-stu-id="e6be9-130">DCE IDL compilers require the presence of an explicit \* as a pointer declarator in the parameter declaration.</span></span> <span data-ttu-id="e6be9-131">Microsoft IDL offre une extension qui supprime cette exigence et autorise un tableau ou un type de pointeur défini précédemment.</span><span class="sxs-lookup"><span data-stu-id="e6be9-131">Microsoft IDL offers an extension that drops this requirement and allows an array or a previously defined pointer type.</span></span>

<span data-ttu-id="e6be9-132">Un attribut associé, \[ [**dans**](in.md) \] , indique que le paramètre est passé de la procédure appelante à la procédure appelée.</span><span class="sxs-lookup"><span data-stu-id="e6be9-132">A related attribute, \[[**in**](in.md)\], indicates that the parameter is passed from the calling procedure to the called procedure.</span></span> <span data-ttu-id="e6be9-133">Les \[  \] attributs in et \[ **out** \] spécifient la direction dans laquelle les paramètres sont passés.</span><span class="sxs-lookup"><span data-stu-id="e6be9-133">The \[**in**\] and \[**out**\] attributes specify the direction in which the parameters are passed.</span></span> <span data-ttu-id="e6be9-134">Un paramètre peut être défini en tant que \[ **en** \] seule, en \[ **sortie** seule \] ou \[ **en** **sortie** \] .</span><span class="sxs-lookup"><span data-stu-id="e6be9-134">A parameter can be defined as \[**in**\]-only, \[**out**\]-only, or \[**in**, **out**\].</span></span>

<span data-ttu-id="e6be9-135">Un \[ paramètre en **sortie** \] seule est supposé être non défini lorsque la procédure distante est appelée et que la mémoire de l’objet est allouée par le serveur.</span><span class="sxs-lookup"><span data-stu-id="e6be9-135">An \[**out**\]-only parameter is assumed to be undefined when the remote procedure is called and memory for the object is allocated by the server.</span></span> <span data-ttu-id="e6be9-136">Étant donné que les curseurs/paramètres de niveau supérieur doivent toujours pointer vers un stockage valide, et ne peuvent donc pas avoir la **valeur null**, \[ **out** \] ne peut pas être appliqué aux \[ [](unique.md) \] pointeurs uniques ou \[ [**ptr**](ptr.md) de niveau supérieur \] .</span><span class="sxs-lookup"><span data-stu-id="e6be9-136">Since top-level pointer/parameters must always point to valid storage, and therefore cannot be **NULL**, \[**out**\] cannot be applied to top-level \[[**unique**](unique.md)\] or \[[**ptr**](ptr.md)\] pointers.</span></span> <span data-ttu-id="e6be9-137">Les paramètres qui sont \[ **uniques** \] ou les \[  \] pointeurs PTR doivent être \[ [**dans**](in.md) \] ou \[ **dans**, paramètres de **sortie** \] .</span><span class="sxs-lookup"><span data-stu-id="e6be9-137">Parameters that are \[**unique**\] or \[**ptr**\] pointers must be either \[[**in**](in.md)\] or \[**in**, **out**\] parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="e6be9-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="e6be9-138">Examples</span></span>

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a><span data-ttu-id="e6be9-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6be9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6be9-140">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="e6be9-140">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="e6be9-141">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="e6be9-141">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e6be9-142">**rappel**</span><span class="sxs-lookup"><span data-stu-id="e6be9-142">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="e6be9-143">**const**</span><span class="sxs-lookup"><span data-stu-id="e6be9-143">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="e6be9-144">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="e6be9-144">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="e6be9-145">**variables**</span><span class="sxs-lookup"><span data-stu-id="e6be9-145">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e6be9-146">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="e6be9-146">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="e6be9-147">**tenir**</span><span class="sxs-lookup"><span data-stu-id="e6be9-147">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="e6be9-148">**in**</span><span class="sxs-lookup"><span data-stu-id="e6be9-148">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="e6be9-149">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="e6be9-149">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="e6be9-150">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="e6be9-150">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="e6be9-151">**localisé**</span><span class="sxs-lookup"><span data-stu-id="e6be9-151">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="e6be9-152">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="e6be9-152">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="e6be9-153">**ptr**</span><span class="sxs-lookup"><span data-stu-id="e6be9-153">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="e6be9-154">**ref**</span><span class="sxs-lookup"><span data-stu-id="e6be9-154">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="e6be9-155">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="e6be9-155">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="e6be9-156">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6be9-156">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="e6be9-157">**modélis**</span><span class="sxs-lookup"><span data-stu-id="e6be9-157">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="e6be9-158">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="e6be9-158">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="e6be9-159">**UE**</span><span class="sxs-lookup"><span data-stu-id="e6be9-159">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="e6be9-160">**unique**</span><span class="sxs-lookup"><span data-stu-id="e6be9-160">**unique**</span></span>](unique.md)
</dt> </dl>

 

 