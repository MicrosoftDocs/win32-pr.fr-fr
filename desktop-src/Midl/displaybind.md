---
title: displaybind (attribut)
description: L’attribut \ displaybind \ indique une propriété qui doit être affichée à l’utilisateur comme pouvant être liée.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- MIDL de l’attribut DisplayBind
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725436"
---
# <a name="displaybind-attribute"></a><span data-ttu-id="33c03-104">displaybind (attribut)</span><span class="sxs-lookup"><span data-stu-id="33c03-104">displaybind attribute</span></span>

<span data-ttu-id="33c03-105">L’attribut **\[ displaybind \]** indique une propriété qui doit être affichée à l’utilisateur comme pouvant être liée.</span><span class="sxs-lookup"><span data-stu-id="33c03-105">The **\[displaybind\]** attribute indicates a property that should be displayed to the user as bindable.</span></span>

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="33c03-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33c03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c03-107">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="33c03-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="33c03-108">Spécifie une liste facultative d’attributs d’interface.</span><span class="sxs-lookup"><span data-stu-id="33c03-108">Specifies an optional list of interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="33c03-109">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="33c03-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="33c03-110">Nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="33c03-110">The name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="33c03-111">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="33c03-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="33c03-112">Spécifie une liste d’un ou plusieurs attributs, séparés par des virgules, qui s’appliquent au type de retour de fonction.</span><span class="sxs-lookup"><span data-stu-id="33c03-112">Specifies a list of one or more attributes, separated by commas, that apply to the function-return type.</span></span>

</dd> <dt>

<span data-ttu-id="33c03-113">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="33c03-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="33c03-114">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="33c03-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="33c03-115">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="33c03-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="33c03-116">Spécifie le nom de la fonction à laquelle l’attribut **\[ displaybind \]** sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="33c03-116">Specifies the name of the function to which the **\[displaybind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="33c03-117">*params*</span><span class="sxs-lookup"><span data-stu-id="33c03-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="33c03-118">Liste des paramètres de la fonction.</span><span class="sxs-lookup"><span data-stu-id="33c03-118">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33c03-119">Notes</span><span class="sxs-lookup"><span data-stu-id="33c03-119">Remarks</span></span>

<span data-ttu-id="33c03-120">Les propriétés qui ont l’attribut **\[ displaybind \]** doivent également avoir l' **\[** attribut pouvant être [**lié**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="33c03-120">Properties that have the **\[displaybind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="33c03-121">Un objet peut prendre en charge la liaison de données mais ne pas avoir cet attribut.</span><span class="sxs-lookup"><span data-stu-id="33c03-121">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="33c03-122">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="33c03-122">Flags</span></span>

<span data-ttu-id="33c03-123">FUNCFLAG \_ FDISPLAYBIND, VARFLAG \_ FDISPLAYBIND</span><span class="sxs-lookup"><span data-stu-id="33c03-123">FUNCFLAG\_FDISPLAYBIND, VARFLAG\_FDISPLAYBIND</span></span>

## <a name="examples"></a><span data-ttu-id="33c03-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="33c03-124">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="33c03-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33c03-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c03-126">**bindable**</span><span class="sxs-lookup"><span data-stu-id="33c03-126">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="33c03-127">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="33c03-127">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="33c03-128">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="33c03-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="33c03-129">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="33c03-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="33c03-130">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="33c03-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 