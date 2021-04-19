---
title: vararg (attribut)
description: L’attribut \ vararg \ spécifie que la fonction accepte un nombre variable de paramètres. Pour ce faire, le dernier paramètre doit être un tableau sécurisé de type VARIANT qui contient tous les paramètres restants.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- MIDL (MIDL), attribut vararg
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509031"
---
# <a name="vararg-attribute"></a><span data-ttu-id="74bc4-105">vararg (attribut)</span><span class="sxs-lookup"><span data-stu-id="74bc4-105">vararg attribute</span></span>

<span data-ttu-id="74bc4-106">L’attribut **\[ vararg \]** spécifie que la fonction accepte un nombre variable de paramètres.</span><span class="sxs-lookup"><span data-stu-id="74bc4-106">The **\[vararg\]** attribute specifies that the function takes a variable number of parameters.</span></span> <span data-ttu-id="74bc4-107">Pour ce faire, le dernier paramètre doit être un tableau sécurisé de type **Variant** qui contient tous les paramètres restants.</span><span class="sxs-lookup"><span data-stu-id="74bc4-107">To accomplish this, the last parameter must be a safe array of **VARIANT** type that contains all the remaining parameters.</span></span>

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a><span data-ttu-id="74bc4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74bc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74bc4-109">*attributs facultatifs*</span><span class="sxs-lookup"><span data-stu-id="74bc4-109">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="74bc4-110">Spécifie zéro ou plusieurs attributs à appliquer à la fonction.</span><span class="sxs-lookup"><span data-stu-id="74bc4-110">Specifies zero or more attributes to be applied to the function.</span></span> <span data-ttu-id="74bc4-111">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="74bc4-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="74bc4-112">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="74bc4-112">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="74bc4-113">Type des données retournées par la procédure distante à l’achèvement.</span><span class="sxs-lookup"><span data-stu-id="74bc4-113">The type of the data returned by the remote procedure upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="74bc4-114">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="74bc4-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="74bc4-115">Nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="74bc4-115">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="74bc4-116">*facultatif-param-Attributes*</span><span class="sxs-lookup"><span data-stu-id="74bc4-116">*optional-param-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="74bc4-117">Spécifie zéro ou plusieurs attributs à appliquer au paramètre de fonction immédiatement après la liste d’attributs.</span><span class="sxs-lookup"><span data-stu-id="74bc4-117">Specifies zero or more attributes to be applied to the function parameter immediately following the attribute listing.</span></span>

</dd> <dt>

<span data-ttu-id="74bc4-118">*Param-liste*</span><span class="sxs-lookup"><span data-stu-id="74bc4-118">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="74bc4-119">Spécifie tous les paramètres, enregistrez le paramètre final, variable.</span><span class="sxs-lookup"><span data-stu-id="74bc4-119">Specifies all the parameters, save the final, varying, parameter.</span></span>

</dd> <dt>

<span data-ttu-id="74bc4-120">*Last-param-Name*</span><span class="sxs-lookup"><span data-stu-id="74bc4-120">*last-param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="74bc4-121">Nom du paramètre variable.</span><span class="sxs-lookup"><span data-stu-id="74bc4-121">The name of the varying parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74bc4-122">Notes</span><span class="sxs-lookup"><span data-stu-id="74bc4-122">Remarks</span></span>

<span data-ttu-id="74bc4-123">Vous ne pouvez pas appliquer les **\[** attributs [**facultatifs**](optional.md) **\]** ou **\[** [**DefaultValue**](defaultvalue.md) **\]** à des paramètres dans une fonction qui a l’attribut **\[ vararg \]** .</span><span class="sxs-lookup"><span data-stu-id="74bc4-123">You cannot apply the **\[**[**optional**](optional.md)**\]** or **\[**[**defaultvalue**](defaultvalue.md)**\]** attributes to any parameters in a function that has the **\[vararg\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="74bc4-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="74bc4-124">Examples</span></span>

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a><span data-ttu-id="74bc4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74bc4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bc4-126">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="74bc4-126">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="74bc4-127">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="74bc4-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="74bc4-128">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="74bc4-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="74bc4-129">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="74bc4-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="74bc4-130">**facultatif**</span><span class="sxs-lookup"><span data-stu-id="74bc4-130">**optional**</span></span>](optional.md)
</dt> </dl>

 

 