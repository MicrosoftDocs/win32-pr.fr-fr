---
title: attribut HelpString
description: L’attribut \ HelpString \ spécifie une chaîne de caractères utilisée pour décrire l’élément auquel il s’applique.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- attribut HelpString MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940880"
---
# <a name="helpstring-attribute"></a><span data-ttu-id="4182a-104">attribut HelpString</span><span class="sxs-lookup"><span data-stu-id="4182a-104">helpstring attribute</span></span>

<span data-ttu-id="4182a-105">L’attribut **\[ helpString \]** spécifie une chaîne de caractères utilisée pour décrire l’élément auquel il s’applique.</span><span class="sxs-lookup"><span data-stu-id="4182a-105">The **\[helpstring\]** attribute specifies a character string that is used to describe the element to which it applies.</span></span> <span data-ttu-id="4182a-106">Vous pouvez appliquer l’attribut **\[ helpString \]** aux instructions Library, importlib, interface, dispinterface, module ou coclass, typedefs, propriétés et méthodes.</span><span class="sxs-lookup"><span data-stu-id="4182a-106">You can apply the **\[helpstring\]** attribute to library, importlib, interface, dispinterface, module, or coclass statements, typedefs, properties, and methods.</span></span>

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a><span data-ttu-id="4182a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4182a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4182a-108">*Help-Text-String*</span><span class="sxs-lookup"><span data-stu-id="4182a-108">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="4182a-109">Chaîne de caractères se terminant par zéro qui contient le texte d’aide.</span><span class="sxs-lookup"><span data-stu-id="4182a-109">A zero-terminated string of characters containing help text.</span></span>

</dd> <dt>

<span data-ttu-id="4182a-110">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4182a-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4182a-111">Zéro, une ou plusieurs instructions d’attribut MIDL.</span><span class="sxs-lookup"><span data-stu-id="4182a-111">Zero or more MIDL attribute statements.</span></span>

</dd> <dt>

<span data-ttu-id="4182a-112">*appartient*</span><span class="sxs-lookup"><span data-stu-id="4182a-112">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="4182a-113">L’une des directives suivantes : [**Library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **Method**, **Property** ou [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="4182a-113">One of the following directives: [**library**](library.md), **\[**[**importlib**](importlib.md)**\]**, [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="4182a-114">*nom de l’élément*</span><span class="sxs-lookup"><span data-stu-id="4182a-114">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4182a-115">Nom que d’autres composants logiciels peuvent utiliser pour décourber l’élément actuel</span><span class="sxs-lookup"><span data-stu-id="4182a-115">The name that other software components can use to delineate the current element</span></span>

</dd> <dt>

<span data-ttu-id="4182a-116">*définition*</span><span class="sxs-lookup"><span data-stu-id="4182a-116">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="4182a-117">Spécifie les instructions qui composent la définition de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4182a-117">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="4182a-118">*IDL-Statement*</span><span class="sxs-lookup"><span data-stu-id="4182a-118">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="4182a-119">Une instruction de définition d’interface MIDL telle que [**propget**](propget.md) ou [**propput**](propput.md).</span><span class="sxs-lookup"><span data-stu-id="4182a-119">A MIDL interface definition statement such as [**propget**](propget.md) or [**propput**](propput.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4182a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4182a-120">Remarks</span></span>

<span data-ttu-id="4182a-121">Utilisez les fonctions [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) dans les interfaces [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) et [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) pour récupérer la chaîne d’aide.</span><span class="sxs-lookup"><span data-stu-id="4182a-121">Use the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="4182a-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="4182a-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a><span data-ttu-id="4182a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4182a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4182a-124">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="4182a-124">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="4182a-125">**importlib**</span><span class="sxs-lookup"><span data-stu-id="4182a-125">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="4182a-126">**interface**</span><span class="sxs-lookup"><span data-stu-id="4182a-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="4182a-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="4182a-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="4182a-128">**modules**</span><span class="sxs-lookup"><span data-stu-id="4182a-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="4182a-129">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="4182a-129">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="4182a-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="4182a-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="4182a-131">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="4182a-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4182a-132">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="4182a-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4182a-133">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="4182a-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 