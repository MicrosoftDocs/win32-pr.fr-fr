---
title: propput (attribut)
description: L’attribut \ propput \ spécifie une fonction de définition de propriété. La propriété doit avoir le même nom que la fonction.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- propput, attribut MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101501"
---
# <a name="propput-attribute"></a><span data-ttu-id="07984-105">propput (attribut)</span><span class="sxs-lookup"><span data-stu-id="07984-105">propput attribute</span></span>

<span data-ttu-id="07984-106">L’attribut **\[ propput \]** spécifie une fonction de définition de propriété.</span><span class="sxs-lookup"><span data-stu-id="07984-106">The **\[propput\]** attribute specifies a property-setting function.</span></span> <span data-ttu-id="07984-107">La propriété doit avoir le même nom que la fonction *.*</span><span class="sxs-lookup"><span data-stu-id="07984-107">The property must have the same name as the function *.*</span></span>

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="07984-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07984-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07984-109">*attributs facultatifs*</span><span class="sxs-lookup"><span data-stu-id="07984-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="07984-110">Zéro, un ou plusieurs attributs de propriété.</span><span class="sxs-lookup"><span data-stu-id="07984-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="07984-111">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="07984-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="07984-112">Type des données retournées par la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="07984-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="07984-113">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="07984-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="07984-114">Nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="07984-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="07984-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="07984-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="07984-116">Zéro, un ou plusieurs paramètres à la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="07984-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07984-117">Notes</span><span class="sxs-lookup"><span data-stu-id="07984-117">Remarks</span></span>

<span data-ttu-id="07984-118">Une fonction qui a l’attribut **\[ propput \]** doit également avoir, en tant que dernier paramètre, un paramètre qui a l' **\[** attribut [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="07984-118">A function that has the **\[propput\]** attribute must also have, as its last parameter, a parameter that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="07984-119">Au maximum, vous **\[** [](propget.md) **\]** pouvez spécifier un propget, **\[ propput \]** et **\[** [**PROPPUTREF**](propputref.md) **\]** pour une fonction.</span><span class="sxs-lookup"><span data-stu-id="07984-119">At most, one of **\[**[**propget**](propget.md)**\]**, **\[propput\]** and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="07984-120">Si l' **\[** attribut [**LCID**](lcid.md) **\]** est utilisé dans la liste des paramètres d’une fonction qui contient un paramètre avec l’attribut **\[ propput \]** , le paramètre **\[ LCID \]** doit être le dernier de la dernière.</span><span class="sxs-lookup"><span data-stu-id="07984-120">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[propput\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="07984-121">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="07984-121">Flags</span></span>

<span data-ttu-id="07984-122">APPELER \_ PROPERTYPUT</span><span class="sxs-lookup"><span data-stu-id="07984-122">INVOKE\_PROPERTYPUT</span></span>

## <a name="examples"></a><span data-ttu-id="07984-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="07984-123">Examples</span></span>

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a><span data-ttu-id="07984-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07984-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07984-125">Différences entre MIDL et MKTYPLIB</span><span class="sxs-lookup"><span data-stu-id="07984-125">Differences Between MIDL and MKTYPLIB</span></span>](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[<span data-ttu-id="07984-126">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="07984-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="07984-127">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="07984-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="07984-128">**propget**</span><span class="sxs-lookup"><span data-stu-id="07984-128">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="07984-129">**propputref**</span><span class="sxs-lookup"><span data-stu-id="07984-129">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="07984-130">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="07984-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 