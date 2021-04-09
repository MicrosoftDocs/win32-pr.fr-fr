---
description: La propriété CIMType de l’objet SWbemProperty est un entier qui peut être utilisé pour déterminer le type CIM de cette propriété. Cette propriété est en lecture seule.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: SWbemProperty. CIMType, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952152"
---
# <a name="swbempropertycimtype-property"></a><span data-ttu-id="efe1b-104">SWbemProperty. CIMType, propriété</span><span class="sxs-lookup"><span data-stu-id="efe1b-104">SWbemProperty.CIMType property</span></span>

<span data-ttu-id="efe1b-105">La propriété **CimType** de l’objet [**SWbemProperty**](swbemproperty.md) est un entier qui peut être utilisé pour déterminer le type CIM de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="efe1b-105">The **CIMType** property of the [**SWbemProperty**](swbemproperty.md) object is an integer that can be used to determine the CIM type of this property.</span></span> <span data-ttu-id="efe1b-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="efe1b-106">This property is read-only.</span></span>

<span data-ttu-id="efe1b-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="efe1b-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="efe1b-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="efe1b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe1b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efe1b-109">Syntax</span></span>


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a><span data-ttu-id="efe1b-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="efe1b-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="efe1b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="efe1b-111">Remarks</span></span>

<span data-ttu-id="efe1b-112">Pour plus d’informations sur les types valides pour cette propriété, consultez [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="efe1b-112">For more information about valid types for this property, see [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>

<span data-ttu-id="efe1b-113">Les instances d’objets incorporés sont stockées dans des objets composites en tant que propriétés de type **\_ objet CIM**.</span><span class="sxs-lookup"><span data-stu-id="efe1b-113">Instances of embedded objects are stored in composite objects as properties of type **CIM\_OBJECT**.</span></span> <span data-ttu-id="efe1b-114">Pour déterminer la classe d’un objet incorporé dans une instance d’une classe composite, vous devez examiner le qualificateur **CimType** de la propriété type d' **\_ objet CIM** .</span><span class="sxs-lookup"><span data-stu-id="efe1b-114">To determine the class of an embedded object in an instance of a composite class, you must examine the **CIMType** qualifier of the **CIM\_OBJECT** type property.</span></span>

<span data-ttu-id="efe1b-115">Les références d’objet dans une classe d’association sont stockées dans des propriétés de type **\_ référence CIM**.</span><span class="sxs-lookup"><span data-stu-id="efe1b-115">The object references in an association class are stored in properties of type **CIM\_REFERENCE**.</span></span> <span data-ttu-id="efe1b-116">Pour déterminer les chemins d’accès aux objets réels, vous devez examiner le qualificateur **CimType** de la propriété type de **\_ référence CIM** .</span><span class="sxs-lookup"><span data-stu-id="efe1b-116">To determine the actual object paths you must examine the **CIMType** qualifier of the **CIM\_REFERENCE** type property.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe1b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efe1b-117">Requirements</span></span>



| <span data-ttu-id="efe1b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efe1b-118">Requirement</span></span> | <span data-ttu-id="efe1b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="efe1b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efe1b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efe1b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="efe1b-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efe1b-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="efe1b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efe1b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="efe1b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efe1b-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="efe1b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="efe1b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="efe1b-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="efe1b-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="efe1b-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="efe1b-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="efe1b-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="efe1b-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="efe1b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="efe1b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efe1b-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efe1b-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="efe1b-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="efe1b-130">CLSID</span></span><br/>                    | <span data-ttu-id="efe1b-131">CLSID \_ SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="efe1b-131">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="efe1b-132">IID</span><span class="sxs-lookup"><span data-stu-id="efe1b-132">IID</span></span><br/>                      | <span data-ttu-id="efe1b-133">IID \_ ISWbemProperty</span><span class="sxs-lookup"><span data-stu-id="efe1b-133">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




