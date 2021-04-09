---
title: Méthode SystemMonitor. ScaleToFit
description: Mettre à l’échelle les valeurs de compteur pour les adapter au graphique.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Méthode ScaleToFit SysMon
- Méthode ScaleToFit SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode ScaleToFit
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741109"
---
# <a name="systemmonitorscaletofit-method"></a><span data-ttu-id="9782f-106">Méthode SystemMonitor. ScaleToFit</span><span class="sxs-lookup"><span data-stu-id="9782f-106">SystemMonitor.ScaleToFit method</span></span>

<span data-ttu-id="9782f-107">Mettre à l’échelle les valeurs de compteur pour les adapter au graphique.</span><span class="sxs-lookup"><span data-stu-id="9782f-107">Scale counter values to fit in the graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="9782f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9782f-108">Syntax</span></span>


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a><span data-ttu-id="9782f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9782f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9782f-110">*selectedCountersOnly* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9782f-110">*selectedCountersOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9782f-111">True pour mettre à l’échelle uniquement les compteurs sélectionnés ; Sinon, false pour mettre à l’échelle tous les compteurs.</span><span class="sxs-lookup"><span data-stu-id="9782f-111">True to scale only the selected counters; otherwise, false to scale all counters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9782f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9782f-112">Return value</span></span>

<span data-ttu-id="9782f-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9782f-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9782f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9782f-114">Remarks</span></span>

<span data-ttu-id="9782f-115">Cette méthode efface la vue du graphique.</span><span class="sxs-lookup"><span data-stu-id="9782f-115">This method will clear the graph view.</span></span> <span data-ttu-id="9782f-116">SYSMON utilise ensuite le facteur d’échelle spécifié pour chaque compteur pour redessiner le graphique si la source de données est un fichier journal, ou commence à représenter graphiquement les nouvelles valeurs de compteur si la source de données est une activité en temps réel.</span><span class="sxs-lookup"><span data-stu-id="9782f-116">SYSMON then uses the scale factor specified for each counter to redraw the graph if the data source is a log file, or begin graphing new counter values if the data source is real time activity.</span></span>

## <a name="requirements"></a><span data-ttu-id="9782f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9782f-117">Requirements</span></span>



| <span data-ttu-id="9782f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9782f-118">Requirement</span></span> | <span data-ttu-id="9782f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9782f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9782f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9782f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9782f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9782f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9782f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9782f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9782f-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9782f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9782f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9782f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9782f-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="9782f-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9782f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9782f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9782f-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="9782f-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="9782f-128">**CounterItem. ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="9782f-128">**CounterItem.ScaleFactor**</span></span>](counteritem-scalefactor.md)
</dt> <dt>

[<span data-ttu-id="9782f-129">**CounterItem. Selected**</span><span class="sxs-lookup"><span data-stu-id="9782f-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





