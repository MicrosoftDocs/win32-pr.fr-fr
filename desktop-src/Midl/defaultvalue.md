---
title: defaultvalue (attribut)
description: L’attribut \ DefaultValue \ vous permet de spécifier une valeur par défaut pour un paramètre facultatif typé.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- MIDL d’attribut DefaultValue
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314981"
---
# <a name="defaultvalue-attribute"></a><span data-ttu-id="69bf2-104">defaultvalue (attribut)</span><span class="sxs-lookup"><span data-stu-id="69bf2-104">defaultvalue attribute</span></span>

<span data-ttu-id="69bf2-105">L’attribut **\[ DefaultValue \]** vous permet de spécifier une valeur par défaut pour un paramètre facultatif typé.</span><span class="sxs-lookup"><span data-stu-id="69bf2-105">The **\[defaultvalue\]** attribute allows you to specify a default value for a typed optional parameter.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a><span data-ttu-id="69bf2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69bf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69bf2-107">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="69bf2-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="69bf2-108">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="69bf2-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="69bf2-109">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="69bf2-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="69bf2-110">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="69bf2-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="69bf2-111">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="69bf2-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="69bf2-112">Spécifie le nom de la fonction à laquelle l’attribut **\[ DefaultValue \]** sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="69bf2-112">Specifies the name of the function to which the **\[defaultvalue\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="69bf2-113">*obligatoire-param-List*</span><span class="sxs-lookup"><span data-stu-id="69bf2-113">*mandatory-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="69bf2-114">Spécifie un ou plusieurs paramètres obligatoires.</span><span class="sxs-lookup"><span data-stu-id="69bf2-114">Specifies on or more required parameters.</span></span>

</dd> <dt>

<span data-ttu-id="69bf2-115">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="69bf2-115">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="69bf2-116">Spécifie une liste d’un ou plusieurs attributs, séparés par des virgules, qui s’appliquent au paramètre.</span><span class="sxs-lookup"><span data-stu-id="69bf2-116">Specifies a list of one or more attributes, separated by commas, that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="69bf2-117">*Param-type*</span><span class="sxs-lookup"><span data-stu-id="69bf2-117">*param-type*</span></span> 
</dt> <dd>

<span data-ttu-id="69bf2-118">Indique le type du paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="69bf2-118">Indicates the type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="69bf2-119">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="69bf2-119">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="69bf2-120">Spécifie le nom du paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="69bf2-120">Specifies the name of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="69bf2-121">*Liste facultative-param*</span><span class="sxs-lookup"><span data-stu-id="69bf2-121">*optional-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="69bf2-122">Spécifie zéro, un ou plusieurs paramètres supplémentaires, chacun d’entre eux devant avoir une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="69bf2-122">Specifies zero or more additional parameters, each of which must have a default value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69bf2-123">Notes</span><span class="sxs-lookup"><span data-stu-id="69bf2-123">Remarks</span></span>

<span data-ttu-id="69bf2-124">La valeur par défaut que vous spécifiez pour le paramètre peut être n’importe quelle constante, ou une expression qui correspond à une constante, qui peut être représentée par un **Variant**.</span><span class="sxs-lookup"><span data-stu-id="69bf2-124">The default value you specify for the parameter can be any constant, or an expression that resolves to a constant, that can be represented by a **VARIANT**.</span></span> <span data-ttu-id="69bf2-125">Plus précisément, vous ne pouvez pas appliquer l’attribut **\[ \] DefaultValue** à un paramètre qui est une structure, un tableau ou un type **SAFEARRAY** .</span><span class="sxs-lookup"><span data-stu-id="69bf2-125">Specifically, you cannot apply the **\[defaultvalue\]** attribute to a parameter that is a structure, an array, or a **SAFEARRAY** type.</span></span>

<span data-ttu-id="69bf2-126">Le compilateur MIDL accepte l’ordonnancement des paramètres suivant (de gauche à droite) :</span><span class="sxs-lookup"><span data-stu-id="69bf2-126">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="69bf2-127">Paramètres obligatoires (paramètres qui n’ont pas les attributs **\[ DefaultValue \]** ou **\[** [**facultatifs**](optional.md) **\]** )</span><span class="sxs-lookup"><span data-stu-id="69bf2-127">Required parameters (parameters that do not have the **\[defaultvalue\]** or **\[**[**optional**](optional.md)**\]** attributes),</span></span>
2.  <span data-ttu-id="69bf2-128">paramètres facultatifs avec ou sans l’attribut **\[ DefaultValue \]** ,</span><span class="sxs-lookup"><span data-stu-id="69bf2-128">optional parameters with or without the **\[defaultvalue\]** attribute,</span></span>
3.  <span data-ttu-id="69bf2-129">paramètres avec l’attribut **\[ facultatif \]** et sans l’attribut **\[ DefaultValue \]** ,</span><span class="sxs-lookup"><span data-stu-id="69bf2-129">parameters with the **\[optional\]** attribute and without the **\[defaultvalue\]** attribute,</span></span>
4.  <span data-ttu-id="69bf2-130">**\[** paramètre [**LCID**](lcid.md) **\]** , le cas échéant,</span><span class="sxs-lookup"><span data-stu-id="69bf2-130">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="69bf2-131">**\[**[**retVal**](retval.md) **\]** paramètre</span><span class="sxs-lookup"><span data-stu-id="69bf2-131">**\[**[**retval**](retval.md)**\]** parameter</span></span>

## <a name="examples"></a><span data-ttu-id="69bf2-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="69bf2-132">Examples</span></span>

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a><span data-ttu-id="69bf2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69bf2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69bf2-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="69bf2-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="69bf2-135">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="69bf2-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="69bf2-136">**interface**</span><span class="sxs-lookup"><span data-stu-id="69bf2-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="69bf2-137">**LCID**</span><span class="sxs-lookup"><span data-stu-id="69bf2-137">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="69bf2-138">**facultatif**</span><span class="sxs-lookup"><span data-stu-id="69bf2-138">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="69bf2-139">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="69bf2-139">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="69bf2-140">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="69bf2-140">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="69bf2-141">**retval**</span><span class="sxs-lookup"><span data-stu-id="69bf2-141">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="69bf2-142">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="69bf2-142">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 