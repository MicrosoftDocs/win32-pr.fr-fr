---
title: defaultbind (attribut)
description: L’attribut \ defaultbind \ indique la propriété unique pouvant être liée qui représente le mieux l’objet.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- MIDL de l’attribut defaultbind
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 518c11da8d5f9b0762843c5b69292562a94b80c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031213"
---
# <a name="defaultbind-attribute"></a><span data-ttu-id="3c28c-104">defaultbind (attribut)</span><span class="sxs-lookup"><span data-stu-id="3c28c-104">defaultbind attribute</span></span>

<span data-ttu-id="3c28c-105">L’attribut **\[ defaultbind \]** indique la propriété unique pouvant être liée qui représente le mieux l’objet.</span><span class="sxs-lookup"><span data-stu-id="3c28c-105">The **\[defaultbind\]** attribute indicates the single, bindable property that best represents the object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="3c28c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c28c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c28c-107">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="3c28c-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3c28c-108">Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="3c28c-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="3c28c-109">Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="3c28c-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="3c28c-110">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="3c28c-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3c28c-111">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="3c28c-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="3c28c-112">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="3c28c-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3c28c-113">Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="3c28c-113">Specifies a list of one or more attributes that apply to the function.</span></span> <span data-ttu-id="3c28c-114">Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="3c28c-114">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="3c28c-115">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="3c28c-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="3c28c-116">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="3c28c-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="3c28c-117">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="3c28c-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3c28c-118">Spécifie le nom de la fonction à laquelle l’attribut **\[ defaultbind \]** sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="3c28c-118">Specifies the name of the function to which the **\[defaultbind\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="3c28c-119">*params*</span><span class="sxs-lookup"><span data-stu-id="3c28c-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="3c28c-120">Liste des paramètres de la fonction.</span><span class="sxs-lookup"><span data-stu-id="3c28c-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c28c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="3c28c-121">Remarks</span></span>

<span data-ttu-id="3c28c-122">Les propriétés qui ont l’attribut **\[ defaultbind \]** doivent également avoir l' **\[** attribut pouvant être [**lié**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="3c28c-122">Properties that have the **\[defaultbind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span> <span data-ttu-id="3c28c-123">Une seule propriété dans une interface ou une dispinterface peut avoir l’attribut **\[ defaultbind \]** .</span><span class="sxs-lookup"><span data-stu-id="3c28c-123">Only one property in an interface or dispinterface can have the **\[defaultbind\]** attribute.</span></span>

<span data-ttu-id="3c28c-124">Cet attribut est utilisé par les conteneurs qui ont un modèle utilisateur impliquant la liaison à un objet plutôt que la liaison à une propriété d’un objet.</span><span class="sxs-lookup"><span data-stu-id="3c28c-124">This attribute is used by containers that have a user model involving binding to an object rather than binding to a property of an object.</span></span> <span data-ttu-id="3c28c-125">Un objet peut prendre en charge la liaison de données mais ne pas avoir cet attribut.</span><span class="sxs-lookup"><span data-stu-id="3c28c-125">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="3c28c-126">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="3c28c-126">Flags</span></span>

<span data-ttu-id="3c28c-127">FUNCFLAG \_ FDEFAULTBIND, VARFLAG \_ FDEFAULTBIND</span><span class="sxs-lookup"><span data-stu-id="3c28c-127">FUNCFLAG\_FDEFAULTBIND, VARFLAG\_FDEFAULTBIND</span></span>

## <a name="examples"></a><span data-ttu-id="3c28c-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="3c28c-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="3c28c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c28c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c28c-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="3c28c-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="3c28c-131">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="3c28c-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="3c28c-132">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="3c28c-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="3c28c-133">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="3c28c-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3c28c-134">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="3c28c-134">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 