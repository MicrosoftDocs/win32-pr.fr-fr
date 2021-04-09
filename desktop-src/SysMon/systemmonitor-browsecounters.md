---
title: Méthode SystemMonitor BrowseCounters
description: Affiche la boîte de dialogue Ajouter des compteurs.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Méthode BrowseCounters SysMon
- Méthode BrowseCounters SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, méthode BrowseCounters
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032316"
---
# <a name="systemmonitorbrowsecounters-method"></a><span data-ttu-id="39eb8-106">SystemMonitor :: BrowseCounters, méthode</span><span class="sxs-lookup"><span data-stu-id="39eb8-106">SystemMonitor::BrowseCounters method</span></span>

<span data-ttu-id="39eb8-107">Affiche la boîte de dialogue **Ajouter des compteurs** .</span><span class="sxs-lookup"><span data-stu-id="39eb8-107">Displays the **Add Counters** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="39eb8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39eb8-108">Syntax</span></span>


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a><span data-ttu-id="39eb8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39eb8-109">Parameters</span></span>

<span data-ttu-id="39eb8-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="39eb8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39eb8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39eb8-111">Return value</span></span>

<span data-ttu-id="39eb8-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="39eb8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39eb8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="39eb8-113">Remarks</span></span>

<span data-ttu-id="39eb8-114">Cette boîte de dialogue permet à l’utilisateur de sélectionner des compteurs de performance locaux ou distants dans une liste d’objets de performance.</span><span class="sxs-lookup"><span data-stu-id="39eb8-114">This dialog box lets the user select local or remote performance counters from a list of performance objects.</span></span> <span data-ttu-id="39eb8-115">Les compteurs sélectionnés sont ajoutés à la collection de [**compteurs**](counters.md) et s’affichent dans le graphique ou le rapport.</span><span class="sxs-lookup"><span data-stu-id="39eb8-115">The selected counters are added to the [**Counters**](counters.md) collection and displayed in the graph or report.</span></span>

<span data-ttu-id="39eb8-116">Pour recevoir une notification lorsqu’un compteur est ajouté, implémentez l’événement [**OnCounterAdded**](systemmonitor-oncounteradded.md) .</span><span class="sxs-lookup"><span data-stu-id="39eb8-116">To receive notification when a counter is added, implement the [**OnCounterAdded**](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="39eb8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39eb8-117">Requirements</span></span>



| <span data-ttu-id="39eb8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39eb8-118">Requirement</span></span> | <span data-ttu-id="39eb8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="39eb8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39eb8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39eb8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="39eb8-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39eb8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="39eb8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39eb8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="39eb8-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39eb8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39eb8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="39eb8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39eb8-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="39eb8-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39eb8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39eb8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39eb8-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="39eb8-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="39eb8-128">**Compteurs. Add**</span><span class="sxs-lookup"><span data-stu-id="39eb8-128">**Counters.Add**</span></span>](counters-add.md)
</dt> </dl>

 

 





