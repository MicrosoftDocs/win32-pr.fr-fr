---
title: attribut source
description: L’attribut \ source \ indique qu’un membre d’une coclasse, d’une propriété ou d’une méthode est une source d’événements. Pour un membre d’une coclasse, cet attribut signifie que le membre est appelé au lieu d’être implémenté.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- MIDL de l’attribut source
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940866"
---
# <a name="source-attribute"></a><span data-ttu-id="03f43-105">attribut source</span><span class="sxs-lookup"><span data-stu-id="03f43-105">source attribute</span></span>

<span data-ttu-id="03f43-106">L’attribut **\[ source \]** indique qu’un membre d’une [**coclasse**](coclass.md), d’une propriété ou d’une méthode est une source d’événements.</span><span class="sxs-lookup"><span data-stu-id="03f43-106">The **\[source\]** attribute indicates that a member of a [**coclass**](coclass.md), property, or method is a source of events.</span></span> <span data-ttu-id="03f43-107">Pour un membre d’une **coclasse**, cet attribut signifie que le membre est appelé au lieu d’être implémenté.</span><span class="sxs-lookup"><span data-stu-id="03f43-107">For a member of a **coclass**, this attribute means that the member is called rather than implemented.</span></span>

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a><span data-ttu-id="03f43-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03f43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03f43-109">*coclasse-attributs*</span><span class="sxs-lookup"><span data-stu-id="03f43-109">*coclass-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="03f43-110">Zéro, un ou plusieurs attributs qui seront appliqués à la [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="03f43-110">Zero or more attributes that will be applied to the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f43-111">*nom de la coclasse*</span><span class="sxs-lookup"><span data-stu-id="03f43-111">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="03f43-112">Identificateur de nom de la [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="03f43-112">The name identifier of the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f43-113">*attributs facultatifs*</span><span class="sxs-lookup"><span data-stu-id="03f43-113">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="03f43-114">Zéro, un ou plusieurs attributs MIDL.</span><span class="sxs-lookup"><span data-stu-id="03f43-114">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="03f43-115">*type d’instruction*</span><span class="sxs-lookup"><span data-stu-id="03f43-115">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="03f43-116">Peut être [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="03f43-116">Can be [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f43-117">*nom de l’instruction*</span><span class="sxs-lookup"><span data-stu-id="03f43-117">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="03f43-118">Nom de l' [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="03f43-118">The name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f43-119">*type d’objet*</span><span class="sxs-lookup"><span data-stu-id="03f43-119">*object-type*</span></span> 
</dt> <dd>

<span data-ttu-id="03f43-120">Type de l’objet retourné par la méthode.</span><span class="sxs-lookup"><span data-stu-id="03f43-120">The type of the object that the method returns.</span></span> <span data-ttu-id="03f43-121">Cet objet est une source d’événements.</span><span class="sxs-lookup"><span data-stu-id="03f43-121">This object is a source of events.</span></span>

</dd> <dt>

<span data-ttu-id="03f43-122">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="03f43-122">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="03f43-123">Nom d’une méthode dans une [**interface**](interface.md) ou une [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="03f43-123">The name of a method in an [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="03f43-124">*liste de paramètres facultatifs*</span><span class="sxs-lookup"><span data-stu-id="03f43-124">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="03f43-125">Zéro, un ou plusieurs paramètres de méthode.</span><span class="sxs-lookup"><span data-stu-id="03f43-125">Zero or more method parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03f43-126">Notes</span><span class="sxs-lookup"><span data-stu-id="03f43-126">Remarks</span></span>

<span data-ttu-id="03f43-127">Sur une propriété ou une méthode, l’attribut **\[ source \]** indique que le membre retourne un objet ou un variant qui est une source d’événements.</span><span class="sxs-lookup"><span data-stu-id="03f43-127">On a property or method, the **\[source\]** attribute indicates that the member returns an object or VARIANT that is a source of events.</span></span> <span data-ttu-id="03f43-128">L’objet implémente **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="03f43-128">The object implements **IConnectionPointContainer**.</span></span>

### <a name="flags"></a><span data-ttu-id="03f43-129">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="03f43-129">Flags</span></span>

<span data-ttu-id="03f43-130">IMPLTYPEFLAG \_ FSOURCE, \_ source VARFLAG, FUNCFLAG \_ source</span><span class="sxs-lookup"><span data-stu-id="03f43-130">IMPLTYPEFLAG\_FSOURCE, VARFLAG\_SOURCE, FUNCFLAG\_SOURCE</span></span>

## <a name="examples"></a><span data-ttu-id="03f43-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="03f43-131">Examples</span></span>

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a><span data-ttu-id="03f43-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03f43-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f43-133">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="03f43-133">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="03f43-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="03f43-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="03f43-135">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="03f43-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="03f43-136">**interface**</span><span class="sxs-lookup"><span data-stu-id="03f43-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="03f43-137">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="03f43-137">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="03f43-138">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="03f43-138">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="03f43-139">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="03f43-139">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 