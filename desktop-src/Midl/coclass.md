---
title: coclass (attribut)
description: L’instruction coclass fournit une liste des interfaces prises en charge pour un objet composant.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- attribut de coclasse MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381891"
---
# <a name="coclass-attribute"></a><span data-ttu-id="a8429-104">coclass (attribut)</span><span class="sxs-lookup"><span data-stu-id="a8429-104">coclass attribute</span></span>

<span data-ttu-id="a8429-105">L’instruction **coclass** fournit une liste des interfaces prises en charge pour un objet composant.</span><span class="sxs-lookup"><span data-stu-id="a8429-105">The **coclass** statement provides a listing of the supported interfaces for a component object.</span></span>

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a><span data-ttu-id="a8429-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8429-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8429-107">*coclass-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="a8429-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a8429-108">L' **\[** attribut [**UUID**](uuid.md) **\]** est requis sur une **coclasse**.</span><span class="sxs-lookup"><span data-stu-id="a8429-108">The **\[**[**uuid**](uuid.md)**\]** attribute is required on a **coclass**.</span></span> <span data-ttu-id="a8429-109">Il s’agit du même **\[ UUID \]** qui est inscrit en tant que CLSID dans la base de données d’inscription du système.</span><span class="sxs-lookup"><span data-stu-id="a8429-109">This is the same **\[uuid\]** that is registered as a CLSID in the system registration database.</span></span> <span data-ttu-id="a8429-110">Les **\[** [](helpstring.md) **\]** attributs HelpString, **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**Licensed**](licensed.md), **\]** **\[** [**version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** et **\[** [**AppObject**](appobject.md) **\]** sont acceptés, mais pas obligatoires, avant une définition de **coclasse** .</span><span class="sxs-lookup"><span data-stu-id="a8429-110">The **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**licensed**](licensed.md)**\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, and **\[**[**appobject**](appobject.md)**\]** attributes are accepted, but not required, before a **coclass** definition.</span></span>

</dd> <dt>

<span data-ttu-id="a8429-111">*NomClasse*</span><span class="sxs-lookup"><span data-stu-id="a8429-111">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="a8429-112">Nom par lequel l’objet commun est connu dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="a8429-112">Name by which the common object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="a8429-113">*interface-attributs*</span><span class="sxs-lookup"><span data-stu-id="a8429-113">*interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="a8429-114">Attributs facultatifs pour l’interface ou dispinterface.</span><span class="sxs-lookup"><span data-stu-id="a8429-114">Optional attributes for the interface or dispinterface.</span></span> <span data-ttu-id="a8429-115">Les **\[** attributs [**source**](source.md) **\]** , **\[** [**default**](default.md) **\]** et **\[** [**Restricted**](restricted.md) **\]** sont acceptés sur une interface ou dispinterface dans une **coclasse**.</span><span class="sxs-lookup"><span data-stu-id="a8429-115">The **\[**[**source**](source.md)**\]**, **\[**[**default**](default.md)**\]**, and **\[**[**restricted**](restricted.md)**\]** attributes are accepted on an interface or dispinterface within a **coclass**.</span></span>

</dd> <dt>

<span data-ttu-id="a8429-116">*InterfaceName*</span><span class="sxs-lookup"><span data-stu-id="a8429-116">*interfacename*</span></span> 
</dt> <dd>

<span data-ttu-id="a8429-117">Soit une interface déclarée avec le mot clé [**interface**](interface.md) , soit une dispinterface déclarée avec le mot clé [**dispinterface**](dispinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="a8429-117">Either an interface declared with the [**interface**](interface.md) keyword, or a dispinterface declared with the [**dispinterface**](dispinterface.md) keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8429-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a8429-118">Remarks</span></span>

<span data-ttu-id="a8429-119">Le modèle d’objet de composant Microsoft définit une classe en tant qu’implémentation de qui autorise **QueryInterface** entre un ensemble d’interfaces.</span><span class="sxs-lookup"><span data-stu-id="a8429-119">The Microsoft Component Object Model defines a class as an implementation that allows **QueryInterface** between a set of interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="a8429-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="a8429-120">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a><span data-ttu-id="a8429-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8429-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8429-122">**appobject**</span><span class="sxs-lookup"><span data-stu-id="a8429-122">**appobject**</span></span>](appobject.md)
</dt> <dt>

[<span data-ttu-id="a8429-123">**régulation**</span><span class="sxs-lookup"><span data-stu-id="a8429-123">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="a8429-124">**default**</span><span class="sxs-lookup"><span data-stu-id="a8429-124">**default**</span></span>](default.md)
</dt> <dt>

[<span data-ttu-id="a8429-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="a8429-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="a8429-126">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="a8429-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="a8429-127">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="a8429-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="a8429-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="a8429-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="a8429-129">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="a8429-129">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="a8429-130">**masquer**</span><span class="sxs-lookup"><span data-stu-id="a8429-130">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="a8429-131">**interface**</span><span class="sxs-lookup"><span data-stu-id="a8429-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="a8429-132">**licensed**</span><span class="sxs-lookup"><span data-stu-id="a8429-132">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="a8429-133">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="a8429-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="a8429-134">**sensible**</span><span class="sxs-lookup"><span data-stu-id="a8429-134">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="a8429-135">**code**</span><span class="sxs-lookup"><span data-stu-id="a8429-135">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="a8429-136">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="a8429-136">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="a8429-137">**universel**</span><span class="sxs-lookup"><span data-stu-id="a8429-137">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="a8429-138">**Version**</span><span class="sxs-lookup"><span data-stu-id="a8429-138">**version**</span></span>](version.md)
</dt> </dl>

 

 