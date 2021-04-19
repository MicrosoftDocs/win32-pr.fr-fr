---
title: attribut personnalisé
description: L’attribut \ custom \ crée un attribut défini par l’utilisateur.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- MIDL d’attribut personnalisé
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106513710"
---
# <a name="custom-attribute"></a><span data-ttu-id="e0a42-104">attribut personnalisé</span><span class="sxs-lookup"><span data-stu-id="e0a42-104">custom attribute</span></span>

<span data-ttu-id="e0a42-105">L’attribut **\[ personnalisé \]** crée un attribut défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e0a42-105">The **\[custom\]** attribute creates a user-defined attribute.</span></span>

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a><span data-ttu-id="e0a42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0a42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0a42-107">*ID d’attribut*</span><span class="sxs-lookup"><span data-stu-id="e0a42-107">*attribute-id*</span></span> 
</dt> <dd>

<span data-ttu-id="e0a42-108">GUID de l’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e0a42-108">The GUID for the custom attribute.</span></span>

</dd> <dt>

<span data-ttu-id="e0a42-109">*attribut-valeur*</span><span class="sxs-lookup"><span data-stu-id="e0a42-109">*attribute-value*</span></span> 
</dt> <dd>

<span data-ttu-id="e0a42-110">Valeur que l’attribut contient.</span><span class="sxs-lookup"><span data-stu-id="e0a42-110">The value that the attribute holds.</span></span> <span data-ttu-id="e0a42-111">La valeur doit être une valeur qui peut être placée dans un type VARIANT.</span><span class="sxs-lookup"><span data-stu-id="e0a42-111">The value must be one that can be put into a VARIANT type.</span></span>

</dd> <dt>

<span data-ttu-id="e0a42-112">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="e0a42-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e0a42-113">Autres attributs, tels que **\[** [**UUID**](uuid.md) **\]** et **\[** [**helpString**](helpstring.md) **\]** , qui s’appliquent à cet élément.</span><span class="sxs-lookup"><span data-stu-id="e0a42-113">Other attributes, such as **\[**[**uuid**](uuid.md)**\]** and **\[**[**helpstring**](helpstring.md)**\]**, that apply to this element.</span></span>

</dd> <dt>

<span data-ttu-id="e0a42-114">*type d’élément*</span><span class="sxs-lookup"><span data-stu-id="e0a42-114">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e0a42-115">Type d’élément auquel s’applique l’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e0a42-115">The type of element to which the custom attribute applies.</span></span> <span data-ttu-id="e0a42-116">Il peut s’agir d’une instruction de bibliothèque, d’informations de type, d’une variable, d’une fonction ou d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="e0a42-116">This can be a library statement, type information, a variable, a function, or a parameter.</span></span> <span data-ttu-id="e0a42-117">Vous ne pouvez pas utiliser un attribut personnalisé sur un membre d’une coclasse.</span><span class="sxs-lookup"><span data-stu-id="e0a42-117">You cannot use a custom attribute on a member of a coclass.</span></span>

</dd> <dt>

<span data-ttu-id="e0a42-118">*nom de l’élément*</span><span class="sxs-lookup"><span data-stu-id="e0a42-118">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e0a42-119">Nom de l'élément.</span><span class="sxs-lookup"><span data-stu-id="e0a42-119">The name of the element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0a42-120">Notes</span><span class="sxs-lookup"><span data-stu-id="e0a42-120">Remarks</span></span>

<span data-ttu-id="e0a42-121">Utilisez l’attribut **\[ personnalisé \]** pour définir votre propre attribut.</span><span class="sxs-lookup"><span data-stu-id="e0a42-121">Use the **\[custom\]** attribute to define your own attribute.</span></span> <span data-ttu-id="e0a42-122">Par exemple, vous pouvez créer un attribut à valeur de chaîne qui donne le ProgID pour une classe.</span><span class="sxs-lookup"><span data-stu-id="e0a42-122">For example, you might create a string-valued attribute that gives the ProgID for a class.</span></span>

<span data-ttu-id="e0a42-123">Pour récupérer une valeur d’attribut personnalisée, appelez l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e0a42-123">To retrieve a custom attribute value call one of the following:</span></span>

-   <span data-ttu-id="e0a42-124">ITypeLib2 :: GetCustData (rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="e0a42-124">ITypeLib2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="e0a42-125">ITypeInfo2 :: GetCustData (rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="e0a42-125">ITypeInfo2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="e0a42-126">ITypeInfo2 :: GetFuncCustData (index, rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="e0a42-126">ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)</span></span>
-   <span data-ttu-id="e0a42-127">ITypeInfo2 :: GetVarCustData (index, rguid, pVarVal)</span><span class="sxs-lookup"><span data-stu-id="e0a42-127">ITypeInfo2::GetVarCustData(index, rguid, pvarval)</span></span>
-   <span data-ttu-id="e0a42-128">ITypeInfo2 :: GetParamCustData (indexFunc, indexParam, rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="e0a42-128">ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)</span></span>

## <a name="see-also"></a><span data-ttu-id="e0a42-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0a42-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a42-130">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="e0a42-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="e0a42-131">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="e0a42-131">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="e0a42-132">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="e0a42-132">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="e0a42-133">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="e0a42-133">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="e0a42-134">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="e0a42-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="e0a42-135">**universel**</span><span class="sxs-lookup"><span data-stu-id="e0a42-135">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 