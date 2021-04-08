---
title: optional (attribut)
description: L’attribut \ Optional spécifie un paramètre facultatif pour une fonction membre.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- MIDL d’attribut facultatif
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842262"
---
# <a name="optional-attribute"></a><span data-ttu-id="7b1b8-104">optional (attribut)</span><span class="sxs-lookup"><span data-stu-id="7b1b8-104">optional attribute</span></span>

<span data-ttu-id="7b1b8-105">L’attribut **\[ facultatif \]** spécifie un paramètre facultatif pour une fonction membre.</span><span class="sxs-lookup"><span data-stu-id="7b1b8-105">The **\[optional\]** attribute specifies an optional parameter for a member function.</span></span>

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a><span data-ttu-id="7b1b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b1b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b1b8-107">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="7b1b8-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7b1b8-108">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="7b1b8-108">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7b1b8-109">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="7b1b8-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7b1b8-110">Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="7b1b8-110">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="7b1b8-111">*autres attributs*</span><span class="sxs-lookup"><span data-stu-id="7b1b8-111">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7b1b8-112">Zéro, un ou plusieurs attributs MIDL facultatifs.</span><span class="sxs-lookup"><span data-stu-id="7b1b8-112">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="7b1b8-113">*type de paramètre*</span><span class="sxs-lookup"><span data-stu-id="7b1b8-113">*parameter-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7b1b8-114">Type de données du paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="7b1b8-114">The data type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7b1b8-115">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="7b1b8-115">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7b1b8-116">Spécifie le nom du paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="7b1b8-116">Specifies the name of the optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b1b8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7b1b8-117">Remarks</span></span>

<span data-ttu-id="7b1b8-118">L’attribut **\[ facultatif \]** est valide uniquement si le paramètre est de type **Variant** ou **Variant** \* .</span><span class="sxs-lookup"><span data-stu-id="7b1b8-118">The **\[optional\]** attribute is valid only if the parameter is of type **VARIANT** or **VARIANT** Â \*.</span></span>

<span data-ttu-id="7b1b8-119">Le compilateur MIDL accepte l’ordonnancement des paramètres suivant (de gauche à droite) :</span><span class="sxs-lookup"><span data-stu-id="7b1b8-119">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="7b1b8-120">Paramètres obligatoires (paramètres qui n’ont pas les **\[** attributs [**DefaultValue**](defaultvalue.md) **\]** ou **\[ facultatifs \]** )</span><span class="sxs-lookup"><span data-stu-id="7b1b8-120">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[optional\]** attributes),</span></span>
2.  <span data-ttu-id="7b1b8-121">Paramètres facultatifs avec ou sans l' **\[** [](defaultvalue.md) **\]** attribut DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="7b1b8-121">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
3.  <span data-ttu-id="7b1b8-122">Paramètres avec l’attribut **\[ facultatif \]** et sans l' **\[** attribut [**DefaultValue**](defaultvalue.md) **\]** ,</span><span class="sxs-lookup"><span data-stu-id="7b1b8-122">Parameters with the **\[optional\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
4.  <span data-ttu-id="7b1b8-123">**\[** paramètre [**LCID**](lcid.md) **\]** , le cas échéant,</span><span class="sxs-lookup"><span data-stu-id="7b1b8-123">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="7b1b8-124">**\[**[**retVal**](retval.md) **\]** paramètre</span><span class="sxs-lookup"><span data-stu-id="7b1b8-124">**\[**[**retval**](retval.md)**\]** parameter</span></span>

<span data-ttu-id="7b1b8-125">Vous ne pouvez pas appliquer l’attribut **\[ facultatif \]** à un paramètre qui possède également les **\[** [](lcid.md) **\]** attributs LCID ou **\[** [**retVal**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7b1b8-125">You cannot apply the **\[optional\]** attribute to a parameter that also has the **\[**[**lcid**](lcid.md)**\]** or **\[**[**retval**](retval.md)**\]** attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="7b1b8-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="7b1b8-126">Examples</span></span>

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a><span data-ttu-id="7b1b8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b1b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b1b8-128">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="7b1b8-128">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="7b1b8-129">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="7b1b8-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="7b1b8-130">**LCID**</span><span class="sxs-lookup"><span data-stu-id="7b1b8-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="7b1b8-131">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="7b1b8-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7b1b8-132">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="7b1b8-132">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7b1b8-133">**retval**</span><span class="sxs-lookup"><span data-stu-id="7b1b8-133">**retval**</span></span>](retval.md)
</dt> </dl>

 

 