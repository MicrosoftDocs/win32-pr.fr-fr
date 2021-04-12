---
title: SystemMonitor. EnableDigitGrouping, propriété
description: Récupère ou définit une valeur qui détermine si SYSMON utilise le regroupement de chiffres lors de l’affichage de valeurs numériques.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Propriété EnableDigitGrouping SysMon
- Propriété EnableDigitGrouping SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété EnableDigitGrouping
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384716"
---
# <a name="systemmonitorenabledigitgrouping-property"></a><span data-ttu-id="a9bc9-106">SystemMonitor. EnableDigitGrouping, propriété</span><span class="sxs-lookup"><span data-stu-id="a9bc9-106">SystemMonitor.EnableDigitGrouping property</span></span>

<span data-ttu-id="a9bc9-107">Récupère ou définit une valeur qui détermine si SYSMON utilise le regroupement de chiffres lors de l’affichage de valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="a9bc9-107">Retrieves or sets a value that determines if SYSMON uses digit grouping when displaying numeric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9bc9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9bc9-108">Syntax</span></span>


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a9bc9-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a9bc9-109">Property value</span></span>

<span data-ttu-id="a9bc9-110">Si la valeur est true, SYSMON groupe les chiffres lors de l’affichage des valeurs numériques, par exemple 1 214.</span><span class="sxs-lookup"><span data-stu-id="a9bc9-110">If True, SYSMON will group digits when displaying numeric values, for example, 1,214.</span></span> <span data-ttu-id="a9bc9-111">Si la valeur est false, les valeurs numériques ne sont pas regroupées, par exemple, 1214.</span><span class="sxs-lookup"><span data-stu-id="a9bc9-111">If False, numeric values are not grouped, for example, 1214.</span></span> <span data-ttu-id="a9bc9-112">La valeur par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="a9bc9-112">True is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9bc9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a9bc9-113">Remarks</span></span>

<span data-ttu-id="a9bc9-114">Le symbole de regroupement digits est localisé.</span><span class="sxs-lookup"><span data-stu-id="a9bc9-114">The digit grouping symbol is localized.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9bc9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9bc9-115">Requirements</span></span>



| <span data-ttu-id="a9bc9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9bc9-116">Requirement</span></span> | <span data-ttu-id="a9bc9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9bc9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9bc9-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9bc9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a9bc9-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9bc9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9bc9-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9bc9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a9bc9-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9bc9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9bc9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a9bc9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9bc9-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a9bc9-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





