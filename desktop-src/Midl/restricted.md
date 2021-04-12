---
title: restricted (attribut)
description: L’attribut \ Restricted \ spécifie qu’une bibliothèque, ou un membre d’un module, d’une interface ou d’une dispinterface ne peut pas être appelé arbitrairement.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- MIDL d’attribut limité
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381889"
---
# <a name="restricted-attribute"></a><span data-ttu-id="7a79a-104">restricted (attribut)</span><span class="sxs-lookup"><span data-stu-id="7a79a-104">restricted attribute</span></span>

<span data-ttu-id="7a79a-105">L’attribut **\[ Restricted \]** spécifie qu’une bibliothèque, ou un membre d’un module, d’une interface ou d’une dispinterface ne peut pas être appelé arbitrairement.</span><span class="sxs-lookup"><span data-stu-id="7a79a-105">The **\[restricted\]** attribute specifies that a library, or member of a module, interface, or dispinterface cannot be called arbitrarily.</span></span>

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a><span data-ttu-id="7a79a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a79a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a79a-107">*autres attributs*</span><span class="sxs-lookup"><span data-stu-id="7a79a-107">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="7a79a-108">Zéro, un ou plusieurs attributs MIDL.</span><span class="sxs-lookup"><span data-stu-id="7a79a-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="7a79a-109">*type d’instruction*</span><span class="sxs-lookup"><span data-stu-id="7a79a-109">*statement-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7a79a-110">Une des valeurs suivantes : [**Library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="7a79a-110">One of the following: [**library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="7a79a-111">*nom de l’instruction*</span><span class="sxs-lookup"><span data-stu-id="7a79a-111">*statement-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7a79a-112">Identificateur par lequel le logiciel fait référence à cette instruction.</span><span class="sxs-lookup"><span data-stu-id="7a79a-112">The identifier by which the software refers to this statement.</span></span>

</dd> <dt>

<span data-ttu-id="7a79a-113">*Description*</span><span class="sxs-lookup"><span data-stu-id="7a79a-113">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="7a79a-114">Éléments de langage MIDL qui définissent le contenu de cette instruction.</span><span class="sxs-lookup"><span data-stu-id="7a79a-114">MIDL language elements that define the contents of this statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a79a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7a79a-115">Remarks</span></span>

<span data-ttu-id="7a79a-116">Cet attribut vous permet de contrôler l’accès aux éléments des interfaces, bibliothèques, modules et dispinterfaces.</span><span class="sxs-lookup"><span data-stu-id="7a79a-116">This attribute enables you to control access to elements of interfaces, libraries, modules, and dispinterfaces.</span></span> <span data-ttu-id="7a79a-117">Par exemple, il peut empêcher l’utilisation d’un élément de données par un programmeur de macro.</span><span class="sxs-lookup"><span data-stu-id="7a79a-117">For example, it can prevent a data item from being used by a macro programmer.</span></span> <span data-ttu-id="7a79a-118">Vous pouvez appliquer cet attribut à un membre d’une [**coclasse**](coclass.md), indépendamment du fait que le membre est une dispinterface ou une interface, et indépendamment du fait que le membre soit un récepteur (entrant) ou une source (sortante).</span><span class="sxs-lookup"><span data-stu-id="7a79a-118">You can apply this attribute to a member of a [**coclass**](coclass.md), independent of whether the member is a dispinterface or interface, and independent of whether the member is a sink (incoming) or source (outgoing).</span></span> <span data-ttu-id="7a79a-119">Un membre d’une **coclasse** ne peut pas avoir à la fois les attributs **\[ Restricted \]** et **\[ default \]** .</span><span class="sxs-lookup"><span data-stu-id="7a79a-119">A member of a **coclass** cannot have both the **\[restricted\]** and **\[default\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="7a79a-120">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="7a79a-120">Flags</span></span>

<span data-ttu-id="7a79a-121">IMPLTYPEFLAG \_ FRESTRICTED, FUNCFLAG \_ FRESTRICTED</span><span class="sxs-lookup"><span data-stu-id="7a79a-121">IMPLTYPEFLAG\_FRESTRICTED, FUNCFLAG\_FRESTRICTED</span></span>

## <a name="examples"></a><span data-ttu-id="7a79a-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="7a79a-122">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a><span data-ttu-id="7a79a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a79a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a79a-124">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="7a79a-124">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="7a79a-125">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="7a79a-125">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="7a79a-126">**interface**</span><span class="sxs-lookup"><span data-stu-id="7a79a-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="7a79a-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="7a79a-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="7a79a-128">**modules**</span><span class="sxs-lookup"><span data-stu-id="7a79a-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="7a79a-129">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="7a79a-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7a79a-130">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="7a79a-130">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="7a79a-131">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="7a79a-131">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 