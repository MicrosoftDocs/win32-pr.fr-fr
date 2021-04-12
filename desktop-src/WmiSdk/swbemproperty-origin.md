---
description: La propriété Origin de l’objet SWbemProperty récupère le nom de la classe WMI dans laquelle cette propriété a été introduite. Pour les classes avec des hiérarchies d’héritage profond, il est souvent souhaitable de savoir quelles propriétés ont été déclarées dans quelles classes.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Propriété SWbemProperty. Origin (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203155"
---
# <a name="swbempropertyorigin-property"></a><span data-ttu-id="f36ff-104">SWbemProperty. Origin, propriété</span><span class="sxs-lookup"><span data-stu-id="f36ff-104">SWbemProperty.Origin property</span></span>

<span data-ttu-id="f36ff-105">La propriété **origin** de l’objet [**SWbemProperty**](swbemproperty.md) récupère le nom de la classe WMI dans laquelle cette propriété a été introduite.</span><span class="sxs-lookup"><span data-stu-id="f36ff-105">The **Origin** property of the [**SWbemProperty**](swbemproperty.md) object retrieves the name of the WMI class in which this property was introduced.</span></span> <span data-ttu-id="f36ff-106">Pour les classes avec des hiérarchies d’héritage profond, il est souvent souhaitable de savoir quelles propriétés ont été déclarées dans quelles classes.</span><span class="sxs-lookup"><span data-stu-id="f36ff-106">For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes.</span></span>

<span data-ttu-id="f36ff-107">Si la propriété est locale (consultez [**SWbemQualifier. IsLocal**](swbemqualifier-islocal.md)), cette valeur est la même que la classe propriétaire.</span><span class="sxs-lookup"><span data-stu-id="f36ff-107">If the property is local (see [**SWbemQualifier.IsLocal**](swbemqualifier-islocal.md)), this value is the same as the owning class.</span></span> <span data-ttu-id="f36ff-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f36ff-108">This property is read-only.</span></span>

<span data-ttu-id="f36ff-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f36ff-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f36ff-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f36ff-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36ff-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f36ff-111">Syntax</span></span>


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="f36ff-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f36ff-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="f36ff-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f36ff-113">Requirements</span></span>



| <span data-ttu-id="f36ff-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f36ff-114">Requirement</span></span> | <span data-ttu-id="f36ff-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f36ff-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f36ff-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f36ff-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f36ff-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f36ff-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f36ff-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f36ff-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f36ff-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f36ff-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f36ff-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f36ff-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f36ff-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f36ff-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f36ff-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f36ff-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="f36ff-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f36ff-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f36ff-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f36ff-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f36ff-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f36ff-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f36ff-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="f36ff-126">CLSID</span></span><br/>                    | <span data-ttu-id="f36ff-127">CLSID \_ SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="f36ff-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="f36ff-128">IID</span><span class="sxs-lookup"><span data-stu-id="f36ff-128">IID</span></span><br/>                      | <span data-ttu-id="f36ff-129">IID \_ ISWbemProperty</span><span class="sxs-lookup"><span data-stu-id="f36ff-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




