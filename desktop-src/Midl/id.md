---
title: attribut id
description: L’attribut \ ID \ spécifie un DISPID pour une fonction membre (une propriété ou une méthode, dans une interface ou une dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- ID MIDL de l’attribut ID
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381814"
---
# <a name="id-attribute"></a><span data-ttu-id="fc568-104">attribut id</span><span class="sxs-lookup"><span data-stu-id="fc568-104">id attribute</span></span>

<span data-ttu-id="fc568-105">L’attribut **\[ ID \]** spécifie un DISPID pour une fonction membre (une propriété ou une méthode, dans une interface ou une dispinterface).</span><span class="sxs-lookup"><span data-stu-id="fc568-105">The **\[id\]** attribute specifies a DISPID for a member function (either a property or a method, in an interface or dispinterface).</span></span>

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="fc568-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc568-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc568-107">*ID-num*</span><span class="sxs-lookup"><span data-stu-id="fc568-107">*id-num*</span></span> 
</dt> <dd>

<span data-ttu-id="fc568-108">DISPID pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="fc568-108">DISPID for the function.</span></span>

</dd> <dt>

<span data-ttu-id="fc568-109">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="fc568-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fc568-110">Spécifie une liste de zéro, un ou plusieurs attributs d’interface MIDL.</span><span class="sxs-lookup"><span data-stu-id="fc568-110">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="fc568-111">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="fc568-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="fc568-112">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="fc568-112">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="fc568-113">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="fc568-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fc568-114">Spécifie le nom de la fonction dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="fc568-114">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="fc568-115">*liste de paramètres facultatifs*</span><span class="sxs-lookup"><span data-stu-id="fc568-115">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fc568-116">Zéro, un ou plusieurs paramètres de fonction.</span><span class="sxs-lookup"><span data-stu-id="fc568-116">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc568-117">Notes</span><span class="sxs-lookup"><span data-stu-id="fc568-117">Remarks</span></span>

<span data-ttu-id="fc568-118">Utilisez l’attribut **\[ ID \]** lorsque vous souhaitez assigner un DISPID standard (tel que \_ value DISPID, DISPID NEWENUM, \_ etc.) à une méthode ou une propriété, ou lorsque vous implémentez votre propre **IDispatch :: Invoke** au lieu de le déléguer à **DispInvoke** / **ITypeInfo :: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="fc568-118">Use the **\[id\]** attribute when you want to assign a standard DISPID (like DISPID\_VALUE, DISPID\_NEWENUM etc.) to a method or property, or when you implement your own **IDispatch::Invoke** instead of delegating to **DispInvoke**/**ITypeInfo::Invoke**.</span></span>

<span data-ttu-id="fc568-119">Si vous n’utilisez pas l’attribut **\[ ID \]** sur une interface, le compilateur MIDL assigne un DISPID pour vous.</span><span class="sxs-lookup"><span data-stu-id="fc568-119">If you do not use the **\[id\]** attribute on an interface, the MIDL compiler will assign a DISPID for you.</span></span> <span data-ttu-id="fc568-120">Toutefois, lorsque vous spécifiez une dispinterface à l’aide de propriétés et de méthodes, vous devez spécifier un DISPID pour chaque propriété et méthode.</span><span class="sxs-lookup"><span data-stu-id="fc568-120">However, when you specify a dispinterface by using properties and methods, you must specify a DISPID for every property and method.</span></span>

<span data-ttu-id="fc568-121">L' *ID-num* est une valeur intégrale positive 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fc568-121">The *id-num* is a 32-bit positive integral value.</span></span> <span data-ttu-id="fc568-122">Les ID négatifs sont réservés pour une utilisation par Automation.</span><span class="sxs-lookup"><span data-stu-id="fc568-122">Negative IDs are reserved for use by Automation.</span></span>

## <a name="examples"></a><span data-ttu-id="fc568-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="fc568-123">Examples</span></span>

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a><span data-ttu-id="fc568-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc568-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc568-125">**interface**</span><span class="sxs-lookup"><span data-stu-id="fc568-125">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="fc568-126">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="fc568-126">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="fc568-127">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="fc568-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="fc568-128">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="fc568-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="fc568-129">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="fc568-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 