---
title: attribut par défaut
description: L’attribut \ default \ indique que l’interface ou dispinterface, définie dans une coclasse, représente l’interface de programmabilité par défaut. Cet attribut est destiné à être utilisé par les langages de macro.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- MIDL d’attribut par défaut
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463010"
---
# <a name="default-attribute"></a><span data-ttu-id="b7603-105">attribut par défaut</span><span class="sxs-lookup"><span data-stu-id="b7603-105">default attribute</span></span>

<span data-ttu-id="b7603-106">L’attribut **\[ par \] défaut** indique que l' [**interface**](interface.md) ou la [**dispinterface**](dispinterface.md), définie dans une [**coclasse**](coclass.md), représente l’interface de programmabilité par défaut.</span><span class="sxs-lookup"><span data-stu-id="b7603-106">The **\[default\]** attribute Indicates that the [**interface**](interface.md) or [**dispinterface**](dispinterface.md), defined within a [**coclass**](coclass.md), represents the default programmability interface.</span></span> <span data-ttu-id="b7603-107">Cet attribut est destiné à être utilisé par les langages de macro.</span><span class="sxs-lookup"><span data-stu-id="b7603-107">This attribute is intended for use by macro languages.</span></span>

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a><span data-ttu-id="b7603-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7603-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7603-109">*UUID-Number*</span><span class="sxs-lookup"><span data-stu-id="b7603-109">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="b7603-110">Spécifie un numéro d’identification unique universel pour la [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="b7603-110">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7603-111">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="b7603-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b7603-112">Spécifie d’autres attributs de [**coclasse**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="b7603-112">Specifies additional [**coclass**](coclass.md) attributes.</span></span> <span data-ttu-id="b7603-113">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="b7603-113">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="b7603-114">*nom de la coclasse*</span><span class="sxs-lookup"><span data-stu-id="b7603-114">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b7603-115">Spécifie le nom par lequel d’autres composants logiciels peuvent référencer cette [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="b7603-115">Specifies the name by which other software components can reference this [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7603-116">*Optional-interface-Attribute*</span><span class="sxs-lookup"><span data-stu-id="b7603-116">*optional-interface-attribute*</span></span> 
</dt> <dd>

<span data-ttu-id="b7603-117">L' **\[** [](source.md) **\]** attribut source, qui spécifie qu’une interface ou une dispinterface est sortante, est le seul autre attribut qui peut être utilisé ici.</span><span class="sxs-lookup"><span data-stu-id="b7603-117">The **\[**[**source**](source.md)**\]** attribute, which specifies that an interface or dispinterface is outgoing, is the only other attribute that can be used here.</span></span>

</dd> <dt>

<span data-ttu-id="b7603-118">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="b7603-118">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b7603-119">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="b7603-119">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7603-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b7603-120">Remarks</span></span>

<span data-ttu-id="b7603-121">Une [**coclasse**](coclass.md) peut avoir au plus deux membres **\[ par défaut \]** .</span><span class="sxs-lookup"><span data-stu-id="b7603-121">A [**coclass**](coclass.md) may have at most two **\[default\]** members.</span></span> <span data-ttu-id="b7603-122">L’une représente l’interface sortante (source) ou dispinterface, tandis que l’autre représente l’interface entrante (sink) ou dispinterface.</span><span class="sxs-lookup"><span data-stu-id="b7603-122">One represents the outgoing (source) interface or dispinterface, and the other represents the incoming (sink) interface or dispinterface.</span></span> <span data-ttu-id="b7603-123">Si l’attribut **\[ par \] défaut** n’est spécifié pour aucun membre de la **coclasse** ou du **cotype**, les premiers membres sortants et entrants qui n’ont pas l' **\[** attribut [**Restricted**](restricted.md) **\]** sont traités comme des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="b7603-123">If the **\[default\]** attribute is not specified for any member of the **coclass** or **cotype**, the first outgoing and incoming members that do not have the **\[**[**restricted**](restricted.md)**\]** attribute are treated as the defaults.</span></span>

### <a name="flags"></a><span data-ttu-id="b7603-124">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="b7603-124">Flags</span></span>

<span data-ttu-id="b7603-125">IMPLTYPEFLAG \_ FDEFAULT</span><span class="sxs-lookup"><span data-stu-id="b7603-125">IMPLTYPEFLAG\_FDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="b7603-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="b7603-126">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a><span data-ttu-id="b7603-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7603-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7603-128">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="b7603-128">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="b7603-129">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="b7603-129">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="b7603-130">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="b7603-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b7603-131">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="b7603-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="b7603-132">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="b7603-132">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="b7603-133">**sensible**</span><span class="sxs-lookup"><span data-stu-id="b7603-133">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="b7603-134">**code**</span><span class="sxs-lookup"><span data-stu-id="b7603-134">**source**</span></span>](source.md)
</dt> </dl>

 

 