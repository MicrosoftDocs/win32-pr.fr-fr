---
title: propget (attribut)
description: L’attribut \ propget \ spécifie une fonction d’accesseur de propriété. La propriété doit avoir le même nom que la fonction.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- attribut propget MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031084"
---
# <a name="propget-attribute"></a><span data-ttu-id="f074b-105">propget (attribut)</span><span class="sxs-lookup"><span data-stu-id="f074b-105">propget attribute</span></span>

<span data-ttu-id="f074b-106">L’attribut **\[ propget \]** spécifie une fonction d’accesseur de propriété.</span><span class="sxs-lookup"><span data-stu-id="f074b-106">The **\[propget\]** attribute specifies a property accessor function.</span></span> <span data-ttu-id="f074b-107">La propriété doit avoir le même nom que la fonction.</span><span class="sxs-lookup"><span data-stu-id="f074b-107">The property must have the same name as the function.</span></span>

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="f074b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f074b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f074b-109">*attributs facultatifs*</span><span class="sxs-lookup"><span data-stu-id="f074b-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="f074b-110">Zéro, un ou plusieurs attributs de propriété.</span><span class="sxs-lookup"><span data-stu-id="f074b-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f074b-111">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="f074b-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f074b-112">Type des données retournées par la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="f074b-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f074b-113">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="f074b-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f074b-114">Nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="f074b-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f074b-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="f074b-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="f074b-116">Zéro, un ou plusieurs paramètres à la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="f074b-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f074b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f074b-117">Remarks</span></span>

<span data-ttu-id="f074b-118">Une fonction qui a l’attribut propget doit également avoir, en tant que dernier paramètre, un type pointeur avec les **\[** attributs [**out**](out-idl.md) **\]** et **\[** [**retVal**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f074b-118">A function that has the propget attribute should also have, as its last parameter, a pointer type with the **\[**[**out**](out-idl.md)**\]** and **\[**[**retval**](retval.md)**\]** attributes.</span></span> <span data-ttu-id="f074b-119">Si le dernier paramètre n’a pas les \[ attributs out, retval \] , la valeur de retour de la fonction est traitée comme un \[ paramètre out, retval \] .</span><span class="sxs-lookup"><span data-stu-id="f074b-119">If the last parameter does not have the \[out, retval\] attributes, the return value of the function is treated as an \[out, retval\] parameter.</span></span> <span data-ttu-id="f074b-120">Par exemple, une fonction avec le prototype</span><span class="sxs-lookup"><span data-stu-id="f074b-120">For example, a function with the prototype</span></span>

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

<span data-ttu-id="f074b-121">est traité comme</span><span class="sxs-lookup"><span data-stu-id="f074b-121">is treated as</span></span>

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

<span data-ttu-id="f074b-122">Au maximum, vous pouvez spécifier un **\[ propget \]**, **\[** [**propput**](propput.md) **\]** et **\[** [**PROPPUTREF**](propputref.md) **\]** pour une fonction.</span><span class="sxs-lookup"><span data-stu-id="f074b-122">At most, one of **\[propget\]**, **\[**[**propput**](propput.md)**\]**, and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="f074b-123">Si l' **\[** attribut [**LCID**](lcid.md) **\]** est utilisé dans la liste des paramètres d’une fonction qui contient un paramètre avec l' **\[** attribut [**propput**](propput.md) **\]** , le paramètre **\[ LCID \]** doit être le dernier de la dernière.</span><span class="sxs-lookup"><span data-stu-id="f074b-123">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[**[**propput**](propput.md)**\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="f074b-124">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="f074b-124">Flags</span></span>

<span data-ttu-id="f074b-125">APPELER \_ PropertyGet (</span><span class="sxs-lookup"><span data-stu-id="f074b-125">INVOKE\_PROPERTYGET</span></span>

## <a name="examples"></a><span data-ttu-id="f074b-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="f074b-126">Examples</span></span>

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a><span data-ttu-id="f074b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f074b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f074b-128">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="f074b-128">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f074b-129">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="f074b-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f074b-130">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="f074b-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f074b-131">**à**</span><span class="sxs-lookup"><span data-stu-id="f074b-131">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="f074b-132">**retval**</span><span class="sxs-lookup"><span data-stu-id="f074b-132">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="f074b-133">**propput**</span><span class="sxs-lookup"><span data-stu-id="f074b-133">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="f074b-134">**propputref**</span><span class="sxs-lookup"><span data-stu-id="f074b-134">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="f074b-135">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="f074b-135">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 