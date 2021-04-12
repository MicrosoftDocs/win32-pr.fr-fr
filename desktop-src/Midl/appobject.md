---
title: appobject (attribut)
description: L’attribut \ AppObject \ identifie la coclasse comme un objet application, qui est associé à une application EXE complète.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- MIDL de l’attribut AppObject
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381840"
---
# <a name="appobject-attribute"></a><span data-ttu-id="95d9f-104">appobject (attribut)</span><span class="sxs-lookup"><span data-stu-id="95d9f-104">appobject attribute</span></span>

<span data-ttu-id="95d9f-105">L’attribut **\[ AppObject \]** identifie la [**coclasse**](coclass.md) comme un objet application, qui est associé à une application exe complète.</span><span class="sxs-lookup"><span data-stu-id="95d9f-105">The **\[appobject\]** attribute identifies the [**coclass**](coclass.md) as an application object, which is associated with a full EXE application.</span></span>

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a><span data-ttu-id="95d9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95d9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d9f-107">*UUID-Number*</span><span class="sxs-lookup"><span data-stu-id="95d9f-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="95d9f-108">Spécifie un numéro d’identification unique universel pour la [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="95d9f-108">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d9f-109">*coclass-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="95d9f-109">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="95d9f-110">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à l’instruction [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="95d9f-110">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="95d9f-111">Les attributs **de coclasse** autorisés sont [**\[ helpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ Licensed \]**](licensed.md), [**\[ version \]**](version.md), [**\[ Control \]**](control.md)et [**\[ Hidden \]**](hidden.md).</span><span class="sxs-lookup"><span data-stu-id="95d9f-111">Allowable **coclass** attributes are [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[licensed\]**](licensed.md), [**\[version\]**](version.md), [**\[control\]**](control.md), and [**\[hidden\]**](hidden.md).</span></span>

</dd> <dt>

<span data-ttu-id="95d9f-112">*NomClasse*</span><span class="sxs-lookup"><span data-stu-id="95d9f-112">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="95d9f-113">Spécifie le nom par lequel l’objet composant est connu dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="95d9f-113">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="95d9f-114">*définition de coclasse*</span><span class="sxs-lookup"><span data-stu-id="95d9f-114">*coclass definition*</span></span> 
</dt> <dd>

<span data-ttu-id="95d9f-115">Spécifie les instructions qui composent la définition de [**coclasse**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="95d9f-115">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95d9f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="95d9f-116">Remarks</span></span>

<span data-ttu-id="95d9f-117">L’attribut **\[ AppObject \]** indique également que les fonctions et les propriétés de la [**coclasse**](coclass.md) sont globalement disponibles dans la bibliothèque de types actuelle.</span><span class="sxs-lookup"><span data-stu-id="95d9f-117">The **\[appobject\]** attribute also indicates that the functions and properties of the [**coclass**](coclass.md) are globally available in the current type library.</span></span>

<span data-ttu-id="95d9f-118">La représentation TYPEFLAG de cet attribut est TYPEFLAG \_ FAPPOBJECT</span><span class="sxs-lookup"><span data-stu-id="95d9f-118">The typeflag representation for this attribute is TYPEFLAG\_FAPPOBJECT</span></span>

## <a name="examples"></a><span data-ttu-id="95d9f-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="95d9f-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="95d9f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95d9f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d9f-121">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="95d9f-121">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="95d9f-122">**régulation**</span><span class="sxs-lookup"><span data-stu-id="95d9f-122">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="95d9f-123">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="95d9f-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="95d9f-124">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="95d9f-124">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="95d9f-125">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="95d9f-125">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="95d9f-126">**masquer**</span><span class="sxs-lookup"><span data-stu-id="95d9f-126">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="95d9f-127">**licensed**</span><span class="sxs-lookup"><span data-stu-id="95d9f-127">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="95d9f-128">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="95d9f-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="95d9f-129">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="95d9f-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="95d9f-130">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="95d9f-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="95d9f-131">**Version**</span><span class="sxs-lookup"><span data-stu-id="95d9f-131">**version**</span></span>](version.md)
</dt> </dl>

 

 