---
title: defaultcollelem (attribut)
description: L’attribut \ defaultcollelem \ signale une propriété comme fonction d’accesseur pour un élément de la collection par défaut.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- MIDL de l’attribut defaultcollelem
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031186"
---
# <a name="defaultcollelem-attribute"></a><span data-ttu-id="fd4b5-104">defaultcollelem (attribut)</span><span class="sxs-lookup"><span data-stu-id="fd4b5-104">defaultcollelem attribute</span></span>

<span data-ttu-id="fd4b5-105">L’attribut **\[ defaultcollelem \]** signale une propriété comme fonction d’accesseur pour un élément de la collection par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-105">The **\[defaultcollelem\]** attribute flags a property as an accessor function for an element of the default collection.</span></span>

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="fd4b5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd4b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd4b5-107">*property-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="fd4b5-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fd4b5-108">Autres attributs qui s’appliquent à la propriété.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="fd4b5-109">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="fd4b5-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="fd4b5-110">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="fd4b5-111">*nom de la propriété*</span><span class="sxs-lookup"><span data-stu-id="fd4b5-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fd4b5-112">Nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-112">The name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="fd4b5-113">*prop-param-List*</span><span class="sxs-lookup"><span data-stu-id="fd4b5-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fd4b5-114">Liste de zéro ou plusieurs paramètres associés à la propriété.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-114">A list of zero or more parameters associated with the property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd4b5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fd4b5-115">Remarks</span></span>

<span data-ttu-id="fd4b5-116">L’attribut **\[ defaultcollelem \]** est utilisé pour l’optimisation du code® Visual BasicÂ.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-116">The **\[defaultcollelem\]** attribute is used for Visual BasicÂ® code optimization.</span></span> <span data-ttu-id="fd4b5-117">Si un membre d’une interface ou d’une dispinterface est marqué comme fonction d’accesseur, l’appel passera directement à ce membre.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-117">If a member of an interface or dispinterface is flagged as an accessor function, then the call will go directly to that member.</span></span>

<span data-ttu-id="fd4b5-118">L’utilisation de **\[ defaultcollelem \]** doit être cohérente pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-118">Use of **\[defaultcollelem\]** must be consistent for a property.</span></span> <span data-ttu-id="fd4b5-119">Par exemple, si vous utilisez l’attribut sur une propriété *obtenir* , il doit également être présent sur une propriété *Let* .</span><span class="sxs-lookup"><span data-stu-id="fd4b5-119">For example, if you use the attribute on a *Get* property, it must also be present on a *Let* property.</span></span>

### <a name="typeflags-representation"></a><span data-ttu-id="fd4b5-120">Représentation TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="fd4b5-120">Typeflags Representation</span></span>

<span data-ttu-id="fd4b5-121">Présence de FUNCFLAG \_ FDEFAULTCOLLELEM ou VARFLAG \_ FDEFAULTCOLLELEM.</span><span class="sxs-lookup"><span data-stu-id="fd4b5-121">The presence of FUNCFLAG\_FDEFAULTCOLLELEM or VARFLAG\_FDEFAULTCOLLELEM.</span></span>

## <a name="examples"></a><span data-ttu-id="fd4b5-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="fd4b5-122">Examples</span></span>

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a><span data-ttu-id="fd4b5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd4b5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd4b5-124">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="fd4b5-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="fd4b5-125">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="fd4b5-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="fd4b5-126">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="fd4b5-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 