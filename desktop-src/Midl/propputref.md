---
title: propputref (attribut)
description: L’attribut \ propputref \ spécifie une fonction de définition de propriété qui utilise une référence au lieu d’une valeur.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- propputref, attribut MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940867"
---
# <a name="propputref-attribute"></a><span data-ttu-id="00fd6-104">propputref (attribut)</span><span class="sxs-lookup"><span data-stu-id="00fd6-104">propputref attribute</span></span>

<span data-ttu-id="00fd6-105">L’attribut **\[ PROPPUTREF \]** spécifie une fonction de définition de propriété qui utilise une référence au lieu d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="00fd6-105">The **\[propputref\]** attribute specifies a property-setting function that uses a reference instead of a value.</span></span>

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="00fd6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00fd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00fd6-107">*attributs facultatifs*</span><span class="sxs-lookup"><span data-stu-id="00fd6-107">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="00fd6-108">Zéro, un ou plusieurs attributs de propriété.</span><span class="sxs-lookup"><span data-stu-id="00fd6-108">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="00fd6-109">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="00fd6-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="00fd6-110">Type des données retournées par la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="00fd6-110">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="00fd6-111">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="00fd6-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="00fd6-112">Nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="00fd6-112">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="00fd6-113">*parameters*</span><span class="sxs-lookup"><span data-stu-id="00fd6-113">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="00fd6-114">Zéro, un ou plusieurs paramètres à la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="00fd6-114">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00fd6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="00fd6-115">Remarks</span></span>

<span data-ttu-id="00fd6-116">Une fonction qui a l’attribut **\[ PROPPUTREF \]** doit également avoir, en tant que dernier paramètre, un pointeur qui a l' **\[** attribut [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="00fd6-116">A function that has the **\[propputref\]** attribute must also have, as its last parameter, a pointer that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="00fd6-117">La propriété doit avoir le même nom que la fonction.</span><span class="sxs-lookup"><span data-stu-id="00fd6-117">The property must have the same name as the function.</span></span> <span data-ttu-id="00fd6-118">Au maximum, l’un des **\[** attributs [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** et **\[ PROPPUTREF \]** peut être spécifié pour une fonction.</span><span class="sxs-lookup"><span data-stu-id="00fd6-118">At most, one of **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]** and **\[propputref\]** attributes can be specified for a function.</span></span>

### <a name="flags"></a><span data-ttu-id="00fd6-119">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="00fd6-119">Flags</span></span>

<span data-ttu-id="00fd6-120">APPELER \_ PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="00fd6-120">INVOKE\_PROPERTYPUTREF</span></span>

## <a name="examples"></a><span data-ttu-id="00fd6-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="00fd6-121">Examples</span></span>

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a><span data-ttu-id="00fd6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00fd6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00fd6-123">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="00fd6-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="00fd6-124">**in**</span><span class="sxs-lookup"><span data-stu-id="00fd6-124">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="00fd6-125">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="00fd6-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="00fd6-126">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="00fd6-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="00fd6-127">**propget**</span><span class="sxs-lookup"><span data-stu-id="00fd6-127">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="00fd6-128">**propput**</span><span class="sxs-lookup"><span data-stu-id="00fd6-128">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="00fd6-129">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="00fd6-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 