---
title: retval (attribut)
description: L’attribut \ retval \ désigne le paramètre qui reçoit la valeur de retour du membre.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- attribut retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842130"
---
# <a name="retval-attribute"></a><span data-ttu-id="1c606-104">retval (attribut)</span><span class="sxs-lookup"><span data-stu-id="1c606-104">retval attribute</span></span>

<span data-ttu-id="1c606-105">L’attribut **\[ retval \]** désigne le paramètre qui reçoit la valeur de retour du membre.</span><span class="sxs-lookup"><span data-stu-id="1c606-105">The **\[retval\]** attribute designates the parameter that receives the return value of the member.</span></span>

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a><span data-ttu-id="1c606-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c606-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c606-107">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="1c606-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1c606-108">Type de données de la valeur de retour de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="1c606-108">The data type of the return value of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="1c606-109">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="1c606-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1c606-110">Nom utilisé pour appeler la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="1c606-110">The name used to invoke the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="1c606-111">*attributs facultatifs*</span><span class="sxs-lookup"><span data-stu-id="1c606-111">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="1c606-112">Zéro, un ou plusieurs attributs MIDL.</span><span class="sxs-lookup"><span data-stu-id="1c606-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="1c606-113">*type de données*</span><span class="sxs-lookup"><span data-stu-id="1c606-113">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="1c606-114">Type des données passées via le paramètre.</span><span class="sxs-lookup"><span data-stu-id="1c606-114">The type of the data passed through the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1c606-115">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="1c606-115">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1c606-116">Nom de l’identificateur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="1c606-116">The identifier name of the parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c606-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1c606-117">Remarks</span></span>

<span data-ttu-id="1c606-118">Vous pouvez utiliser l’attribut **\[ retval \]** sur les paramètres des membres d’interface qui décrivent des méthodes ou obtiennent des propriétés.</span><span class="sxs-lookup"><span data-stu-id="1c606-118">You can use the **\[retval\]** attribute on parameters of interface members that describe methods or get properties.</span></span> <span data-ttu-id="1c606-119">(L’attribut est requis sur le dernier paramètre d’une méthode qui a le **\[** [**propget**](propget.md) **\]** attribut.) Le paramètre doit avoir l' **\[** attribut [**out**](out-idl.md) **\]** et doit être un type pointeur.</span><span class="sxs-lookup"><span data-stu-id="1c606-119">(The attribute is required on the last parameter of a method that has the **\[**[**propget**](propget.md)**\]** attribute.) The parameter must have the **\[**[**out**](out-idl.md)**\]** attribute and must be a pointer type.</span></span>

<span data-ttu-id="1c606-120">Vous ne pouvez pas appliquer l' **\[** attribut [**facultatif**](optional.md) **\]** à un paramètre **\[ \] retVal** .</span><span class="sxs-lookup"><span data-stu-id="1c606-120">You cannot apply the **\[**[**optional**](optional.md)**\]** attribute to a **\[retval\]** parameter.</span></span>

<span data-ttu-id="1c606-121">Le compilateur MIDL accepte l’ordonnancement des paramètres suivant (de gauche à droite) :</span><span class="sxs-lookup"><span data-stu-id="1c606-121">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="1c606-122">Paramètres obligatoires (paramètres qui n’ont pas les **\[** attributs [**DefaultValue**](defaultvalue.md) **\]** ou **\[** [**Optional**](optional.md) **\]** ).</span><span class="sxs-lookup"><span data-stu-id="1c606-122">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[**[**optional**](optional.md)**\]** attributes).</span></span>
2.  <span data-ttu-id="1c606-123">Paramètres facultatifs avec ou sans l' **\[** [](defaultvalue.md) **\]** attribut DefaultValue.</span><span class="sxs-lookup"><span data-stu-id="1c606-123">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
3.  <span data-ttu-id="1c606-124">Paramètres avec l' **\[** attribut [**facultatif**](optional.md) **\]** et sans l' **\[** attribut [**DefaultValue**](defaultvalue.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="1c606-124">Parameters with the **\[**[**optional**](optional.md)**\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
4.  <span data-ttu-id="1c606-125">**\[** paramètre [**LCID**](lcid.md) **\]** , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1c606-125">**\[**[**lcid**](lcid.md)**\]** parameter, if any.</span></span>
5.  <span data-ttu-id="1c606-126">paramètre **\[ retval \]** .</span><span class="sxs-lookup"><span data-stu-id="1c606-126">**\[retval\]** parameter.</span></span>

<span data-ttu-id="1c606-127">Les paramètres avec l’attribut **\[ retval \]** ne sont pas affichés dans les navigateurs orientés utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c606-127">Parameters with the **\[retval\]** attribute are not displayed in user-oriented browsers.</span></span>

### <a name="flags"></a><span data-ttu-id="1c606-128">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="1c606-128">Flags</span></span>

<span data-ttu-id="1c606-129">IDLFLAG \_ FRETVAL</span><span class="sxs-lookup"><span data-stu-id="1c606-129">IDLFLAG\_FRETVAL</span></span>

## <a name="examples"></a><span data-ttu-id="1c606-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="1c606-130">Examples</span></span>

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a><span data-ttu-id="1c606-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c606-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c606-132">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="1c606-132">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="1c606-133">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="1c606-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="1c606-134">**LCID**</span><span class="sxs-lookup"><span data-stu-id="1c606-134">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="1c606-135">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="1c606-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="1c606-136">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="1c606-136">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="1c606-137">**facultatif**</span><span class="sxs-lookup"><span data-stu-id="1c606-137">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="1c606-138">**à**</span><span class="sxs-lookup"><span data-stu-id="1c606-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="1c606-139">**propget**</span><span class="sxs-lookup"><span data-stu-id="1c606-139">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="1c606-140">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="1c606-140">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 