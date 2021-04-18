---
title: nonextensible, attribut
description: L’attribut \ non extensible \ spécifie que l’implémentation IDispatch comprend uniquement les propriétés et les méthodes listées dans la description de l’interface et ne peut pas être étendue avec des membres supplémentaires au moment de l’exécution.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- MIDL d’attribut unextensible
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512305"
---
# <a name="nonextensible-attribute"></a><span data-ttu-id="c94ea-104">nonextensible, attribut</span><span class="sxs-lookup"><span data-stu-id="c94ea-104">nonextensible attribute</span></span>

<span data-ttu-id="c94ea-105">L’attribut non **\[ \] extensible** spécifie que l’implémentation [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) comprend uniquement les propriétés et les méthodes listées dans la description de l’interface et ne peut pas être étendue avec des membres supplémentaires au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c94ea-105">The **\[nonextensible\]** attribute specifies that the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) implementation includes only the properties and methods listed in the interface description and cannot be extended with additional members at run time.</span></span> <span data-ttu-id="c94ea-106">(Par défaut, Automation suppose que les interfaces peuvent ajouter des membres au moment de l’exécution ; autrement dit, elles sont extensibles.)</span><span class="sxs-lookup"><span data-stu-id="c94ea-106">(By default, Automation assumes that interfaces may add members at run time; that is, it assumes they are extensible.)</span></span>

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="c94ea-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c94ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c94ea-108">*UUID-Number*</span><span class="sxs-lookup"><span data-stu-id="c94ea-108">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="c94ea-109">Spécifie un numéro d’identification unique universel pour l' [**interface**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="c94ea-109">Specifies a universally unique identification number for the [**interface**](interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="c94ea-110">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="c94ea-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c94ea-111">Spécifie une liste de zéro, un ou plusieurs attributs d’interface MIDL.</span><span class="sxs-lookup"><span data-stu-id="c94ea-111">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="c94ea-112">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="c94ea-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c94ea-113">Spécifie le nom de l' [**interface**](interface.md) ou de [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="c94ea-113">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="c94ea-114">*définition d’interface*</span><span class="sxs-lookup"><span data-stu-id="c94ea-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="c94ea-115">Spécifie les instructions IDL qui forment la définition de l' [**interface**](interface.md) ou de [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="c94ea-115">Specifies IDL statements that form the definition of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c94ea-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c94ea-116">Remarks</span></span>

<span data-ttu-id="c94ea-117">Vous pouvez appliquer l’attribut non **\[ extensible \]** à une interface ou une dispinterface.</span><span class="sxs-lookup"><span data-stu-id="c94ea-117">You can apply the **\[nonextensible\]** attribute to either an interface or a dispinterface.</span></span> <span data-ttu-id="c94ea-118">Toutefois, une interface doit également avoir les **\[** attributs [**Dual**](dual.md) **\]** et **\[** [**oleautomation**](oleautomation.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="c94ea-118">However, an interface must also have the **\[**[**dual**](dual.md)**\]** and **\[**[**oleautomation**](oleautomation.md)**\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="c94ea-119">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="c94ea-119">Flags</span></span>

<span data-ttu-id="c94ea-120">TYPEFLAG \_ FNONEXTENSIBLE</span><span class="sxs-lookup"><span data-stu-id="c94ea-120">TYPEFLAG\_FNONEXTENSIBLE</span></span>

## <a name="examples"></a><span data-ttu-id="c94ea-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="c94ea-121">Examples</span></span>

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c94ea-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c94ea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c94ea-123">Contenu d’une bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c94ea-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="c94ea-124">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="c94ea-124">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="c94ea-125">**double**</span><span class="sxs-lookup"><span data-stu-id="c94ea-125">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="c94ea-126">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="c94ea-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="c94ea-127">**interface**</span><span class="sxs-lookup"><span data-stu-id="c94ea-127">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="c94ea-128">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="c94ea-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c94ea-129">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="c94ea-129">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="c94ea-130">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="c94ea-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 