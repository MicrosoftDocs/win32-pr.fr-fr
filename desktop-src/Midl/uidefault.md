---
title: uidefault (attribut)
description: L’attribut \ UIDefault \ indique que le membre des informations de type est le membre par défaut à afficher dans l’interface utilisateur.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- MIDL de l’attribut UIDefault
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381810"
---
# <a name="uidefault-attribute"></a><span data-ttu-id="ec362-104">uidefault (attribut)</span><span class="sxs-lookup"><span data-stu-id="ec362-104">uidefault attribute</span></span>

<span data-ttu-id="ec362-105">L’attribut **\[ UIDefault \]** indique que le membre d’informations de type est le membre par défaut à afficher dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ec362-105">The **\[uidefault\]** attribute indicates that the type information member is the default member for display in the user interface.</span></span>

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="ec362-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec362-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec362-107">*méthode-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ec362-107">*method-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ec362-108">Autres attributs qui s’appliquent à la méthode.</span><span class="sxs-lookup"><span data-stu-id="ec362-108">Other attributes that apply to the method.</span></span>

</dd> <dt>

<span data-ttu-id="ec362-109">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="ec362-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ec362-110">Type des données retournées par la méthode à la fin de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ec362-110">The type of the data that the method will return when it finishes execution.</span></span>

</dd> <dt>

<span data-ttu-id="ec362-111">*nom de méthode*</span><span class="sxs-lookup"><span data-stu-id="ec362-111">*method-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ec362-112">Nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ec362-112">The name of the method.</span></span>

</dd> <dt>

<span data-ttu-id="ec362-113">*méthode-parameter-list*</span><span class="sxs-lookup"><span data-stu-id="ec362-113">*method-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ec362-114">Zéro, un ou plusieurs paramètres pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="ec362-114">Zero or more parameters for the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec362-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ec362-115">Remarks</span></span>

<span data-ttu-id="ec362-116">L’application de l’attribut **\[ UIDefault \]** à un membre d’une interface ou d’une dispinterface indique Visual Basic, au moment du design, d’afficher automatiquement cet événement ou cette propriété à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ec362-116">Applying the **\[uidefault\]** attribute to a member of an interface or a dispinterface tells Visual Basic, at design-time, to automatically display this event or property to the user.</span></span> <span data-ttu-id="ec362-117">Cela signifie que lorsque l’utilisateur double-clique sur un objet, Visual Basic passe à l’événement dans l’interface source par défaut qui a l’attribut **\[ UIDefault \]** .</span><span class="sxs-lookup"><span data-stu-id="ec362-117">This means that when the user double-clicks an object, Visual Basic jumps to the event in the default source interface that has the **\[uidefault\]** attribute.</span></span> <span data-ttu-id="ec362-118">Quand l’utilisateur sélectionne un objet, l’Explorateur de propriétés de Visual Basic affiche la propriété dans l’interface source par défaut qui a cet attribut.</span><span class="sxs-lookup"><span data-stu-id="ec362-118">When the user selects an object, Visual Basic's Properties browser displays the property in the default source interface that has this attribute.</span></span> <span data-ttu-id="ec362-119">Si aucun événement ou propriété n’a l’attribut **\[ uidefault \]** , Visual Basic affiche le premier événement ou la première propriété figurant dans l’interface par défaut.</span><span class="sxs-lookup"><span data-stu-id="ec362-119">If no event or property has the **\[uidefault\]** attribute, Visual Basic displays the first event or property listed in the default interface.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="ec362-120">Représentation TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="ec362-120">Typeflag Representation</span></span>

<span data-ttu-id="ec362-121">Présence de FUNCFLAG \_ FUIDEFAULT ou VARFLAG \_ FUIDEFAULT</span><span class="sxs-lookup"><span data-stu-id="ec362-121">The presence of FUNCFLAG\_FUIDEFAULT or VARFLAG\_FUIDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="ec362-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="ec362-122">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="ec362-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec362-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec362-124">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="ec362-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="ec362-125">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="ec362-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="ec362-126">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="ec362-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 