---
title: attribut sous licence
description: L’attribut \ Licensed indique que la coclasse à laquelle elle s’applique est concédée sous licence et doit être instanciée à l’aide de IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- MIDL d’attribut sous licence
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031109"
---
# <a name="licensed-attribute"></a><span data-ttu-id="56658-104">attribut sous licence</span><span class="sxs-lookup"><span data-stu-id="56658-104">licensed attribute</span></span>

<span data-ttu-id="56658-105">L’attribut **\[ Licensed \]** indique que la [**coclasse**](coclass.md) à laquelle elle s’applique est concédée sous licence et doit être instanciée à l’aide de [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span><span class="sxs-lookup"><span data-stu-id="56658-105">The **\[licensed\]** attribute indicates that the [**coclass**](coclass.md) to which it applies is licensed, and must be instantiated using [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span></span>

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a><span data-ttu-id="56658-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56658-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56658-107">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="56658-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="56658-108">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à l’instruction [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="56658-108">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="56658-109">Les attributs de **coclasse** autorisés sont **\[** [**helpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[ Licensed \]**, **\[** [**version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** et **\[** [**Hidden**](hidden.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="56658-109">Allowable **coclass** attributes are **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[licensed\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, and **\[**[**hidden**](hidden.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="56658-110">*NomClasse*</span><span class="sxs-lookup"><span data-stu-id="56658-110">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="56658-111">Spécifie le nom par lequel l’objet composant est connu dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="56658-111">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="56658-112">*coclasse-définition*</span><span class="sxs-lookup"><span data-stu-id="56658-112">*coclass-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="56658-113">Spécifie les instructions qui composent la définition de [**coclasse**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="56658-113">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56658-114">Notes</span><span class="sxs-lookup"><span data-stu-id="56658-114">Remarks</span></span>

<span data-ttu-id="56658-115">La gestion des licences est une fonctionnalité de COM qui permet de contrôler la création d’objets.</span><span class="sxs-lookup"><span data-stu-id="56658-115">Licensing is a feature of COM that provides control over object creation.</span></span> <span data-ttu-id="56658-116">Les objets sous licence ne peuvent être créés que par des clients autorisés à les utiliser.</span><span class="sxs-lookup"><span data-stu-id="56658-116">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="56658-117">La gestion des licences est implémentée dans COM par le biais de l’interface [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) et par la prise en charge d’une clé de licence qui peut être transmise au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="56658-117">Licensing is implemented in COM through the [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

### <a name="flags"></a><span data-ttu-id="56658-118">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="56658-118">Flags</span></span>

<span data-ttu-id="56658-119">TYPEFLAG \_ FLICENSED</span><span class="sxs-lookup"><span data-stu-id="56658-119">TYPEFLAG\_FLICENSED</span></span>

## <a name="examples"></a><span data-ttu-id="56658-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="56658-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a><span data-ttu-id="56658-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56658-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56658-122">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="56658-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="56658-123">Contenu d’une bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="56658-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="56658-124">**régulation**</span><span class="sxs-lookup"><span data-stu-id="56658-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="56658-125">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="56658-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="56658-126">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="56658-126">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="56658-127">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="56658-127">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="56658-128">**masquer**</span><span class="sxs-lookup"><span data-stu-id="56658-128">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="56658-129">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="56658-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="56658-130">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="56658-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="56658-131">**Version**</span><span class="sxs-lookup"><span data-stu-id="56658-131">**version**</span></span>](version.md)
</dt> </dl>

 

 