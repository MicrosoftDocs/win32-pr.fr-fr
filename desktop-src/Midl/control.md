---
title: attribut de contrôle
description: L’attribut \ Control \ identifie une coclasse ou une bibliothèque comme un contrôle COM, à partir duquel un site conteneur dérivera des bibliothèques de types ou des classes d’objets composant supplémentaires.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- attribut de contrôle MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724956"
---
# <a name="control-attribute"></a><span data-ttu-id="b379a-104">attribut de contrôle</span><span class="sxs-lookup"><span data-stu-id="b379a-104">control attribute</span></span>

<span data-ttu-id="b379a-105">L’attribut **\[ Control \]** identifie une [**coclasse**](coclass.md) ou une [**bibliothèque**](library.md) comme un contrôle com, à partir duquel un site conteneur dérivera des bibliothèques de types ou des classes d’objets composant supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b379a-105">The **\[control\]** attribute identifies a [**coclass**](coclass.md) or [**library**](library.md) as a COM control, from which a container site will derive additional type libraries or component object classes.</span></span>

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a><span data-ttu-id="b379a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b379a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b379a-107">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="b379a-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b379a-108">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la [**bibliothèque**](library.md) ou à l’instruction de [**coclasse**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="b379a-108">Specifies zero or more attributes that apply to the [**library**](library.md) or [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="b379a-109">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="b379a-109">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="b379a-110">*lib-or-NomCoclasse*</span><span class="sxs-lookup"><span data-stu-id="b379a-110">*lib-or-coclassname*</span></span> 
</dt> <dd>

<span data-ttu-id="b379a-111">Spécifie le nom de la [**bibliothèque**](library.md) ou de la [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="b379a-111">Specifies the name of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="b379a-112">*Description*</span><span class="sxs-lookup"><span data-stu-id="b379a-112">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="b379a-113">Instructions MIDL qui spécifient les membres de la [**bibliothèque**](library.md) ou de la [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="b379a-113">MIDL statements that specify the members of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b379a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b379a-114">Remarks</span></span>

<span data-ttu-id="b379a-115">Cet attribut vous permet de marquer des bibliothèques de types qui décrivent des contrôles afin qu’elles ne soient pas affichées dans les navigateurs de type destinés aux objets non visuels.</span><span class="sxs-lookup"><span data-stu-id="b379a-115">This attribute allows you to mark type libraries that describe controls so they will not be displayed in type browsers intended for nonvisual objects.</span></span>

### <a name="flags"></a><span data-ttu-id="b379a-116">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="b379a-116">Flags</span></span>

<span data-ttu-id="b379a-117">TYPEFLAG \_ FCONTROL, libflag \_ FCONTROL</span><span class="sxs-lookup"><span data-stu-id="b379a-117">TYPEFLAG\_FCONTROL, LIBFLAG\_FCONTROL</span></span>

## <a name="examples"></a><span data-ttu-id="b379a-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="b379a-118">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a><span data-ttu-id="b379a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b379a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b379a-120">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="b379a-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b379a-121">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="b379a-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="b379a-122">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="b379a-122">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="b379a-123">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="b379a-123">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="b379a-124">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="b379a-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="b379a-125">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="b379a-125">**library**</span></span>](library.md)
</dt> </dl>

 

 