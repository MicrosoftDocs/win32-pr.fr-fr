---
description: La propriété Value de l’objet SWbemProperty définit la valeur de type variant de la propriété WMI. Il s’agit de la propriété Automation par défaut de cet objet.
ms.assetid: 547ec691-ff1c-4a6d-bee8-54e73d21cc93
ms.tgt_platform: multiple
title: SWbemProperty. Value, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Value
- ISWbemProperty.Value
- ISWbemProperty.get_Value
- ISWbemProperty.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e203929d0ce6ce98deff5ea89f9f226cd4cebfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952151"
---
# <a name="swbempropertyvalue-property"></a><span data-ttu-id="15e3d-104">SWbemProperty. Value (propriété)</span><span class="sxs-lookup"><span data-stu-id="15e3d-104">SWbemProperty.Value property</span></span>

<span data-ttu-id="15e3d-105">La propriété **value** de l’objet [**SWbemProperty**](swbemproperty.md) définit la valeur de type variant de la propriété WMI.</span><span class="sxs-lookup"><span data-stu-id="15e3d-105">The **Value** property of the [**SWbemProperty**](swbemproperty.md) object defines the variant value of the WMI property.</span></span> <span data-ttu-id="15e3d-106">Il s’agit de la propriété Automation par défaut de cet objet.</span><span class="sxs-lookup"><span data-stu-id="15e3d-106">This is the default automation property of this object.</span></span>

<span data-ttu-id="15e3d-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="15e3d-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="15e3d-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="15e3d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e3d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15e3d-109">Syntax</span></span>


```VB
SWbemProperty.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="15e3d-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="15e3d-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="15e3d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15e3d-111">Requirements</span></span>



| <span data-ttu-id="15e3d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15e3d-112">Requirement</span></span> | <span data-ttu-id="15e3d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="15e3d-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15e3d-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15e3d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="15e3d-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15e3d-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15e3d-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15e3d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="15e3d-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15e3d-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15e3d-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="15e3d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="15e3d-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="15e3d-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15e3d-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="15e3d-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="15e3d-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15e3d-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15e3d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="15e3d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15e3d-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15e3d-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="15e3d-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="15e3d-124">CLSID</span></span><br/>                    | <span data-ttu-id="15e3d-125">CLSID \_ SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="15e3d-125">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="15e3d-126">IID</span><span class="sxs-lookup"><span data-stu-id="15e3d-126">IID</span></span><br/>                      | <span data-ttu-id="15e3d-127">IID \_ ISWbemProperty</span><span class="sxs-lookup"><span data-stu-id="15e3d-127">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




