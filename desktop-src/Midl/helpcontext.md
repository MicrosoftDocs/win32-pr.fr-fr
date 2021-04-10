---
title: helpcontext (attribut)
description: L’attribut \ HelpContext \ spécifie un identificateur de contexte qui permet à l’utilisateur d’afficher des informations sur cet élément dans le fichier d’aide.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- l’attribut HelpContext MIDL
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940893"
---
# <a name="helpcontext-attribute"></a><span data-ttu-id="ef374-104">helpcontext (attribut)</span><span class="sxs-lookup"><span data-stu-id="ef374-104">helpcontext attribute</span></span>

<span data-ttu-id="ef374-105">L' \[ attribut **HelpContext** \] spécifie un identificateur de contexte qui permet à l’utilisateur d’afficher des informations sur cet élément dans le fichier d’aide.</span><span class="sxs-lookup"><span data-stu-id="ef374-105">The \[**helpcontext**\] attribute specifies a context identifier that lets the user view information about this element in the Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a><span data-ttu-id="ef374-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef374-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef374-107">*UUID-Number*</span><span class="sxs-lookup"><span data-stu-id="ef374-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="ef374-108">Spécifie un numéro d’identification unique universel pour la [**bibliothèque**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **Methods**, **\[ Property \]** ou [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="ef374-108">Specifies a universally unique identification number for the [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **methods**, **\[property\]**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef374-109">*HelpContext-valeur*</span><span class="sxs-lookup"><span data-stu-id="ef374-109">*helpcontext-value*</span></span> 
</dt> <dd>

<span data-ttu-id="ef374-110">Entier unique qui identifie le texte d’aide associé à l’élément MIDL actuel.</span><span class="sxs-lookup"><span data-stu-id="ef374-110">A unique integer that identifies the help text associated with the current MIDL element.</span></span>

</dd> <dt>

<span data-ttu-id="ef374-111">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="ef374-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ef374-112">Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à l’élément MIDL dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="ef374-112">Specifies a list of one or more attributes that apply to the MIDL element as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="ef374-113">*appartient*</span><span class="sxs-lookup"><span data-stu-id="ef374-113">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="ef374-114">L’une des directives suivantes : [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="ef374-114">One of the following directives: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef374-115">*nom de l’élément*</span><span class="sxs-lookup"><span data-stu-id="ef374-115">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ef374-116">Nom que d’autres composants logiciels peuvent utiliser pour décourber l’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="ef374-116">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="ef374-117">*Description*</span><span class="sxs-lookup"><span data-stu-id="ef374-117">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="ef374-118">Spécifie les instructions qui composent la définition de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ef374-118">Specifies statements that make up the element definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef374-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ef374-119">Remarks</span></span>

<span data-ttu-id="ef374-120">L' \[ **attribut HelpContext** \] peut être appliqué aux éléments suivants : [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="ef374-120">The \[**helpcontext**\] attribute can be applied to the following elements: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

<span data-ttu-id="ef374-121">La *valeur HelpContext* est un identificateur de contexte 32 bits dans le fichier d’aide qui peut être récupéré avec les fonctions [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) dans les interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) et [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) .</span><span class="sxs-lookup"><span data-stu-id="ef374-121">The *helpcontext-value* is a 32-bit context identifier within the Help file that can be retrieved with the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="ef374-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="ef374-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="ef374-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef374-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef374-124">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="ef374-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="ef374-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="ef374-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="ef374-126">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="ef374-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="ef374-127">**importlib**</span><span class="sxs-lookup"><span data-stu-id="ef374-127">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="ef374-128">**interface**</span><span class="sxs-lookup"><span data-stu-id="ef374-128">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="ef374-129">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="ef374-129">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="ef374-130">**modules**</span><span class="sxs-lookup"><span data-stu-id="ef374-130">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="ef374-131">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="ef374-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="ef374-132">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="ef374-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="ef374-133">**typedef**</span><span class="sxs-lookup"><span data-stu-id="ef374-133">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 