---
title: unique (attribut)
description: L’attribut \ unique \ spécifie un pointeur unique.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- MIDL d’attribut unique
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512090"
---
# <a name="unique-attribute"></a><span data-ttu-id="818b3-104">unique (attribut)</span><span class="sxs-lookup"><span data-stu-id="818b3-104">unique attribute</span></span>

<span data-ttu-id="818b3-105">L’attribut **\[ unique \]** spécifie un pointeur unique.</span><span class="sxs-lookup"><span data-stu-id="818b3-105">The **\[unique\]** attribute specifies a unique pointer.</span></span>

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="818b3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="818b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="818b3-107">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="818b3-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="818b3-108">Spécifie un ou plusieurs attributs qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="818b3-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="818b3-109">Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[ \] unique** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[** [**chaîne**](string.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="818b3-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="818b3-110">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="818b3-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="818b3-111">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="818b3-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="818b3-112">Spécifie un [type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="818b3-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="818b3-113">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="818b3-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="818b3-114">*déclarateur et déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="818b3-114">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="818b3-115">Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="818b3-115">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="818b3-116">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md)et [pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="818b3-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="818b3-117">La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="818b3-117">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="818b3-118">L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.</span><span class="sxs-lookup"><span data-stu-id="818b3-118">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="818b3-119">*struct-or-Union-declarator*</span><span class="sxs-lookup"><span data-stu-id="818b3-119">*struct-or-union-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="818b3-120">Spécifie un déclarateur de [**struct**](struct.md) ou d' [**Union**](union.md) MIDL.</span><span class="sxs-lookup"><span data-stu-id="818b3-120">Specifies a MIDL [**struct**](struct.md) or [**union**](union.md) declarator.</span></span>

</dd> <dt>

<span data-ttu-id="818b3-121">*Field-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="818b3-121">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="818b3-122">Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent au membre de structure, au membre d’Union ou au paramètre de fonction.</span><span class="sxs-lookup"><span data-stu-id="818b3-122">Specifies zero or more field attributes that apply to the structure member, union member, or function parameter.</span></span> <span data-ttu-id="818b3-123">Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; the usage Attributes **\[ \] String**, **\[ ignore \]** et **\[ Context \_ \] handle**; the pointer **\[ Ref \]**, **\[ unique \]** ou **\[ ptr \]**; et le **\[ \_ type \] de commutateur** d’Union.</span><span class="sxs-lookup"><span data-stu-id="818b3-123">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="818b3-124">Séparez plusieurs attributs de champ par des virgules.</span><span class="sxs-lookup"><span data-stu-id="818b3-124">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="818b3-125">*function-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="818b3-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="818b3-126">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="818b3-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="818b3-127">Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l’attribut de pointeur **\[ \] ref**, **\[ unique \]** ou **\[ ptr \]**; et les attributs d’utilisation **\[ chaîne \]**, **\[ Ignorer \]** et **\[ \_ \] handle de contexte**.</span><span class="sxs-lookup"><span data-stu-id="818b3-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="818b3-128">*pointeur-decl*</span><span class="sxs-lookup"><span data-stu-id="818b3-128">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="818b3-129">Spécifie au moins un déclarateur de pointeur auquel s’applique l’attribut **\[ unique \]** .</span><span class="sxs-lookup"><span data-stu-id="818b3-129">Specifies at least one pointer declarator to which the **\[unique\]** attribute applies.</span></span> <span data-ttu-id="818b3-130">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="818b3-130">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="818b3-131">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="818b3-131">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="818b3-132">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="818b3-132">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="818b3-133">*Parameter-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="818b3-133">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="818b3-134">Se compose de zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="818b3-134">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="818b3-135">Les attributs de paramètre peuvent accepter et **\[ \] sortir** les attributs directionnels, les attributs **\[ de \]** **\[ \]**  **\[ \]** [](ptr.md) **\[ \_ \]** champ en **\[ premier \_ \]**,, le nom, la **\[ longueur \_ \]**, la valeur **\[ maximale \_ \]**, la **\[ taille \_ \]** et le **\[ \_ type \] de commutateur**; l’attribut de pointeur REF, unique ou PTR ; et le **\[ \_ handle \] de contexte** et la chaîne des attributs d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="818b3-135">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **unique**, or [**ptr**](ptr.md); and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="818b3-136">L’attribut d’utilisation **\[ ignore \]** ne peut pas être utilisé en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="818b3-136">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="818b3-137">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="818b3-137">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="818b3-138">Notes</span><span class="sxs-lookup"><span data-stu-id="818b3-138">Remarks</span></span>

<span data-ttu-id="818b3-139">Les attributs de pointeur peuvent être appliqués en tant qu’attribut de type ; en tant qu’attribut de champ qui s’applique à un membre de structure, un membre d’Union ou un paramètre ; ou en tant qu’attribut de fonction qui s’applique au type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="818b3-139">Pointer attributes can be applied as a type attribute; as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="818b3-140">L’attribut de pointeur peut également apparaître avec le **\[** mot clé [**\_ default du pointeur**](pointer-default.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="818b3-140">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="818b3-141">Un pointeur unique présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="818b3-141">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="818b3-142">Peut avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="818b3-142">Can have the value **NULL**.</span></span>
-   <span data-ttu-id="818b3-143">Peut changer pendant un appel de **null** en non **null**, de non **null à** **null** ou d’une valeur non **null** à une autre.</span><span class="sxs-lookup"><span data-stu-id="818b3-143">Can change during a call from **NULL** to non-**NULL**, from non-**NULL** to **NULL**, or from one non-**NULL** value to another.</span></span>
-   <span data-ttu-id="818b3-144">Peut allouer une nouvelle mémoire sur le client.</span><span class="sxs-lookup"><span data-stu-id="818b3-144">Can allocate new memory on the client.</span></span> <span data-ttu-id="818b3-145">Lorsque le pointeur unique passe de **null** à non **null**, les données retournées à partir du serveur sont écrites dans un nouveau stockage.</span><span class="sxs-lookup"><span data-stu-id="818b3-145">When the unique pointer changes from **NULL** to non-**NULL**, data returned from the server is written into new storage.</span></span>
-   <span data-ttu-id="818b3-146">Peut utiliser la mémoire existante sur le client sans allouer de nouvelle mémoire.</span><span class="sxs-lookup"><span data-stu-id="818b3-146">Can use existing memory on the client without allocating new memory.</span></span> <span data-ttu-id="818b3-147">Lorsqu’un pointeur unique change pendant un appel d’une valeur non **null** à une autre, le pointeur est supposé pointer vers un objet de données du même type.</span><span class="sxs-lookup"><span data-stu-id="818b3-147">When a unique pointer changes during a call from one non-**NULL** value to another, the pointer is assumed to point to a data object of the same type.</span></span> <span data-ttu-id="818b3-148">Les données retournées par le serveur sont écrites dans le stockage existant spécifié par la valeur du pointeur unique avant l’appel.</span><span class="sxs-lookup"><span data-stu-id="818b3-148">Data returned from the server is written into existing storage specified by the value of the unique pointer before the call.</span></span>
-   <span data-ttu-id="818b3-149">Peut disposer d’une mémoire orpheline sur le client.</span><span class="sxs-lookup"><span data-stu-id="818b3-149">Can orphan memory on the client.</span></span> <span data-ttu-id="818b3-150">La mémoire référencée par un pointeur unique non **null** peut ne jamais être libérée si le pointeur unique devient **null** pendant un appel et que le client n’a pas d’autre moyen de déréférencer le stockage.</span><span class="sxs-lookup"><span data-stu-id="818b3-150">Memory referenced by a non-**NULL** unique pointer may never be freed if the unique pointer changes to **NULL** during a call and the client does not have another means of dereferencing the storage.</span></span>
-   <span data-ttu-id="818b3-151">Ne provoque pas d’alias.</span><span class="sxs-lookup"><span data-stu-id="818b3-151">Does not cause aliasing.</span></span> <span data-ttu-id="818b3-152">À l’instar du stockage pointé par un pointeur de référence, le stockage désigné par un pointeur unique ne peut pas être atteint à partir d’un autre nom de la fonction.</span><span class="sxs-lookup"><span data-stu-id="818b3-152">Like storage pointed to by a reference pointer, storage pointed to by a unique pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="818b3-153">Les stubs appellent les fonctions de gestion de mémoire fournies par l’utilisateur, [**MIDL \_ \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) et l' [**\_ utilisateur MIDL \_ Free**](/windows/desktop/Rpc/the-midl-user-free-function) pour allouer et libérer la mémoire requise pour les pointeurs uniques et leurs référents.</span><span class="sxs-lookup"><span data-stu-id="818b3-153">The stubs call the user-supplied memory-management functions [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) to allocate and deallocate memory required for unique pointers and their referents.</span></span>

<span data-ttu-id="818b3-154">Les restrictions suivantes s’appliquent aux pointeurs uniques :</span><span class="sxs-lookup"><span data-stu-id="818b3-154">The following restrictions apply to unique pointers:</span></span>

-   <span data-ttu-id="818b3-155">L’attribut **\[ unique \]** ne peut pas être appliqué aux paramètres de handle de liaison ( [**handle \_ t**](handle-t.md)) et aux paramètres de handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="818b3-155">The **\[unique\]** attribute cannot be applied to binding-handle parameters ( [**handle\_t**](handle-t.md)) and context-handle parameters.</span></span>
-   <span data-ttu-id="818b3-156">L’attribut **\[ \] unique** ne peut pas être appliqué aux paramètres de pointeur de **\[** [](out-idl.md) **\]** niveau supérieur uniquement (paramètres qui ont uniquement l’attribut directionnel **\[ out \]** ).</span><span class="sxs-lookup"><span data-stu-id="818b3-156">The **\[unique\]** attribute cannot be applied to **\[**[**out**](out-idl.md)**\]**-only top-level pointer parameters (parameters that have only the **\[out\]** directional attribute).</span></span>
-   <span data-ttu-id="818b3-157">Par défaut, les pointeurs de niveau supérieur dans les listes de paramètres sont des **\[** [](ref.md) **\]** pointeurs de référence.</span><span class="sxs-lookup"><span data-stu-id="818b3-157">By default, top-level pointers in parameter lists are **\[**[**ref**](ref.md)**\]** pointers.</span></span> <span data-ttu-id="818b3-158">Cela est vrai même si l’interface spécifie un **pointeur \_ par défaut (unique)**.</span><span class="sxs-lookup"><span data-stu-id="818b3-158">This is true even if the interface specifies **pointer\_default(unique)**.</span></span> <span data-ttu-id="818b3-159">Les paramètres de niveau supérieur dans les listes de paramètres doivent être spécifiés avec l’attribut **\[ unique \]** comme pointeur unique.</span><span class="sxs-lookup"><span data-stu-id="818b3-159">Top-level parameters in parameter lists must be specified with the **\[unique\]** attribute to be a unique pointer.</span></span>
-   <span data-ttu-id="818b3-160">Les pointeurs uniques ne peuvent pas être utilisés pour décrire la taille d’un tableau ou d’un bras d’Union, car les pointeurs uniques peuvent avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="818b3-160">Unique pointers cannot be used to describe the size of an array or union arm because unique pointers can have the value **NULL**.</span></span> <span data-ttu-id="818b3-161">Cette restriction empêche l’erreur qui se produit si une valeur **null** est utilisée comme taille de tableau ou taille d’Union-ARM.</span><span class="sxs-lookup"><span data-stu-id="818b3-161">This restriction prevents the error that results if a **NULL** value is used as the array size or the union-arm size.</span></span>

## <a name="examples"></a><span data-ttu-id="818b3-162">Exemples</span><span class="sxs-lookup"><span data-stu-id="818b3-162">Examples</span></span>

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="818b3-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="818b3-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="818b3-164">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="818b3-164">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="818b3-165">Tableaux et pointeurs</span><span class="sxs-lookup"><span data-stu-id="818b3-165">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="818b3-166">Attributs de tableau et de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="818b3-166">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="818b3-167">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="818b3-167">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="818b3-168">**rappel**</span><span class="sxs-lookup"><span data-stu-id="818b3-168">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="818b3-169">**const**</span><span class="sxs-lookup"><span data-stu-id="818b3-169">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="818b3-170">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="818b3-170">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="818b3-171">**variables**</span><span class="sxs-lookup"><span data-stu-id="818b3-171">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="818b3-172">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="818b3-172">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="818b3-173">**traitée**</span><span class="sxs-lookup"><span data-stu-id="818b3-173">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="818b3-174">**handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="818b3-174">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="818b3-175">**tenir**</span><span class="sxs-lookup"><span data-stu-id="818b3-175">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="818b3-176">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="818b3-176">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="818b3-177">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="818b3-177">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="818b3-178">**localisé**</span><span class="sxs-lookup"><span data-stu-id="818b3-178">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="818b3-179">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="818b3-179">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="818b3-180">allouer un \_ utilisateur MIDL \_</span><span class="sxs-lookup"><span data-stu-id="818b3-180">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="818b3-181">\_utilisateur \_ gratuit MIDL</span><span class="sxs-lookup"><span data-stu-id="818b3-181">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="818b3-182">**à**</span><span class="sxs-lookup"><span data-stu-id="818b3-182">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="818b3-183">**pointeur \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="818b3-183">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="818b3-184">**ptr**</span><span class="sxs-lookup"><span data-stu-id="818b3-184">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="818b3-185">**ref**</span><span class="sxs-lookup"><span data-stu-id="818b3-185">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="818b3-186">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="818b3-186">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="818b3-187">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="818b3-187">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="818b3-188">**modélis**</span><span class="sxs-lookup"><span data-stu-id="818b3-188">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="818b3-189">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="818b3-189">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="818b3-190">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="818b3-190">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="818b3-191">**UE**</span><span class="sxs-lookup"><span data-stu-id="818b3-191">**union**</span></span>](union.md)
</dt> </dl>

 

 