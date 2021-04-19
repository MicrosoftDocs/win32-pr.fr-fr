---
title: attribut masqué
description: L’attribut \ Hidden \ indique que l’élément existe, mais ne doit pas être affiché dans un navigateur orienté utilisateur.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- MIDL d’attribut masqué
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510877"
---
# <a name="hidden-attribute"></a><span data-ttu-id="7c8cd-104">attribut masqué</span><span class="sxs-lookup"><span data-stu-id="7c8cd-104">hidden attribute</span></span>

<span data-ttu-id="7c8cd-105">L’attribut **\[ Hidden \]** indique que l’élément existe, mais ne doit pas être affiché dans un navigateur orienté utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-105">The **\[hidden\]** attribute indicates that the item exists but should not be displayed in a user-oriented browser.</span></span>

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="7c8cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c8cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c8cd-107">*autres attributs*</span><span class="sxs-lookup"><span data-stu-id="7c8cd-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7c8cd-108">Zéro, un ou plusieurs attributs MIDL facultatifs.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-108">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="7c8cd-109">*appartient*</span><span class="sxs-lookup"><span data-stu-id="7c8cd-109">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="7c8cd-110">L’une des directives suivantes : [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)ou [**Library**](library.md).</span><span class="sxs-lookup"><span data-stu-id="7c8cd-110">One of the following directives: [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), or [**library**](library.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c8cd-111">*nom de l’élément*</span><span class="sxs-lookup"><span data-stu-id="7c8cd-111">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7c8cd-112">Nom que d’autres composants logiciels peuvent utiliser pour décourber l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-112">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="7c8cd-113">*Description*</span><span class="sxs-lookup"><span data-stu-id="7c8cd-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="7c8cd-114">Spécifie les instructions qui composent la définition de l’élément.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-114">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="7c8cd-115">*type de fonction*</span><span class="sxs-lookup"><span data-stu-id="7c8cd-115">*function-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7c8cd-116">Type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-116">Return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7c8cd-117">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="7c8cd-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7c8cd-118">Nom utilisé pour appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-118">Name used for invoking the function.</span></span>

</dd> <dt>

<span data-ttu-id="7c8cd-119">*liste de paramètres facultatifs*</span><span class="sxs-lookup"><span data-stu-id="7c8cd-119">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7c8cd-120">Zéro, un ou plusieurs paramètres de fonction.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-120">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c8cd-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7c8cd-121">Remarks</span></span>

<span data-ttu-id="7c8cd-122">L’attribut **\[ Hidden \]** vous permet de supprimer des membres de votre interface (en les protégeant d’un autre usage) tout en conservant la compatibilité avec le code existant.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-122">The **\[hidden\]** attribute allows you to remove members from your interface (by shielding them from further use) while maintaining compatibility with existing code.</span></span> <span data-ttu-id="7c8cd-123">Vous pouvez utiliser l' **\[ attribut \] Hidden** sur les propriétés, les méthodes et les instructions de [**coclasse**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md)et [**Library**](library.md) .</span><span class="sxs-lookup"><span data-stu-id="7c8cd-123">You can use the **\[hidden\]** attribute on properties, methods, and the [**coclass**](coclass.md), [**dispinterface**](dispinterface.md), [**interface**](interface.md), and [**library**](library.md) statements.</span></span>

<span data-ttu-id="7c8cd-124">Lorsqu’il est spécifié pour une bibliothèque, l’attribut **\[ Hidden \]** empêche l’affichage de la totalité de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-124">When specified for a library, the **\[hidden\]** attribute prevents the entire library from being displayed.</span></span> <span data-ttu-id="7c8cd-125">Cette utilisation est destinée aux contrôles.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-125">This usage is intended for use with controls.</span></span> <span data-ttu-id="7c8cd-126">Les hôtes doivent créer une bibliothèque de types qui encapsule le contrôle avec des propriétés étendues.</span><span class="sxs-lookup"><span data-stu-id="7c8cd-126">Hosts need to create a new type library that wraps the control with extended properties.</span></span>

### <a name="flags"></a><span data-ttu-id="7c8cd-127">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="7c8cd-127">Flags</span></span>

<span data-ttu-id="7c8cd-128">VARFLAG \_ FHIDDEN, FUNCFLAG \_ FHIDDEN, TYPEFLAG \_ FHIDDEN</span><span class="sxs-lookup"><span data-stu-id="7c8cd-128">VARFLAG\_FHIDDEN, FUNCFLAG\_FHIDDEN, TYPEFLAG\_FHIDDEN</span></span>

## <a name="examples"></a><span data-ttu-id="7c8cd-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="7c8cd-129">Examples</span></span>

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a><span data-ttu-id="7c8cd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c8cd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c8cd-131">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="7c8cd-131">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="7c8cd-132">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="7c8cd-132">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="7c8cd-133">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="7c8cd-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="7c8cd-134">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="7c8cd-134">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="7c8cd-135">**interface**</span><span class="sxs-lookup"><span data-stu-id="7c8cd-135">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="7c8cd-136">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="7c8cd-136">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="7c8cd-137">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="7c8cd-137">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7c8cd-138">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="7c8cd-138">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 