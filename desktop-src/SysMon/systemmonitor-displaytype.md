---
title: SystemMonitor. DisplayType, propriété
description: Récupère ou définit le type de graphique utilisé pour représenter graphiquement les données du compteur de performance.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- Propriété DisplayType SysMon
- Propriété DisplayType SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété DisplayType
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103834"
---
# <a name="systemmonitordisplaytype-property"></a><span data-ttu-id="f9003-106">SystemMonitor. DisplayType, propriété</span><span class="sxs-lookup"><span data-stu-id="f9003-106">SystemMonitor.DisplayType property</span></span>

<span data-ttu-id="f9003-107">Récupère ou définit le type de graphique utilisé pour représenter graphiquement les données du compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="f9003-107">Retrieves or sets the type of graph used to graph the performance counter data.</span></span>

<span data-ttu-id="f9003-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f9003-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9003-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9003-109">Syntax</span></span>


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="f9003-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f9003-110">Property value</span></span>

<span data-ttu-id="f9003-111">Type de graphique utilisé pour représenter graphiquement les données du compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="f9003-111">Type of graph used to graph the performance counter data.</span></span> <span data-ttu-id="f9003-112">Pour connaître les valeurs possibles, consultez [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="f9003-112">For possible values, see [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="f9003-113">Exceptions</span><span class="sxs-lookup"><span data-stu-id="f9003-113">Exceptions</span></span>



| <span data-ttu-id="f9003-114">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="f9003-114">Exception type</span></span>               | <span data-ttu-id="f9003-115">Condition</span><span class="sxs-lookup"><span data-stu-id="f9003-115">Condition</span></span>                                         |
|------------------------------|---------------------------------------------------|
| <span data-ttu-id="f9003-116">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="f9003-116">**System.ArgumentException**</span></span> | <span data-ttu-id="f9003-117">Le graphique ou la valeur de rapport spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f9003-117">The specified graph or report value is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f9003-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9003-118">Requirements</span></span>



| <span data-ttu-id="f9003-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9003-119">Requirement</span></span> | <span data-ttu-id="f9003-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9003-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9003-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9003-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f9003-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9003-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f9003-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9003-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f9003-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9003-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9003-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f9003-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9003-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f9003-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9003-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9003-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9003-128">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="f9003-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





