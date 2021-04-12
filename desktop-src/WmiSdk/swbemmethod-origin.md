---
description: La propriété Origin de l’objet SWbemMethod retourne le nom de la classe dans laquelle cette méthode a été introduite.
ms.assetid: da98393b-af95-47ad-b589-663063f65afb
ms.tgt_platform: multiple
title: Propriété SWbemMethod. Origin (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.Origin
- ISWbemMethod.Origin
- ISWbemMethod.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1b903a2c55bbd571a9cd1f36a51812a70c123cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202161"
---
# <a name="swbemmethodorigin-property"></a><span data-ttu-id="e1e40-103">SWbemMethod. Origin, propriété</span><span class="sxs-lookup"><span data-stu-id="e1e40-103">SWbemMethod.Origin property</span></span>

<span data-ttu-id="e1e40-104">La propriété **origin** de l’objet [**SWbemMethod**](swbemmethod.md) retourne le nom de la classe dans laquelle cette méthode a été introduite.</span><span class="sxs-lookup"><span data-stu-id="e1e40-104">The **Origin** property of the [**SWbemMethod**](swbemmethod.md) object returns the name of the class in which this method was introduced.</span></span> <span data-ttu-id="e1e40-105">Pour les classes avec des hiérarchies d’héritage profond, il est souvent souhaitable de savoir quelles méthodes ont été déclarées dans quelles classes.</span><span class="sxs-lookup"><span data-stu-id="e1e40-105">For classes with deep inheritance hierarchies, it is often desirable to know which methods were declared in which classes.</span></span> <span data-ttu-id="e1e40-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e1e40-106">This property is read-only.</span></span>

<span data-ttu-id="e1e40-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e1e40-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e1e40-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e1e40-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1e40-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1e40-109">Syntax</span></span>


```VB
SWbemMethod.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="e1e40-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e1e40-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="e1e40-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1e40-111">Requirements</span></span>



| <span data-ttu-id="e1e40-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1e40-112">Requirement</span></span> | <span data-ttu-id="e1e40-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1e40-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e40-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e40-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e1e40-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1e40-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e1e40-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e40-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e1e40-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1e40-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e1e40-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1e40-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1e40-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1e40-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1e40-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e1e40-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1e40-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e1e40-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e1e40-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e1e40-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1e40-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1e40-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1e40-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="e1e40-124">CLSID</span></span><br/>                    | <span data-ttu-id="e1e40-125">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="e1e40-125">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="e1e40-126">IID</span><span class="sxs-lookup"><span data-stu-id="e1e40-126">IID</span></span><br/>                      | <span data-ttu-id="e1e40-127">IID \_ ISWbemMethod</span><span class="sxs-lookup"><span data-stu-id="e1e40-127">IID\_ISWbemMethod</span></span><br/>                                                            |



 

 




