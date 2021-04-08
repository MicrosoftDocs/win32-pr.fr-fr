---
title: typedef (attribut)
description: Le mot clé IDL IDL autorise les déclarations typedef qui sont très similaires aux déclarations typedef du langage C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- MIDL de l’attribut typedef
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725141"
---
# <a name="typedef-attribute"></a><span data-ttu-id="5e584-104">typedef (attribut)</span><span class="sxs-lookup"><span data-stu-id="5e584-104">typedef attribute</span></span>

<span data-ttu-id="5e584-105">Le mot **clé** IDL IDL autorise les déclarations **typedef** qui sont très similaires aux déclarations **typedef** du langage C.</span><span class="sxs-lookup"><span data-stu-id="5e584-105">The IDL **typedef** keyword allows **typedef** declarations that are very similar to C-language **typedef** declarations.</span></span>

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a><span data-ttu-id="5e584-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e584-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e584-107">*IDL-type-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5e584-107">*idl-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5e584-108">Spécifie un ou plusieurs attributs qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="5e584-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="5e584-109">Les attributs de type valides dans un fichier IDL incluent **\[** [**descripteur**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[** [**chaîne**](string.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5e584-109">Valid type attributes in an IDL file include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="5e584-110">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5e584-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="5e584-111">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="5e584-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="5e584-112">Spécifie un [type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="5e584-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="5e584-113">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="5e584-113">An optional storage specification can precede *type-specifier*.</span></span> <span data-ttu-id="5e584-114">Le mot clé [**const**](const.md) peut précéder le *type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="5e584-114">The [**const**](const.md) keyword can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="5e584-115">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="5e584-115">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5e584-116">Spécifie les déclarateurs MIDL standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="5e584-116">Specifies standard MIDL declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="5e584-117">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="5e584-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="5e584-118">La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5e584-118">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="5e584-119">*ACF-type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="5e584-119">*acf-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5e584-120">Spécifie un ou plusieurs attributs qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="5e584-120">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="5e584-121">Les attributs de type valides dans un CCP incluent l' **\[** [**allocation**](allocate.md) **\]** , l' **\[** [**encodage**](encode.md) **\]** et le **\[** [**décodage**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5e584-121">Valid type attributes in an ACF include **\[**[**allocate**](allocate.md)**\]**, **\[**[**encode**](encode.md)**\]**, and **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="5e584-122">*TypeName*</span><span class="sxs-lookup"><span data-stu-id="5e584-122">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="5e584-123">Spécifie un type défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="5e584-123">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e584-124">Notes</span><span class="sxs-lookup"><span data-stu-id="5e584-124">Remarks</span></span>

<span data-ttu-id="5e584-125">La déclaration de **typedef** IDL est augmentée pour vous permettre d’associer des attributs de type aux types définis.</span><span class="sxs-lookup"><span data-stu-id="5e584-125">The IDL **typedef** declaration is augmented to allow you to associate type attributes with the defined types.</span></span> <span data-ttu-id="5e584-126">Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** , **\[** [**transmettre \_ en tant que**](transmit-as.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**\_ handle de contexte**](context-handle.md) **\]** , **\[** [**chaîne**](string.md) **\]** et **\[** [**Ignorer**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5e584-126">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span>

<span data-ttu-id="5e584-127">Le mot clé **typedef** dans un ACF applique des attributs aux types définis dans le fichier IDL correspondant.</span><span class="sxs-lookup"><span data-stu-id="5e584-127">The **typedef** keyword in an ACF applies attributes to types that are defined in the corresponding IDL file.</span></span> <span data-ttu-id="5e584-128">Par exemple, l’attribut [**allocate**](allocate.md) type vous permet de personnaliser l’allocation et la désallocation de mémoire à la fois par l’application et les stubs.</span><span class="sxs-lookup"><span data-stu-id="5e584-128">For example, the [**allocate**](allocate.md) type attribute allows you to customize memory allocation and deallocation by both the application and the stubs.</span></span>

<span data-ttu-id="5e584-129">L’instruction de **typedef** ACF s’affiche dans le corps du CCP.</span><span class="sxs-lookup"><span data-stu-id="5e584-129">The ACF **typedef** statement appears as part of the ACF body.</span></span> <span data-ttu-id="5e584-130">Notez que la syntaxe du **typedef** ACF est différente de la **syntaxe du typedef IDL et** de la syntaxe **typedef** du langage C.</span><span class="sxs-lookup"><span data-stu-id="5e584-130">Note that the ACF **typedef** syntax is different from the IDL **typedef** syntax and the C-language **typedef** syntax.</span></span> <span data-ttu-id="5e584-131">Aucun nouveau type ne peut être introduit dans le CCP.</span><span class="sxs-lookup"><span data-stu-id="5e584-131">No new types can be introduced in the ACF.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e584-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e584-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e584-133">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="5e584-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="5e584-134">**lui**</span><span class="sxs-lookup"><span data-stu-id="5e584-134">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="5e584-135">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="5e584-135">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="5e584-136">**const**</span><span class="sxs-lookup"><span data-stu-id="5e584-136">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="5e584-137">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="5e584-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="5e584-138">**décoder**</span><span class="sxs-lookup"><span data-stu-id="5e584-138">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="5e584-139">**contraire**</span><span class="sxs-lookup"><span data-stu-id="5e584-139">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="5e584-140">**variables**</span><span class="sxs-lookup"><span data-stu-id="5e584-140">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="5e584-141">**traitée**</span><span class="sxs-lookup"><span data-stu-id="5e584-141">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="5e584-142">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="5e584-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5e584-143">**tenir**</span><span class="sxs-lookup"><span data-stu-id="5e584-143">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="5e584-144">**ptr**</span><span class="sxs-lookup"><span data-stu-id="5e584-144">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="5e584-145">**ref**</span><span class="sxs-lookup"><span data-stu-id="5e584-145">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="5e584-146">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e584-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="5e584-147">**modélis**</span><span class="sxs-lookup"><span data-stu-id="5e584-147">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="5e584-148">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="5e584-148">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="5e584-149">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="5e584-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="5e584-150">**UE**</span><span class="sxs-lookup"><span data-stu-id="5e584-150">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="5e584-151">**unique**</span><span class="sxs-lookup"><span data-stu-id="5e584-151">**unique**</span></span>](unique.md)
</dt> </dl>

 

 