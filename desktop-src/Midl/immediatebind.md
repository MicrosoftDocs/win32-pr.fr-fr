---
title: immediatebind (attribut)
description: L’attribut \ immediatebind \ indique que la base de données sera immédiatement notifiée de toutes les modifications apportées à la propriété d’un objet lié aux données.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- MIDL de l’attribut immediatebind
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104198838"
---
# <a name="immediatebind-attribute"></a><span data-ttu-id="7528c-104">immediatebind (attribut)</span><span class="sxs-lookup"><span data-stu-id="7528c-104">immediatebind attribute</span></span>

<span data-ttu-id="7528c-105">L’attribut **\[ immediatebind \]** indique que la base de données sera immédiatement notifiée de toutes les modifications apportées à la propriété d’un objet lié aux données.</span><span class="sxs-lookup"><span data-stu-id="7528c-105">The **\[immediatebind\]** attribute indicates that the database will be notified immediately of all changes to a property of a data-bound object.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="7528c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7528c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7528c-107">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="7528c-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7528c-108">Spécifie une liste d’un ou plusieurs attributs qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="7528c-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="7528c-109">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="7528c-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7528c-110">Spécifie le nom de l' [**interface**](interface.md) ou de [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="7528c-110">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="7528c-111">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="7528c-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7528c-112">Zéro, un ou plusieurs attributs de fonction.</span><span class="sxs-lookup"><span data-stu-id="7528c-112">Zero or more function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="7528c-113">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="7528c-113">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="7528c-114">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="7528c-114">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7528c-115">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="7528c-115">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7528c-116">Spécifie le nom de la fonction dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="7528c-116">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="7528c-117">*params*</span><span class="sxs-lookup"><span data-stu-id="7528c-117">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="7528c-118">Zéro, un ou plusieurs paramètres de fonction.</span><span class="sxs-lookup"><span data-stu-id="7528c-118">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7528c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="7528c-119">Remarks</span></span>

<span data-ttu-id="7528c-120">L’attribut **\[ immediatebind \]** permet aux contrôles de faire la différence entre les propriétés qui doivent notifier la base de données de chaque modification et celles qui ne le font pas.</span><span class="sxs-lookup"><span data-stu-id="7528c-120">The **\[immediatebind\]** attribute allows controls to differentiate between properties that need to notify the database of every change, and those that do not.</span></span> <span data-ttu-id="7528c-121">Par exemple, chaque modification apportée à un contrôle de case à cocher doit être envoyée immédiatement à la base de données sous-jacente, même si le contrôle n’a pas perdu le focus.</span><span class="sxs-lookup"><span data-stu-id="7528c-121">For example, every change to a checkbox control should be sent to the underlying database immediately, even if the control has not lost the focus.</span></span> <span data-ttu-id="7528c-122">Toutefois, pour un contrôle ListBox, une modification se produit chaque fois qu’une sélection différente est mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="7528c-122">However, for a listbox control, a change occurs whenever a different selection is highlighted.</span></span> <span data-ttu-id="7528c-123">Notifier la base de données d’une modification avant que le contrôle ne perde le focus n’est pas efficace et inutile.</span><span class="sxs-lookup"><span data-stu-id="7528c-123">Notifying the database of a change before the control loses focus would be inefficient and unnecessary.</span></span> <span data-ttu-id="7528c-124">L’attribut **\[ immediatebind \]** vous permet de spécifier, en définissant le bit immediatebind, des propriétés individuelles sur un formulaire dont les modifications doivent être signalées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="7528c-124">The **\[immediatebind\]** attribute allows you to specify, by setting the ImmediateBind bit, individual properties on a form whose changes should be reported immediately.</span></span>

<span data-ttu-id="7528c-125">Les propriétés qui ont l’attribut **\[ immediatebind \]** doivent également avoir l' **\[** attribut pouvant être [**lié**](bindable.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7528c-125">Properties that have the **\[immediatebind\]** attribute must also have the **\[**[**bindable**](bindable.md)**\]** attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="7528c-126">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="7528c-126">Flags</span></span>

<span data-ttu-id="7528c-127">FUNCFLAG \_ FIMMEDIATEBIND, VARFLAG \_ FIMMEDIATEBIND</span><span class="sxs-lookup"><span data-stu-id="7528c-127">FUNCFLAG\_FIMMEDIATEBIND, VARFLAG\_FIMMEDIATEBIND</span></span>

## <a name="examples"></a><span data-ttu-id="7528c-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="7528c-128">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a><span data-ttu-id="7528c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7528c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7528c-130">**bindable**</span><span class="sxs-lookup"><span data-stu-id="7528c-130">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="7528c-131">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="7528c-131">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="7528c-132">**interface**</span><span class="sxs-lookup"><span data-stu-id="7528c-132">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="7528c-133">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="7528c-133">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="7528c-134">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="7528c-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7528c-135">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="7528c-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7528c-136">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="7528c-136">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 