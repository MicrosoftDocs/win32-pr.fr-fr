---
title: Méthode CounterItem. GetDataAt
description: Récupère la valeur de compteur spécifiée à partir d’un point spécifique du graphique.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Méthode GetDataAt SysMon
- Méthode GetDataAt SysMon, objet CounterItem
- Objet CounterItem SysMon, méthode GetDataAt
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508670"
---
# <a name="counteritemgetdataat-method"></a><span data-ttu-id="591ca-106">Méthode CounterItem. GetDataAt</span><span class="sxs-lookup"><span data-stu-id="591ca-106">CounterItem.GetDataAt method</span></span>

<span data-ttu-id="591ca-107">Récupère la valeur de compteur spécifiée à partir d’un point spécifique du graphique.</span><span class="sxs-lookup"><span data-stu-id="591ca-107">Retrieves the specified counter value from a specific point in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="591ca-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="591ca-108">Syntax</span></span>


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="591ca-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="591ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="591ca-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="591ca-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591ca-111">Index de base zéro du point de graphique dont vous souhaitez récupérer la valeur.</span><span class="sxs-lookup"><span data-stu-id="591ca-111">Zero-based index of the graph point whose value you want to retrieve.</span></span> <span data-ttu-id="591ca-112">Les valeurs valides sont comprises entre 0 et ([**systemmonitor. DataPointCount**](systemmonitor-datapointcount.md) -1).</span><span class="sxs-lookup"><span data-stu-id="591ca-112">Valid values range from 0 to ([**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md) - 1).</span></span>

</dd> <dt>

<span data-ttu-id="591ca-113">*qui* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="591ca-113">*which* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591ca-114">Type de valeur de compteur à récupérer, par exemple, la valeur moyenne du compteur tel qu’il s’affiche dans la fenêtre du graphique.</span><span class="sxs-lookup"><span data-stu-id="591ca-114">Type of counter value to retrieve, for example, the average value of the counter as displayed in the graph window.</span></span> <span data-ttu-id="591ca-115">Pour connaître les valeurs possibles, consultez [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span><span class="sxs-lookup"><span data-stu-id="591ca-115">For possible values, see [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).</span></span>

</dd> <dt>

<span data-ttu-id="591ca-116">*variante* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="591ca-116">*variant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="591ca-117">Valeur de compteur qui a été récupérée.</span><span class="sxs-lookup"><span data-stu-id="591ca-117">Counter value that was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="591ca-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="591ca-118">Return value</span></span>

<span data-ttu-id="591ca-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="591ca-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="591ca-120">Notes</span><span class="sxs-lookup"><span data-stu-id="591ca-120">Remarks</span></span>

<span data-ttu-id="591ca-121">Utilisez cette méthode uniquement si</span><span class="sxs-lookup"><span data-stu-id="591ca-121">Use this method only if</span></span>

-   <span data-ttu-id="591ca-122">[**Systemmonitor. DisplayType**](systemmonitor-displaytype.md) a la valeur sysmonLineGraph</span><span class="sxs-lookup"><span data-stu-id="591ca-122">[**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is set to sysmonLineGraph</span></span>
-   <span data-ttu-id="591ca-123">[**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est défini sur SysmonLogFiles ou sysmonSqlLog</span><span class="sxs-lookup"><span data-stu-id="591ca-123">[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles or sysmonSqlLog</span></span>

## <a name="requirements"></a><span data-ttu-id="591ca-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="591ca-124">Requirements</span></span>



| <span data-ttu-id="591ca-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="591ca-125">Requirement</span></span> | <span data-ttu-id="591ca-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="591ca-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="591ca-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="591ca-127">Minimum supported client</span></span><br/> | <span data-ttu-id="591ca-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="591ca-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="591ca-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="591ca-129">Minimum supported server</span></span><br/> | <span data-ttu-id="591ca-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="591ca-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="591ca-131">DLL</span><span class="sxs-lookup"><span data-stu-id="591ca-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="591ca-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="591ca-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="591ca-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="591ca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="591ca-134">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="591ca-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="591ca-135">**CounterItem.GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="591ca-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="591ca-136">**CounterItem. GetValue**</span><span class="sxs-lookup"><span data-stu-id="591ca-136">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





