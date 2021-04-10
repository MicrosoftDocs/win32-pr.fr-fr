---
title: dual (attribut)
description: L’attribut double identifie une interface qui expose des propriétés et des méthodes par le biais de IDispatch et directement par le biais du VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- MIDL avec deux attributs
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940972"
---
# <a name="dual-attribute"></a><span data-ttu-id="4cb7c-104">dual (attribut)</span><span class="sxs-lookup"><span data-stu-id="4cb7c-104">dual attribute</span></span>

<span data-ttu-id="4cb7c-105">L’attribut **double** identifie une interface qui expose des propriétés et des méthodes par le biais de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) et directement par le biais du VTBL.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-105">The **dual** attribute identifies an interface that exposes properties and methods through [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and directly through the VTBL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="4cb7c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cb7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb7c-107">*UUID-Number*</span><span class="sxs-lookup"><span data-stu-id="4cb7c-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="4cb7c-108">Spécifie un numéro d’identification unique universel pour l’interface</span><span class="sxs-lookup"><span data-stu-id="4cb7c-108">Specifies a universally unique identification number for the interface</span></span>

</dd> <dt>

<span data-ttu-id="4cb7c-109">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4cb7c-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4cb7c-110">Spécifie une liste de zéro ou plusieurs attributs MIDL supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-110">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="4cb7c-111">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="4cb7c-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4cb7c-112">Nom de l’interface à laquelle l’attribut **double** sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-112">The name of the interface to which the **dual** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cb7c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4cb7c-113">Remarks</span></span>

<span data-ttu-id="4cb7c-114">Les interfaces identifiées par l’attribut **double** doivent être compatibles avec l’automatisation et être dérivées de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span><span class="sxs-lookup"><span data-stu-id="4cb7c-114">Interfaces identified by the **dual** attribute must be compatible with Automation and be derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span> <span data-ttu-id="4cb7c-115">Cet attribut n’est pas autorisé sur les dispinterfaces.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-115">This attribute is not allowed on dispinterfaces.</span></span>

<span data-ttu-id="4cb7c-116">L’attribut **double** crée une interface qui est à la fois une interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) et une interface com (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="4cb7c-116">The **dual** attribute creates an interface that is both an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface and a Component Object Model (COM) interface.</span></span> <span data-ttu-id="4cb7c-117">Les sept premières entrées du VTBL pour une interface double sont les sept membres de **IDispatch**, et les entrées restantes sont destinées à un accès direct aux membres de l’interface double.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-117">The first seven entries of the VTBL for a dual interface are the seven members of **IDispatch**, and the remaining entries are for direct access to members of the dual interface.</span></span> <span data-ttu-id="4cb7c-118">Tous les paramètres et types de retour spécifiés pour les membres d’une interface double doivent être des types compatibles Automation.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-118">All the parameters and return types specified for members of a dual interface must be Automation-compatible types.</span></span>

<span data-ttu-id="4cb7c-119">Tous les membres d’une interface double doivent passer un HRESULT comme valeur de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-119">All members of a dual interface must pass an HRESULT as the function return value.</span></span> <span data-ttu-id="4cb7c-120">Les membres, tels que les fonctions d’accesseur de propriété, qui doivent retourner d’autres valeurs, doivent spécifier le dernier paramètre comme [**out**](out-idl.md), [**retVal**](retval.md), indiquant un paramètre de sortie qui retourne la valeur de la fonction.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-120">Members, such as property accessor functions, that need to return other values, should specify the last parameter as [**out**](out-idl.md), [**retval**](retval.md), indicating an output parameter that returns the value of the function.</span></span> <span data-ttu-id="4cb7c-121">En outre, les membres qui doivent prendre en charge plusieurs paramètres régionaux doivent passer un paramètre [**LCID**](lcid.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb7c-121">In addition, members that need to support multiple locales should pass an [**lcid**](lcid.md) parameter.</span></span>

<span data-ttu-id="4cb7c-122">Une interface double fournit à la fois la vitesse de liaison VTBL directe et la flexibilité de la liaison [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4cb7c-122">A dual interface provides for both the speed of direct VTBL binding and the flexibility of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) binding.</span></span> <span data-ttu-id="4cb7c-123">Pour cette raison, les interfaces doubles sont recommandées dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-123">For this reason, dual interfaces are recommended whenever possible.</span></span>

> [!Note]  
> <span data-ttu-id="4cb7c-124">Si votre application accède à des données d’objet en effectuant un cast du pointeur *This* dans l’appel d’interface, vous devez vérifier les pointeurs VTBL dans l’objet par rapport à vos propres pointeurs VTBL pour vous assurer que vous êtes connecté au proxy approprié.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-124">If your application accesses object data by casting the *this* pointer within the interface call, you should check the VTBL pointers in the object against your own VTBL pointers to ensure that you are connected to the appropriate proxy.</span></span>

 

<span data-ttu-id="4cb7c-125">Si vous spécifiez **double** sur une interface, cela signifie que l’interface est compatible avec Automation et, par conséquent, les \_ indicateurs TYPEFLAG FDUAL et TYPEFLAG \_ FOLEAUTOMATION sont définis.</span><span class="sxs-lookup"><span data-stu-id="4cb7c-125">Specifying **dual** on an interface implies that the interface is compatible with Automation, and therefore causes both the TYPEFLAG\_FDUAL and TYPEFLAG\_FOLEAUTOMATION flags to be set.</span></span>

### <a name="flags"></a><span data-ttu-id="4cb7c-126">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="4cb7c-126">Flags</span></span>

<span data-ttu-id="4cb7c-127">TYPEFLAG \_ FDUAL, TYPEFLAG \_ FOLEAUTOMATION</span><span class="sxs-lookup"><span data-stu-id="4cb7c-127">TYPEFLAG\_FDUAL, TYPEFLAG\_FOLEAUTOMATION</span></span>

## <a name="examples"></a><span data-ttu-id="4cb7c-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="4cb7c-128">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a><span data-ttu-id="4cb7c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cb7c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb7c-130">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="4cb7c-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="4cb7c-131">**interface**</span><span class="sxs-lookup"><span data-stu-id="4cb7c-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="4cb7c-132">**LCID**</span><span class="sxs-lookup"><span data-stu-id="4cb7c-132">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="4cb7c-133">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="4cb7c-133">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="4cb7c-134">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="4cb7c-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4cb7c-135">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="4cb7c-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4cb7c-136">**à**</span><span class="sxs-lookup"><span data-stu-id="4cb7c-136">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="4cb7c-137">**retval**</span><span class="sxs-lookup"><span data-stu-id="4cb7c-137">**retval**</span></span>](retval.md)
</dt> </dl>

 

 