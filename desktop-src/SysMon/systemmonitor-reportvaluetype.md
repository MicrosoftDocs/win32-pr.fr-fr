---
title: SystemMonitor. ReportValueType, propriété
description: Récupère ou définit une valeur qui détermine si les vues de l’histogramme et du rapport graphiquent la dernière valeur échantillonnée pendant l’intervalle d’échantillonnage ou une valeur calculée de l’échantillonnage, telle que la valeur de compteur moyenne ou minimale.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Propriété ReportValueType SysMon
- Propriété ReportValueType SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété ReportValueType
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942086"
---
# <a name="systemmonitorreportvaluetype-property"></a><span data-ttu-id="40994-106">SystemMonitor. ReportValueType, propriété</span><span class="sxs-lookup"><span data-stu-id="40994-106">SystemMonitor.ReportValueType property</span></span>

<span data-ttu-id="40994-107">Récupère ou définit une valeur qui détermine si les vues de l’histogramme et du rapport graphiquent la dernière valeur échantillonnée pendant l’intervalle d’échantillonnage ou une valeur calculée de l’échantillonnage, telle que la valeur de compteur moyenne ou minimale.</span><span class="sxs-lookup"><span data-stu-id="40994-107">Retrieves or sets a value that determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling, such as the average or minimum counter value.</span></span>

<span data-ttu-id="40994-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="40994-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="40994-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40994-109">Syntax</span></span>


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="40994-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="40994-110">Property value</span></span>

<span data-ttu-id="40994-111">Détermine si l’histogramme et les vues de rapport graphiquent la dernière valeur échantillonnée pendant l’intervalle d’échantillonnage ou une valeur calculée à partir de l’intervalle d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="40994-111">Determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling interval.</span></span> <span data-ttu-id="40994-112">Pour connaître les valeurs possibles, consultez [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="40994-112">For possible values, see [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span></span>

## <a name="remarks"></a><span data-ttu-id="40994-113">Notes</span><span class="sxs-lookup"><span data-stu-id="40994-113">Remarks</span></span>

<span data-ttu-id="40994-114">SYSMON ignore cette valeur et utilise [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) si [**systemmonitor. DisplayType**](systemmonitor-displaytype.md) n’est pas [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) ou **DisplayTypeConstants.sysmonReport**.</span><span class="sxs-lookup"><span data-stu-id="40994-114">SYSMON ignores this value and uses [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) if [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) or **DisplayTypeConstants.sysmonReport**.</span></span>

## <a name="requirements"></a><span data-ttu-id="40994-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40994-115">Requirements</span></span>



| <span data-ttu-id="40994-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40994-116">Requirement</span></span> | <span data-ttu-id="40994-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="40994-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40994-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40994-118">Minimum supported client</span></span><br/> | <span data-ttu-id="40994-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40994-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="40994-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40994-120">Minimum supported server</span></span><br/> | <span data-ttu-id="40994-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40994-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40994-122">DLL</span><span class="sxs-lookup"><span data-stu-id="40994-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40994-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="40994-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40994-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40994-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40994-125">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="40994-125">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





