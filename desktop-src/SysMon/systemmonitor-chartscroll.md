---
title: SystemMonitor. ChartScroll, propriété
description: Récupère ou définit une valeur qui détermine si le graphique linéaire défile dans la vue.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Propriété ChartScroll SysMon
- Propriété ChartScroll SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété ChartScroll
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942230"
---
# <a name="systemmonitorchartscroll-property"></a><span data-ttu-id="a8877-106">SystemMonitor. ChartScroll, propriété</span><span class="sxs-lookup"><span data-stu-id="a8877-106">SystemMonitor.ChartScroll property</span></span>

<span data-ttu-id="a8877-107">Récupère ou définit une valeur qui détermine si le graphique linéaire défile dans la vue.</span><span class="sxs-lookup"><span data-stu-id="a8877-107">Retrieves or sets a value that determines if the line graph scrolls in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8877-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8877-108">Syntax</span></span>


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a8877-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a8877-109">Property value</span></span>

<span data-ttu-id="a8877-110">True si le graphique en courbes fait défiler en continu de droite à gauche ; Sinon, false si le graphique en courbes est dessiné de gauche à droite et s’ajuste à lui-même dans la vue.</span><span class="sxs-lookup"><span data-stu-id="a8877-110">True if the line graph scrolls continuously from right to left; otherwise, False if the line graph is drawn from left to right and wraps around on itself in the view.</span></span> <span data-ttu-id="a8877-111">False représente la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a8877-111">False is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8877-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a8877-112">Remarks</span></span>

<span data-ttu-id="a8877-113">Cette valeur est ignorée si [**systemmonitor. DisplayType**](systemmonitor-displaytype.md) n’est pas [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="a8877-113">This value is ignored if the [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8877-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8877-114">Requirements</span></span>



| <span data-ttu-id="a8877-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8877-115">Requirement</span></span> | <span data-ttu-id="a8877-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8877-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8877-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8877-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8877-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8877-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8877-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8877-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8877-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8877-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8877-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a8877-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8877-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a8877-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





