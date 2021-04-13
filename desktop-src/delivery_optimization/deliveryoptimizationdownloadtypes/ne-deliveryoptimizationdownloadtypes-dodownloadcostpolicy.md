---
title: Énumération DODownloadCostPolicy
description: Spécifie l’ID des options de stratégie de coût associées à la propriété **DODownloadProperty_CostPolicy** .
keywords:
- Énumération DODownloadCostPolicy, DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383999"
---
# <a name="dodownloadcostpolicy-enumeration"></a><span data-ttu-id="23459-104">Énumération DODownloadCostPolicy</span><span class="sxs-lookup"><span data-stu-id="23459-104">DODownloadCostPolicy enumeration</span></span>

<span data-ttu-id="23459-105">L’énumération **DODownloadCostPolicy** spécifie l’ID des options de stratégie de coût associées à la propriété **DODownloadProperty_CostPolicy** .</span><span class="sxs-lookup"><span data-stu-id="23459-105">The **DODownloadCostPolicy** enumeration specifies the ID of cost policies options associated with the **DODownloadProperty_CostPolicy** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="23459-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23459-106">Syntax</span></span>

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a><span data-ttu-id="23459-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="23459-107">Constants</span></span>

| <span data-ttu-id="23459-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23459-108">Requirement</span></span> | <span data-ttu-id="23459-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="23459-109">Value</span></span> |
|-|-|
| <span data-ttu-id="23459-110">DODownloadCostPolicy_Always</span><span class="sxs-lookup"><span data-stu-id="23459-110">DODownloadCostPolicy_Always</span></span> | <span data-ttu-id="23459-111">Les exécutions sont téléchargées quel que soit le coût.</span><span class="sxs-lookup"><span data-stu-id="23459-111">Download runs regardless of the cost.</span></span> |
| <span data-ttu-id="23459-112">DODownloadCostPolicy_Unrestricted</span><span class="sxs-lookup"><span data-stu-id="23459-112">DODownloadCostPolicy_Unrestricted</span></span> | <span data-ttu-id="23459-113">Le téléchargement s’effectue à moins que n’impose des coûts ou des limites de trafic.</span><span class="sxs-lookup"><span data-stu-id="23459-113">Download runs unless imposes costs or traffic limits.</span></span> |
| <span data-ttu-id="23459-114">DODownloadCostPolicy_Standard</span><span class="sxs-lookup"><span data-stu-id="23459-114">DODownloadCostPolicy_Standard</span></span> | <span data-ttu-id="23459-115">Le téléchargement s’effectue à moins qu’il ne soit soumis à une surcharge ou à une épuisement.</span><span class="sxs-lookup"><span data-stu-id="23459-115">Download runs unless neither subject to a surcharge nor near exhaustion.</span></span> |
| <span data-ttu-id="23459-116">DODownloadCostPolicy_NoRoaming</span><span class="sxs-lookup"><span data-stu-id="23459-116">DODownloadCostPolicy_NoRoaming</span></span> | <span data-ttu-id="23459-117">Le téléchargement s’exécute à moins que cette connectivité soit sujette à des surcharges d’itinérance.</span><span class="sxs-lookup"><span data-stu-id="23459-117">Download runs unless that connectivity is subject to roaming surcharges.</span></span> |
| <span data-ttu-id="23459-118">DODownloadCostPolicy_NoSurcharge</span><span class="sxs-lookup"><span data-stu-id="23459-118">DODownloadCostPolicy_NoSurcharge</span></span> | <span data-ttu-id="23459-119">Le téléchargement s’effectue à moins qu’il ne soit soumis à une surcharge.</span><span class="sxs-lookup"><span data-stu-id="23459-119">Download runs unless subject to a surcharge.</span></span> |
| <span data-ttu-id="23459-120">DODownloadCostPolicy_NoCellular</span><span class="sxs-lookup"><span data-stu-id="23459-120">DODownloadCostPolicy_NoCellular</span></span> | <span data-ttu-id="23459-121">Le téléchargement s’exécute sauf si le réseau est sur un réseau cellulaire.</span><span class="sxs-lookup"><span data-stu-id="23459-121">Download runs unless network is on cellular.</span></span> |

## <a name="requirements"></a><span data-ttu-id="23459-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23459-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="23459-123">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="23459-123">**Minimum supported client**</span></span> | <span data-ttu-id="23459-124">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23459-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="23459-125">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="23459-125">**Minimum supported server**</span></span> | <span data-ttu-id="23459-126">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23459-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="23459-127">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="23459-127">**Header**</span></span> | <span data-ttu-id="23459-128">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="23459-128">DeliveryOptimizationDownloadTypes.h</span></span> |
