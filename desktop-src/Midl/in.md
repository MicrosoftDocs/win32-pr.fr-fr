---
title: in (attribut)
description: L’attribut \ in \ indique qu’un paramètre doit être passé de la procédure appelante à la procédure appelée.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- dans l’attribut MIDL
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726965"
---
# <a name="in-attribute"></a><span data-ttu-id="80806-104">in (attribut)</span><span class="sxs-lookup"><span data-stu-id="80806-104">in attribute</span></span>

<span data-ttu-id="80806-105">L’attribut **\[ in \]** indique qu’un paramètre doit être passé de la procédure appelante à la procédure appelée.</span><span class="sxs-lookup"><span data-stu-id="80806-105">The **\[in\]** attribute indicates that a parameter is to be passed from the calling procedure to the called procedure.</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="80806-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80806-107">*function-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="80806-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="80806-108">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="80806-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="80806-109">Les attributs de fonction valides sont **\[ callback \]**, **\[ local \]**, attribut de pointeur **\[ Ref \]**, **\[ unique \]** ou **\[ ptr \]**, et les attributs d’utilisation **\[ chaîne \]**, **\[ Ignorer \]** et **\[ \_ handle \] de contexte**.</span><span class="sxs-lookup"><span data-stu-id="80806-109">Valid function attributes are **\[callback\]**, **\[local\]**, the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**, and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="80806-110">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="80806-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="80806-111">Spécifie un type de **base \_**, un [**struct**](struct.md), une [**Union**](union.md)ou un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="80806-111">Specifies a **base\_type**, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="80806-112">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="80806-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="80806-113">*pointeur-déclarateur*</span><span class="sxs-lookup"><span data-stu-id="80806-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="80806-114">Spécifie zéro ou plusieurs déclarateurs de pointeur.</span><span class="sxs-lookup"><span data-stu-id="80806-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="80806-115">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="80806-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="80806-116">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="80806-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="80806-117">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="80806-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="80806-118">*Parameter-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="80806-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="80806-119">Spécifie zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="80806-119">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="80806-120">Les attributs de paramètre avec l’attribut in peuvent également prendre l' **\[ \] attribut directionnel**, les attributs **\[ de \]** **\[ \]** **\[ \]** **\[ \_ \]** champ en **\[ premier \_ \]** **\[ \]** **\[ \]** **\[ \_ \] ,,** le nom, la **\[ longueur \_ est \]**, le **\[ nombre maximal \_ \]**, la **\[ taille \_ et le type de commutateur, l’attribut de pointeur REF, unique ou PTR ; et le handle de contexte et la chaîne des attributs d’utilisation. \]** **\[ \_ \]**</span><span class="sxs-lookup"><span data-stu-id="80806-120">Parameter attributes with the **\[in\]** attribute can also take the directional attribute **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]** and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="80806-121">L’attribut d’utilisation **\[ ignore \]** ne peut pas être utilisé en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="80806-121">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="80806-122">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="80806-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="80806-123">*declarator*</span><span class="sxs-lookup"><span data-stu-id="80806-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="80806-124">Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="80806-124">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="80806-125">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="80806-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="80806-126">Le déclarateur de paramètre dans le déclarateur de fonction, tel que le nom du paramètre, est facultatif.</span><span class="sxs-lookup"><span data-stu-id="80806-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80806-127">Notes</span><span class="sxs-lookup"><span data-stu-id="80806-127">Remarks</span></span>

<span data-ttu-id="80806-128">L’attribut **\[ in \]** a un attribut réciproque, **\[** [**out**](out-idl.md) **\]** , qui indique qu’un paramètre doit être retourné à partir de la procédure appelée à la procédure appelante.</span><span class="sxs-lookup"><span data-stu-id="80806-128">The **\[in\]** attribute has a converse attribute, **\[**[**out**](out-idl.md)**\]**, which indicates that a parameter is to be returned from the called procedure to the calling procedure.</span></span> <span data-ttu-id="80806-129">Les attributs in et **\[ out \]** sont appelés attributs **\[ de \]** paramètres directionnels, car ils spécifient la direction dans laquelle les paramètres sont passés.</span><span class="sxs-lookup"><span data-stu-id="80806-129">The **\[in\]** and **\[out\]** attributes are known as directional parameter attributes because they specify the direction in which parameters are passed.</span></span> <span data-ttu-id="80806-130">Un paramètre peut être défini comme **\[ in \]**, **\[ out \]** ou **\[ in**, **out \]**.</span><span class="sxs-lookup"><span data-stu-id="80806-130">A parameter can be defined as **\[in\]**, **\[out\]**, or **\[in**, **out\]**.</span></span>

<span data-ttu-id="80806-131">L’attribut **\[ in \]** identifie les paramètres qui sont marshalés par le stub client pour la transmission au serveur.</span><span class="sxs-lookup"><span data-stu-id="80806-131">The **\[in\]** attribute identifies parameters that are marshaled by the client stub for transmission to the server.</span></span>

<span data-ttu-id="80806-132">L’attribut in est appliqué à un paramètre par défaut quand aucun attribut **\[ de \]** paramètre directionnel n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="80806-132">The **\[in\]** attribute is applied to a parameter by default when no directional parameter attribute is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="80806-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="80806-133">Examples</span></span>

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a><span data-ttu-id="80806-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80806-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80806-135">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="80806-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="80806-136">**allouer un \_ utilisateur MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="80806-136">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="80806-137">**à**</span><span class="sxs-lookup"><span data-stu-id="80806-137">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 