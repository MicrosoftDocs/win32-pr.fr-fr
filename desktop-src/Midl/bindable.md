---
title: bindable (attribut)
description: L’attribut \ Binder \ indique que la propriété prend en charge la liaison de données.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- MIDL d’attribut pouvant être lié
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509649"
---
# <a name="bindable-attribute"></a><span data-ttu-id="4fd3a-104">bindable (attribut)</span><span class="sxs-lookup"><span data-stu-id="4fd3a-104">bindable attribute</span></span>

<span data-ttu-id="4fd3a-105">L’attribut **\[ pouvant \] être lié** indique que la propriété prend en charge la liaison de données.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-105">The **\[bindable\]** attribute indicates that the property supports data binding.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="4fd3a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fd3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fd3a-107">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="4fd3a-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd3a-108">Spécifie une liste de zéro ou plusieurs attributs IDL qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="4fd3a-109">Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="4fd3a-110">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="4fd3a-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd3a-111">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="4fd3a-112">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="4fd3a-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd3a-113">Spécifie zéro, un ou plusieurs attributs qui s’appliquent au prototype de fonction pour une propriété ou une méthode dans une [**interface**](interface.md) ou une [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="4fd3a-113">Specifies zero or more attributes that apply to the function prototype for a property or a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span> <span data-ttu-id="4fd3a-114">Les attributs suivants sont valides : [**\[ \] helpString**](helpstring.md), [**\[ \] HelpContext**](helpcontext.md), [**\[ String \]**](string.md), [**\[ defaultbind \]**](defaultbind.md), [**\[ displaybind \]**](displaybind.md), [**\[ immediatebind \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ propput \]**](propput.md), [**\[ PROPPUTREF \]**](propputref.md)et [**\[ vararg \]**](vararg.md).</span><span class="sxs-lookup"><span data-stu-id="4fd3a-114">The following attributes are valid: [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[string\]**](string.md), [**\[defaultbind\]**](defaultbind.md), [**\[displaybind\]**](displaybind.md), [**\[immediatebind\]**](immediatebind.md), [**\[propget\]**](propget.md), [**\[propput\]**](propput.md), [**\[propputref\]**](propputref.md), and [**\[vararg\]**](vararg.md).</span></span> <span data-ttu-id="4fd3a-115">Si **vararg** est spécifié, le dernier paramètre doit être un tableau sécurisé de type Variant.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-115">If **vararg** is specified, the last parameter must be a safe array of type VARIANT.</span></span> <span data-ttu-id="4fd3a-116">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="4fd3a-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="4fd3a-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd3a-118">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="4fd3a-119">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="4fd3a-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd3a-120">Spécifie le nom de la fonction à laquelle l’attribut **\[ pouvant être lié \]** sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-120">Specifies the name of the function to which the **\[bindable\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="4fd3a-121">*params*</span><span class="sxs-lookup"><span data-stu-id="4fd3a-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd3a-122">Liste des paramètres de la fonction.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fd3a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4fd3a-123">Remarks</span></span>

<span data-ttu-id="4fd3a-124">En prenant en charge la liaison de données, l’attribut **\[ pouvant être lié \]** permet au client d’être averti chaque fois qu’une propriété a une valeur modifiée.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-124">By supporting data binding, the **\[bindable\]** attribute allows the client to be notified whenever a property has changed value.</span></span> <span data-ttu-id="4fd3a-125">(Si vous souhaitez que le client soit averti des modifications imminentes apportées à une propriété, utilisez l’attribut [**\[ modification \]**](requestedit.md) .)</span><span class="sxs-lookup"><span data-stu-id="4fd3a-125">(If you want the client to be notified of impending changes to a property, use the [**\[requestedit\]**](requestedit.md) attribute.)</span></span>

<span data-ttu-id="4fd3a-126">Étant donné que l’attribut **\[ pouvant être lié \]** fait référence à la propriété dans son ensemble, il doit être spécifié partout où la propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-126">Because the **\[bindable\]** attribute refers to the property as a whole, it must be specified wherever the property is defined.</span></span> <span data-ttu-id="4fd3a-127">Par conséquent, vous devez spécifier l’attribut à la fois sur la fonction d’accès à la propriété et la fonction de définition de propriété.</span><span class="sxs-lookup"><span data-stu-id="4fd3a-127">Therefore, you need to specify the attribute on both the property-accessing function and the property-setting function.</span></span>

### <a name="flags"></a><span data-ttu-id="4fd3a-128">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="4fd3a-128">Flags</span></span>

<span data-ttu-id="4fd3a-129">FUNCFLAG \_ FBINDABLE, VARFLAG \_ FBINDABLE</span><span class="sxs-lookup"><span data-stu-id="4fd3a-129">FUNCFLAG\_FBINDABLE, VARFLAG\_FBINDABLE</span></span>

## <a name="examples"></a><span data-ttu-id="4fd3a-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="4fd3a-130">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="4fd3a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fd3a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd3a-132">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-132">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-134">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-134">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-135">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="4fd3a-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-136">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-136">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-137">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-137">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-138">**immediatebind**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-138">**immediatebind**</span></span>](immediatebind.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-139">**interface**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-139">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-140">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="4fd3a-140">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4fd3a-141">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="4fd3a-141">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4fd3a-142">**propget**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-142">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-143">**propput**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-143">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-144">**propputref**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-144">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-145">**requestedit**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-145">**requestedit**</span></span>](requestedit.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-146">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="4fd3a-147">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="4fd3a-147">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="4fd3a-148">**vararg**</span><span class="sxs-lookup"><span data-stu-id="4fd3a-148">**vararg**</span></span>](vararg.md)
</dt> </dl>

 

 