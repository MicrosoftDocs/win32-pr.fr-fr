---
title: attribut de chaîne
description: L’attribut \ String \ indique que le tableau Char, WCHAR \_ t, Byte (ou équivalent) unidimensionnel ou le pointeur vers ce tableau doit être traité comme une chaîne.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- MIDL, attribut de chaîne
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940941"
---
# <a name="string-attribute"></a><span data-ttu-id="91052-104">attribut de chaîne</span><span class="sxs-lookup"><span data-stu-id="91052-104">string attribute</span></span>

<span data-ttu-id="91052-105">L’attribut **\[ \] String** indique que le tableau [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Byte**](byte.md) (ou équivalent) unidimensionnel ou le pointeur vers ce tableau doit être traité comme une chaîne.</span><span class="sxs-lookup"><span data-stu-id="91052-105">The **\[string\]** attribute indicates that the one-dimensional [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**byte**](byte.md) (or equivalent) array or the pointer to such an array must be treated as a string.</span></span> <span data-ttu-id="91052-106">La chaîne peut également être un tableau (ou un pointeur vers un tableau) de constructions dont les champs sont tous du type **Byte**.</span><span class="sxs-lookup"><span data-stu-id="91052-106">The string can also be an array (or a pointer to an array) of constructs whose fields are all of the type **byte**.</span></span>

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a><span data-ttu-id="91052-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91052-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91052-108">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="91052-108">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91052-109">Spécifie un ou plusieurs attributs qui s’appliquent à un type.</span><span class="sxs-lookup"><span data-stu-id="91052-109">Specifies one or more attributes that apply to a type.</span></span> <span data-ttu-id="91052-110">Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[ \] chaîne** et **\[** [**Ignorer**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="91052-110">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[string\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="91052-111">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="91052-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="91052-112">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="91052-112">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="91052-113">Spécifie un [type de base](midl-base-types.md), un type [**struct**](struct.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="91052-113">Specifies a [base type](midl-base-types.md), [**struct**](struct.md) type, or type identifier.</span></span> <span data-ttu-id="91052-114">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="91052-114">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="91052-115">*standard-déclarateur*</span><span class="sxs-lookup"><span data-stu-id="91052-115">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="91052-116">Spécifie un déclarateur C standard, tel qu’un identificateur, un déclarateur de pointeur ou un déclarateur de tableau.</span><span class="sxs-lookup"><span data-stu-id="91052-116">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="91052-117">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md)et [pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="91052-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="91052-118">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="91052-118">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91052-119">Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="91052-119">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="91052-120">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md)et [pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="91052-120">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="91052-121">La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="91052-121">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="91052-122">L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.</span><span class="sxs-lookup"><span data-stu-id="91052-122">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="91052-123">*Field-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="91052-123">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91052-124">Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent à la structure, au membre d’Union ou au paramètre de fonction.</span><span class="sxs-lookup"><span data-stu-id="91052-124">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="91052-125">Les deux attributs de champ valides sont **\[** [**Max \_**](max-is.md) **\]** et **\[** [**size \_ est**](size-is.md) **\]** ; les attributs d’utilisation **\[ String \]**, **\[ ignore \]** et **\[ Context \_ handle \]**, l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[ unique \]** ou **\[** [**ptr**](ptr.md) **\]** et le **\[ \_ type \] de commutateur** d’attribut Union.</span><span class="sxs-lookup"><span data-stu-id="91052-125">The two valid field attributes are **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**, the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**, and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="91052-126">Séparez plusieurs attributs de champ par des virgules.</span><span class="sxs-lookup"><span data-stu-id="91052-126">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="91052-127">*function-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="91052-127">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91052-128">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="91052-128">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="91052-129">Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l’attribut de pointeur **\[ \] ref**, **\[ unique \]** ou **\[ ptr \]**; et les attributs d’utilisation **\[ chaîne \]**, **\[ Ignorer \]** et **\[ \_ \] handle de contexte**.</span><span class="sxs-lookup"><span data-stu-id="91052-129">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="91052-130">*pointeur-decl*</span><span class="sxs-lookup"><span data-stu-id="91052-130">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="91052-131">Spécifie un déclarateur de pointeur facultatif auquel s’applique l’attribut de **\[ chaîne \]** .</span><span class="sxs-lookup"><span data-stu-id="91052-131">Specifies an optional pointer declarator to which the **\[string\]** attribute applies.</span></span> <span data-ttu-id="91052-132">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="91052-132">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="91052-133">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="91052-133">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="91052-134">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="91052-134">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="91052-135">*Parameter-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="91052-135">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91052-136">Se compose de zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="91052-136">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="91052-137">Les attributs de paramètre peuvent accepter et **\[ sortir \]** les attributs directionnels ; les attributs **\[ de \]** champ **\[** [**Max \_ sont**](max-is.md) **\]** et **\[** [**size \_ est**](size-is.md) **\]** ; l’attribut de pointeur **\[ \] ref**, **\[ unique \]** ou **\[ ptr \]**; et les attributs d’utilisation **\[ \_ handle \] de contexte** et **\[ chaîne \]**.</span><span class="sxs-lookup"><span data-stu-id="91052-137">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="91052-138">L’attribut d’utilisation **\[ ignore \]** ne peut pas être utilisé en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="91052-138">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="91052-139">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="91052-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91052-140">Notes</span><span class="sxs-lookup"><span data-stu-id="91052-140">Remarks</span></span>

<span data-ttu-id="91052-141">Si l’attribut de **\[ chaîne \]** est utilisé avec un tableau dont les limites sont déterminées au moment de l’exécution, vous devez également spécifier **\[ \_ \] une taille** , ou l’attribut **\[ Max \_ est \]** un attribut, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="91052-141">If the **\[string\]** attribute is used with an array whose bounds are determined at run time, you must also specify a **\[size\_is\]** or **\[max\_is\]** attribute, as in the following example:</span></span>

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

<span data-ttu-id="91052-142">L’attribut de **\[ chaîne \]** ne peut pas être utilisé avec des attributs qui spécifient la plage d’éléments transmis, par exemple **\[ First \_ est \]**, **\[ Last \_ is \]** et **\[ Length \_ est \]**.</span><span class="sxs-lookup"><span data-stu-id="91052-142">The **\[string\]** attribute cannot be used with attributes that specify the range of transmitted elements, such as **\[first\_is\]**, **\[last\_is\]**, and **\[length\_is\]**.</span></span>

<span data-ttu-id="91052-143">Lorsqu’il est utilisé sur des tableaux multidimensionnels, l’attribut de **\[ chaîne \]** s’applique au tableau le plus à droite.</span><span class="sxs-lookup"><span data-stu-id="91052-143">When used on multidimensional arrays, the **\[string\]** attribute applies to the rightmost array.</span></span>

<span data-ttu-id="91052-144">Pour définir une chaîne comptée, n’utilisez pas l’attribut de **\[ chaîne \]** .</span><span class="sxs-lookup"><span data-stu-id="91052-144">To define a counted string, do not use the **\[string\]** attribute.</span></span> <span data-ttu-id="91052-145">Utilisez un tableau de caractères ou un pointeur de type caractère tel que le suivant :</span><span class="sxs-lookup"><span data-stu-id="91052-145">Use a character array or character-based pointer such as the following:</span></span>

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

<span data-ttu-id="91052-146">L’attribut **\[ String \]** spécifie que le stub doit utiliser une méthode fournie par le langage pour déterminer la longueur des chaînes.</span><span class="sxs-lookup"><span data-stu-id="91052-146">The **\[string\]** attribute specifies that the stub should use a language-supplied method to determine the length of strings.</span></span>

<span data-ttu-id="91052-147">Lors de la déclaration de chaînes en C, vous devez allouer de l’espace pour un caractère supplémentaire qui marque la fin de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="91052-147">When declaring strings in C, you must allocate space for an extra character that marks the end of the string.</span></span>

## <a name="examples"></a><span data-ttu-id="91052-148">Exemples</span><span class="sxs-lookup"><span data-stu-id="91052-148">Examples</span></span>

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a><span data-ttu-id="91052-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91052-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91052-150">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="91052-150">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="91052-151">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="91052-151">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="91052-152">**rappel**</span><span class="sxs-lookup"><span data-stu-id="91052-152">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="91052-153">**Char**</span><span class="sxs-lookup"><span data-stu-id="91052-153">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="91052-154">**const**</span><span class="sxs-lookup"><span data-stu-id="91052-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="91052-155">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="91052-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="91052-156">**variables**</span><span class="sxs-lookup"><span data-stu-id="91052-156">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="91052-157">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="91052-157">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="91052-158">**traitée**</span><span class="sxs-lookup"><span data-stu-id="91052-158">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="91052-159">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="91052-159">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="91052-160">**tenir**</span><span class="sxs-lookup"><span data-stu-id="91052-160">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="91052-161">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="91052-161">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="91052-162">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="91052-162">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="91052-163">**localisé**</span><span class="sxs-lookup"><span data-stu-id="91052-163">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="91052-164">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="91052-164">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="91052-165">**pointeur \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="91052-165">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="91052-166">**ptr**</span><span class="sxs-lookup"><span data-stu-id="91052-166">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="91052-167">**ref**</span><span class="sxs-lookup"><span data-stu-id="91052-167">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="91052-168">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="91052-168">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="91052-169">**modélis**</span><span class="sxs-lookup"><span data-stu-id="91052-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="91052-170">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="91052-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="91052-171">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="91052-171">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="91052-172">**UE**</span><span class="sxs-lookup"><span data-stu-id="91052-172">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="91052-173">**unique**</span><span class="sxs-lookup"><span data-stu-id="91052-173">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="91052-174">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="91052-174">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 