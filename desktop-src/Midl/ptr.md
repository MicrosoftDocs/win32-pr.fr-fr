---
title: ptr (attribut)
description: L’attribut \ PTR \ désigne un pointeur comme un pointeur complet.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- pointeur MIDL de l’attribut PTR
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314801"
---
# <a name="ptr-attribute"></a><span data-ttu-id="5d76f-104">ptr (attribut)</span><span class="sxs-lookup"><span data-stu-id="5d76f-104">ptr attribute</span></span>

<span data-ttu-id="5d76f-105">L’attribut **\[ ptr \]** désigne un pointeur comme un pointeur complet.</span><span class="sxs-lookup"><span data-stu-id="5d76f-105">The **\[ptr\]** attribute designates a pointer as a full pointer.</span></span>

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="5d76f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d76f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d76f-107">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="5d76f-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5d76f-108">Spécifie un ou plusieurs attributs qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="5d76f-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="5d76f-109">Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md)ou **\[ ptr \]**; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[** [**chaîne**](string.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5d76f-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md), or **\[ptr\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="5d76f-110">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5d76f-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="5d76f-111">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="5d76f-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="5d76f-112">Spécifie un type de [base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md)ou un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="5d76f-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="5d76f-113">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="5d76f-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="5d76f-114">*standard-déclarateur*</span><span class="sxs-lookup"><span data-stu-id="5d76f-114">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="5d76f-115">Spécifie un déclarateur C standard, tel qu’un identificateur, un déclarateur de pointeur ou un déclarateur de tableau.</span><span class="sxs-lookup"><span data-stu-id="5d76f-115">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="5d76f-116">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="5d76f-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="5d76f-117">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="5d76f-117">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5d76f-118">Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="5d76f-118">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="5d76f-119">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="5d76f-119">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="5d76f-120">La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5d76f-120">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="5d76f-121">L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5d76f-121">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="5d76f-122">*Field-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5d76f-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5d76f-123">Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent au membre de structure ou d’Union ou au paramètre de fonction.</span><span class="sxs-lookup"><span data-stu-id="5d76f-123">Specifies zero or more field attributes that apply to the structure or union member or function parameter.</span></span> <span data-ttu-id="5d76f-124">Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; the usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**ignore**](ignore.md) **\]** et **\[** [**Context \_ handle**](context-handle.md) **\]** ; The pointer **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[ ptr \]**; et le **\[** [**\_ type de commutateur**](switch-type.md)d’Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="5d76f-124">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="5d76f-125">Séparez plusieurs attributs de champ par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5d76f-125">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="5d76f-126">*function-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5d76f-126">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5d76f-127">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="5d76f-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="5d76f-128">Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[ \] ptr**; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[** [**\_ handle de contexte**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5d76f-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="5d76f-129">*pointeur-decl*</span><span class="sxs-lookup"><span data-stu-id="5d76f-129">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="5d76f-130">Spécifie au moins un déclarateur de pointeur auquel s’applique l’attribut **\[ ptr \]** .</span><span class="sxs-lookup"><span data-stu-id="5d76f-130">Specifies at least one pointer declarator to which the **\[ptr\]** attribute applies.</span></span> <span data-ttu-id="5d76f-131">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="5d76f-131">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d76f-132">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="5d76f-132">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5d76f-133">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="5d76f-133">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="5d76f-134">*Parameter-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5d76f-134">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5d76f-135">Se compose de zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="5d76f-135">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="5d76f-136">Les attributs [**de**](in.md) paramètre peuvent prendre les attributs directionnels et les [**éliminer**](out-idl.md). les attributs de [**champ \_ sont en premier**](first-is.md), la [**longueur \_ est**](length-is.md), le [**nombre maximal \_**](max-is.md), la taille et le [**\_ type de commutateur**](switch-type.md); l’attribut de pointeur [**ref**](ref.md), [**unique**](unique.md)ou **\[ ptr \]**; et le [**\_ handle de contexte**](context-handle.md) et la [**chaîne**](string.md)des attributs d’utilisation. [**\_**](last-is.md) [**\_**](size-is.md)</span><span class="sxs-lookup"><span data-stu-id="5d76f-136">Parameter attributes can take the directional attributes [**in**](in.md) and [**out**](out-idl.md); the field attributes [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**length\_is**](length-is.md), [**max\_is**](max-is.md), [**size\_is**](size-is.md), and [**switch\_type**](switch-type.md); the pointer attribute [**ref**](ref.md), [**unique**](unique.md), or **\[ptr\]**; and the usage attributes [**context\_handle**](context-handle.md) and [**string**](string.md).</span></span> <span data-ttu-id="5d76f-137">L’attribut d’utilisation [**ignore**](ignore.md) ne peut pas être utilisé en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="5d76f-137">The usage attribute [**ignore**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="5d76f-138">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5d76f-138">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d76f-139">Notes</span><span class="sxs-lookup"><span data-stu-id="5d76f-139">Remarks</span></span>

<span data-ttu-id="5d76f-140">Le pointeur complet désigné par l’attribut **\[ ptr \]** approche les fonctionnalités complètes du pointeur du langage C.</span><span class="sxs-lookup"><span data-stu-id="5d76f-140">The full pointer designated by the **\[ptr\]** attribute approaches the full functionality of the C-language pointer.</span></span> <span data-ttu-id="5d76f-141">Le pointeur complet peut avoir la valeur **null** et peut changer pendant l’appel de **null** en non **null**.</span><span class="sxs-lookup"><span data-stu-id="5d76f-141">The full pointer can have the value **NULL** and can change during the call from **NULL** to non-**NULL**.</span></span> <span data-ttu-id="5d76f-142">Le stockage désigné par les pointeurs complets peut être atteint par d’autres noms dans l’application prenant en charge les alias et les cycles.</span><span class="sxs-lookup"><span data-stu-id="5d76f-142">Storage pointed to by full pointers can be reached by other names in the application supporting aliasing and cycles.</span></span> <span data-ttu-id="5d76f-143">Cette fonctionnalité nécessite une plus grande surcharge au cours d’un appel de procédure distante pour identifier les données référencées par le pointeur, déterminer si la valeur est **null** et pour déterminer si deux pointeurs pointent vers les mêmes données.</span><span class="sxs-lookup"><span data-stu-id="5d76f-143">This functionality requires more overhead during a remote procedure call to identify the data referred to by the pointer, determine whether the value is **NULL**, and to discover if two pointers point to the same data.</span></span>

<span data-ttu-id="5d76f-144">Utiliser des pointeurs complets pour :</span><span class="sxs-lookup"><span data-stu-id="5d76f-144">Use full pointers for:</span></span>

-   <span data-ttu-id="5d76f-145">Valeurs de retour distantes.</span><span class="sxs-lookup"><span data-stu-id="5d76f-145">Remote return values.</span></span>
-   <span data-ttu-id="5d76f-146">Pointeurs doubles, lorsque la taille d’un paramètre de sortie n’est pas connue.</span><span class="sxs-lookup"><span data-stu-id="5d76f-146">Double pointers, when the size of an output parameter is not known.</span></span>
-   <span data-ttu-id="5d76f-147">Pointeurs **null** .</span><span class="sxs-lookup"><span data-stu-id="5d76f-147">**NULL** pointers.</span></span>

<span data-ttu-id="5d76f-148">Les pointeurs complets (et uniques) ne peuvent pas être utilisés pour décrire la taille d’un tableau ou d’une Union, car ces pointeurs peuvent avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5d76f-148">Full (and unique) pointers cannot be used to describe the size of an array or union because these pointers can have the value **NULL**.</span></span> <span data-ttu-id="5d76f-149">Cette restriction par MIDL empêche une erreur qui peut se produire lorsqu’une valeur **null** est utilisée comme taille.</span><span class="sxs-lookup"><span data-stu-id="5d76f-149">This restriction by MIDL prevents an error that can result when a **NULL** value is used as the size.</span></span>

<span data-ttu-id="5d76f-150">Les pointeurs de référence et uniques sont supposés ne pas générer d’alias de données.</span><span class="sxs-lookup"><span data-stu-id="5d76f-150">Reference and unique pointers are assumed to cause no aliasing of data.</span></span> <span data-ttu-id="5d76f-151">Un graphique dirigé obtenu en démarrant à partir d’un pointeur unique ou de référence et suivant uniquement les pointeurs unique ou de référence ne contient ni reconvergence, ni cycles.</span><span class="sxs-lookup"><span data-stu-id="5d76f-151">A directed graph obtained by starting from a unique or reference pointer and following only unique or reference pointers contains neither reconvergence nor cycles.</span></span>

<span data-ttu-id="5d76f-152">Pour éviter les alias, toutes les valeurs de pointeur doivent être obtenues à partir d’un pointeur d’entrée de la même classe de pointeur.</span><span class="sxs-lookup"><span data-stu-id="5d76f-152">To avoid aliasing, all pointer values should be obtained from an input pointer of the same class of pointer.</span></span> <span data-ttu-id="5d76f-153">Si plusieurs pointeurs pointent vers le même emplacement de mémoire, tous ces pointeurs doivent être des pointeurs complets.</span><span class="sxs-lookup"><span data-stu-id="5d76f-153">If more than one pointer points to the same memory location, all such pointers must be full pointers.</span></span>

<span data-ttu-id="5d76f-154">Dans certains cas, des pointeurs complets et uniques peuvent être mélangés.</span><span class="sxs-lookup"><span data-stu-id="5d76f-154">In some cases, full and unique pointers can be mixed.</span></span> <span data-ttu-id="5d76f-155">La valeur d’un pointeur unique peut être assignée à un pointeur complet, à condition que l’assignation ne viole pas les restrictions de modification de la valeur d’un pointeur unique.</span><span class="sxs-lookup"><span data-stu-id="5d76f-155">A full pointer can be assigned the value of a unique pointer, as long as the assignment does not violate the restrictions on changing the value of a unique pointer.</span></span> <span data-ttu-id="5d76f-156">Toutefois, lorsque vous affectez à un pointeur unique la valeur d’un pointeur complet, vous pouvez créer un alias.</span><span class="sxs-lookup"><span data-stu-id="5d76f-156">However, when you assign a unique pointer the value of a full pointer, you may cause aliasing.</span></span>

<span data-ttu-id="5d76f-157">Le mélange de pointeurs complets et uniques peut entraîner des alias, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="5d76f-157">Mixing full and unique pointers can cause aliasing, as demonstrated in the following example:</span></span>

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

<span data-ttu-id="5d76f-158">Bien que les points « t->Left » et « t->Right » pointent vers des emplacements de mémoire uniques, les « t->à gauche >pData » et le « t->>pData » sont des alias.</span><span class="sxs-lookup"><span data-stu-id="5d76f-158">Although "t->left" and "t->right" point to unique memory locations, "t->left->pdata" and "t->right->pdata" are aliased.</span></span> <span data-ttu-id="5d76f-159">Pour cette raison, les algorithmes de prise en charge d’alias doivent suivre tous les pointeurs (y compris les pointeurs uniques et de référence) qui peuvent finir par atteindre un pointeur complet.</span><span class="sxs-lookup"><span data-stu-id="5d76f-159">For this reason, aliasing-support algorithms must follow all pointers (including unique and reference pointers) that may eventually reach a full pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="5d76f-160">Exemples</span><span class="sxs-lookup"><span data-stu-id="5d76f-160">Examples</span></span>

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="5d76f-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d76f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d76f-162">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="5d76f-162">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="5d76f-163">Tableaux et pointeurs</span><span class="sxs-lookup"><span data-stu-id="5d76f-163">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="5d76f-164">Attributs de tableau et de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="5d76f-164">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d76f-165">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="5d76f-165">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="5d76f-166">**rappel**</span><span class="sxs-lookup"><span data-stu-id="5d76f-166">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="5d76f-167">**const**</span><span class="sxs-lookup"><span data-stu-id="5d76f-167">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="5d76f-168">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="5d76f-168">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="5d76f-169">**variables**</span><span class="sxs-lookup"><span data-stu-id="5d76f-169">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="5d76f-170">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="5d76f-170">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="5d76f-171">**traitée**</span><span class="sxs-lookup"><span data-stu-id="5d76f-171">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="5d76f-172">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="5d76f-172">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5d76f-173">**tenir**</span><span class="sxs-lookup"><span data-stu-id="5d76f-173">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="5d76f-174">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="5d76f-174">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="5d76f-175">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="5d76f-175">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="5d76f-176">**localisé**</span><span class="sxs-lookup"><span data-stu-id="5d76f-176">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="5d76f-177">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="5d76f-177">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="5d76f-178">**pointeur \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="5d76f-178">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="5d76f-179">**ref**</span><span class="sxs-lookup"><span data-stu-id="5d76f-179">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="5d76f-180">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="5d76f-180">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="5d76f-181">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="5d76f-181">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="5d76f-182">**modélis**</span><span class="sxs-lookup"><span data-stu-id="5d76f-182">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="5d76f-183">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="5d76f-183">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="5d76f-184">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="5d76f-184">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="5d76f-185">**UE**</span><span class="sxs-lookup"><span data-stu-id="5d76f-185">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="5d76f-186">**unique**</span><span class="sxs-lookup"><span data-stu-id="5d76f-186">**unique**</span></span>](unique.md)
</dt> </dl>

 

 