---
title: SystemMonitor. DataPointCount, propriété
description: Récupère ou définit le nombre de points de données affichés dans un graphique linéaire.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Propriété DataPointCount SysMon
- Propriété DataPointCount SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété DataPointCount
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941899"
---
# <a name="systemmonitordatapointcount-property"></a><span data-ttu-id="cff2f-106">SystemMonitor. DataPointCount, propriété</span><span class="sxs-lookup"><span data-stu-id="cff2f-106">SystemMonitor.DataPointCount property</span></span>

<span data-ttu-id="cff2f-107">Récupère ou définit le nombre de points de données affichés dans un graphique linéaire.</span><span class="sxs-lookup"><span data-stu-id="cff2f-107">Retrieves or sets the number of data points displayed in a line graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff2f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cff2f-108">Syntax</span></span>


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a><span data-ttu-id="cff2f-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cff2f-109">Property value</span></span>

<span data-ttu-id="cff2f-110">Nombre de points de données affichés dans la vue pour un graphique linéaire.</span><span class="sxs-lookup"><span data-stu-id="cff2f-110">Number of data points displayed in the view for a line graph.</span></span> <span data-ttu-id="cff2f-111">La valeur par défaut est 100 points de données.</span><span class="sxs-lookup"><span data-stu-id="cff2f-111">The default value is 100 data points.</span></span> <span data-ttu-id="cff2f-112">La plage de valeurs valide est comprise entre 2 et 1 000.</span><span class="sxs-lookup"><span data-stu-id="cff2f-112">The valid range of values is 2 to 1,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="cff2f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cff2f-113">Remarks</span></span>

<span data-ttu-id="cff2f-114">Cette propriété est utilisée uniquement si [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est **sysmonCurrentActivity**.</span><span class="sxs-lookup"><span data-stu-id="cff2f-114">This property is used only if [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is **sysmonCurrentActivity**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cff2f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cff2f-115">Requirements</span></span>



| <span data-ttu-id="cff2f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cff2f-116">Requirement</span></span> | <span data-ttu-id="cff2f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="cff2f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cff2f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cff2f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cff2f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cff2f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cff2f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cff2f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cff2f-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cff2f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cff2f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cff2f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cff2f-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="cff2f-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





