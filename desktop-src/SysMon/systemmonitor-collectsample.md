---
title: Méthode SystemMonitor CollectSample
description: Échantillonne une valeur pour chaque compteur dans l’objet compteurs.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Méthode CollectSample SysMon
- Méthode CollectSample SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, méthode CollectSample
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465562"
---
# <a name="systemmonitorcollectsample-method"></a><span data-ttu-id="a98a8-106">SystemMonitor :: CollectSample, méthode</span><span class="sxs-lookup"><span data-stu-id="a98a8-106">SystemMonitor::CollectSample method</span></span>

<span data-ttu-id="a98a8-107">Échantillonne une valeur pour chaque compteur dans l’objet [**compteurs**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="a98a8-107">Samples a value for each counter in the [**Counters**](counters.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a98a8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a98a8-108">Syntax</span></span>


```VB
Sub CollectSample()
```



## <a name="parameters"></a><span data-ttu-id="a98a8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a98a8-109">Parameters</span></span>

<span data-ttu-id="a98a8-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a98a8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a98a8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a98a8-111">Return value</span></span>

<span data-ttu-id="a98a8-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a98a8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a98a8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a98a8-113">Remarks</span></span>

<span data-ttu-id="a98a8-114">Appelez **CollectSample** uniquement si [**ManualUpdate**](systemmonitor-manualupdate.md) a la valeur true et si vous échantillonnez des valeurs de compteur à partir de l’activité actuelle de l’ordinateur, n’utilisez pas cette méthode lors de l’échantillonnage à partir d’un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="a98a8-114">Call **CollectSample** only if [**ManualUpdate**](systemmonitor-manualupdate.md) is True and you are sampling counter values from the current activity of the computer do not use this method when sampling from a log file.</span></span> <span data-ttu-id="a98a8-115">Le graphique ou le rapport est mis à jour avec la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="a98a8-115">The graph or report is updated with the new value.</span></span> <span data-ttu-id="a98a8-116">Notez que certains types de graphiques ont besoin de deux échantillons pour représenter graphiquement les données, par exemple, le graphique en courbes.</span><span class="sxs-lookup"><span data-stu-id="a98a8-116">Note that some types of graphs need two samples in order to graph the data, for example, the line graph.</span></span>

<span data-ttu-id="a98a8-117">Pour recevoir une notification lorsque l’exemple a été collecté, implémentez l’événement [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) .</span><span class="sxs-lookup"><span data-stu-id="a98a8-117">To receive notification when the sample has been collected, implement the [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="a98a8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a98a8-118">Requirements</span></span>



| <span data-ttu-id="a98a8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a98a8-119">Requirement</span></span> | <span data-ttu-id="a98a8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a98a8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a98a8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a98a8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a98a8-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a98a8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a98a8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a98a8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a98a8-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a98a8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a98a8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a98a8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a98a8-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a98a8-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a98a8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a98a8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a98a8-128">**Counters**</span><span class="sxs-lookup"><span data-stu-id="a98a8-128">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="a98a8-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="a98a8-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





