---
title: ref (attribut)
description: L’attribut \ Ref \ identifie un pointeur de référence. Il est utilisé simplement pour représenter un niveau d’indirection.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- MIDL (MIDL), attribut de référence
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842154"
---
# <a name="ref-attribute"></a><span data-ttu-id="ac362-105">ref (attribut)</span><span class="sxs-lookup"><span data-stu-id="ac362-105">ref attribute</span></span>

<span data-ttu-id="ac362-106">L’attribut **\[ Ref \]** identifie un pointeur de référence.</span><span class="sxs-lookup"><span data-stu-id="ac362-106">The **\[ref\]** attribute identifies a reference pointer.</span></span> <span data-ttu-id="ac362-107">Il est utilisé simplement pour représenter un niveau d’indirection.</span><span class="sxs-lookup"><span data-stu-id="ac362-107">It is used simply to represent a level of indirection.</span></span>

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="ac362-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac362-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac362-109">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="ac362-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ac362-110">Spécifie un ou plusieurs attributs qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="ac362-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="ac362-111">Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; les attributs de pointeur **\[ Ref \]**, **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[** [**chaîne**](string.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ac362-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attributes **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="ac362-112">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ac362-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="ac362-113">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="ac362-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="ac362-114">Spécifie un type de [base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md)ou un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="ac362-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="ac362-115">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="ac362-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="ac362-116">*standard-déclarateur*</span><span class="sxs-lookup"><span data-stu-id="ac362-116">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="ac362-117">Spécifie un déclarateur C standard, tel qu’un identificateur, un déclarateur de pointeur ou un déclarateur de tableau.</span><span class="sxs-lookup"><span data-stu-id="ac362-117">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="ac362-118">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="ac362-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="ac362-119">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="ac362-119">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ac362-120">Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="ac362-120">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="ac362-121">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="ac362-121">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="ac362-122">La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ac362-122">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="ac362-123">L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.</span><span class="sxs-lookup"><span data-stu-id="ac362-123">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="ac362-124">*Field-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ac362-124">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ac362-125">Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent à la structure, au membre d’Union ou au paramètre de fonction.</span><span class="sxs-lookup"><span data-stu-id="ac362-125">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="ac362-126">Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; the usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**ignore**](ignore.md) **\]** et **\[** [**Context \_ handle**](context-handle.md) **\]** ; The pointer **\[ \] ref**, **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et le **\[** [**\_ type de commutateur**](switch-type.md)d’Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="ac362-126">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="ac362-127">Séparez plusieurs attributs de champ par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ac362-127">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="ac362-128">*function-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ac362-128">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ac362-129">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="ac362-129">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="ac362-130">Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l’attribut de pointeur **\[ Ref \]**, **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[** [**\_ handle de contexte**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ac362-130">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="ac362-131">*pointeur-decl*</span><span class="sxs-lookup"><span data-stu-id="ac362-131">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="ac362-132">Spécifie au moins un déclarateur de pointeur auquel s’applique l’attribut **\[ Ref \]** .</span><span class="sxs-lookup"><span data-stu-id="ac362-132">Specifies at least one pointer declarator to which the **\[ref\]** attribute applies.</span></span> <span data-ttu-id="ac362-133">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="ac362-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac362-134">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="ac362-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ac362-135">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="ac362-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="ac362-136">*Parameter-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ac362-136">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ac362-137">Se compose de zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="ac362-137">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="ac362-138">Les attributs de paramètre peuvent accepter et sortir les attributs directionnels, **\[** les attributs [**de champ en**](in.md) premier,, le **\]** **\[** [](out-idl.md) **\]** **\[** [**\_**](first-is.md) **\]** nom, la longueur, la valeur maximale, la **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**taille \_**](size-is.md) **\]** et le **\[** [**\_ type de commutateur**](switch-type.md) **\]** ; l’attribut de pointeur **\[ Ref \]**, **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et le **\[** [**\_ handle de contexte**](context-handle.md) et la chaîne des attributs d’utilisation **\]** **\[** [](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ac362-138">Parameter attributes can take the directional attributes **\[**[**in**](in.md)**\]** and **\[**[**out**](out-idl.md)**\]**; the field attributes **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, and **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]** and **\[**[**string**](string.md)**\]**.</span></span> <span data-ttu-id="ac362-139">L’attribut d’utilisation **\[** [**ignore**](ignore.md) **\]** ne peut pas être utilisé en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="ac362-139">The usage attribute **\[**[**ignore**](ignore.md)**\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="ac362-140">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ac362-140">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac362-141">Notes</span><span class="sxs-lookup"><span data-stu-id="ac362-141">Remarks</span></span>

<span data-ttu-id="ac362-142">Un attribut de pointeur peut être appliqué comme un attribut de type, comme un attribut de champ qui s’applique à un membre de structure, un membre d’Union ou un paramètre ; ou en tant qu’attribut de fonction qui s’applique au type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ac362-142">A pointer attribute can be applied as a type attribute, as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="ac362-143">L’attribut de pointeur peut également apparaître avec le **\[** mot clé [**\_ default du pointeur**](pointer-default.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ac362-143">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="ac362-144">Un pointeur de référence présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac362-144">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="ac362-145">Pointe toujours vers un stockage valide ; n’a jamais la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="ac362-145">Always points to valid storage; never has the value **NULL**.</span></span> <span data-ttu-id="ac362-146">Un pointeur de référence peut toujours être déréférencé.</span><span class="sxs-lookup"><span data-stu-id="ac362-146">A reference pointer can always be dereferenced.</span></span>
-   <span data-ttu-id="ac362-147">Jamais modifié pendant un appel.</span><span class="sxs-lookup"><span data-stu-id="ac362-147">Never changes during a call.</span></span> <span data-ttu-id="ac362-148">Un pointeur de référence pointe toujours vers le même stockage sur le client avant et après l’appel.</span><span class="sxs-lookup"><span data-stu-id="ac362-148">A reference pointer always points to the same storage on the client before and after the call.</span></span>
-   <span data-ttu-id="ac362-149">N’alloue pas de nouvelle mémoire sur le client.</span><span class="sxs-lookup"><span data-stu-id="ac362-149">Does not allocate new memory on the client.</span></span> <span data-ttu-id="ac362-150">Les données retournées à partir du serveur sont écrites dans le stockage existant spécifié par la valeur du pointeur de référence avant l’appel.</span><span class="sxs-lookup"><span data-stu-id="ac362-150">Data returned from the server is written into existing storage specified by the value of the reference pointer before the call.</span></span>
-   <span data-ttu-id="ac362-151">Ne provoque pas d’alias.</span><span class="sxs-lookup"><span data-stu-id="ac362-151">Does not cause aliasing.</span></span> <span data-ttu-id="ac362-152">Le stockage vers lequel pointe un pointeur de référence ne peut pas être atteint à partir d’un autre nom dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="ac362-152">Storage pointed to by a reference pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="ac362-153">Un pointeur de référence ne peut pas être utilisé en tant que type d’un pointeur retourné par une fonction.</span><span class="sxs-lookup"><span data-stu-id="ac362-153">A reference pointer cannot be used as the type of a pointer returned by a function.</span></span>

<span data-ttu-id="ac362-154">Si aucun attribut n’est spécifié pour un paramètre de pointeur de niveau supérieur, il est traité comme un pointeur de référence.</span><span class="sxs-lookup"><span data-stu-id="ac362-154">If no attribute is specified for a top-level pointer parameter, it is treated as a reference pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="ac362-155">Exemples</span><span class="sxs-lookup"><span data-stu-id="ac362-155">Examples</span></span>

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a><span data-ttu-id="ac362-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac362-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac362-157">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="ac362-157">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="ac362-158">Tableaux et pointeurs</span><span class="sxs-lookup"><span data-stu-id="ac362-158">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="ac362-159">Attributs de tableau et de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="ac362-159">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ac362-160">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="ac362-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="ac362-161">**rappel**</span><span class="sxs-lookup"><span data-stu-id="ac362-161">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="ac362-162">**const**</span><span class="sxs-lookup"><span data-stu-id="ac362-162">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="ac362-163">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="ac362-163">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="ac362-164">**variables**</span><span class="sxs-lookup"><span data-stu-id="ac362-164">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="ac362-165">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="ac362-165">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="ac362-166">**traitée**</span><span class="sxs-lookup"><span data-stu-id="ac362-166">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="ac362-167">**tenir**</span><span class="sxs-lookup"><span data-stu-id="ac362-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="ac362-168">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="ac362-168">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="ac362-169">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="ac362-169">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="ac362-170">**localisé**</span><span class="sxs-lookup"><span data-stu-id="ac362-170">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="ac362-171">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="ac362-171">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="ac362-172">**à**</span><span class="sxs-lookup"><span data-stu-id="ac362-172">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="ac362-173">**ptr**</span><span class="sxs-lookup"><span data-stu-id="ac362-173">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="ac362-174">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="ac362-174">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="ac362-175">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="ac362-175">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="ac362-176">**modélis**</span><span class="sxs-lookup"><span data-stu-id="ac362-176">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="ac362-177">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="ac362-177">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="ac362-178">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="ac362-178">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="ac362-179">**UE**</span><span class="sxs-lookup"><span data-stu-id="ac362-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="ac362-180">**unique**</span><span class="sxs-lookup"><span data-stu-id="ac362-180">**unique**</span></span>](unique.md)
</dt> </dl>

 

 