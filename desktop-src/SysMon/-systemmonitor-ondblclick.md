---
title: SystemMonitor. OnDblClick, événement
description: Vous avertit quand un utilisateur double-clique sur la ligne de graphique, sur la barre d’histogramme ou sur l’élément de rapport avec le bouton gauche de la souris.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- Événement OnDblClick SysMon
- OnDblClick, événement SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, OnDblClick, événement
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103837"
---
# <a name="systemmonitorondblclick-event"></a><span data-ttu-id="8c151-106">SystemMonitor. OnDblClick, événement</span><span class="sxs-lookup"><span data-stu-id="8c151-106">SystemMonitor.OnDblClick event</span></span>

<span data-ttu-id="8c151-107">Vous avertit quand un utilisateur double-clique sur la ligne de graphique, sur la barre d’histogramme ou sur l’élément de rapport avec le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="8c151-107">Notifies you when a user double-clicks the graph line, histogram bar, or report item with the left mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c151-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c151-108">Syntax</span></span>


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="8c151-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c151-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c151-110">*index* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8c151-110">*index* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c151-111">Index du compteur sélectionné dans l’objet de collection de [**compteurs**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="8c151-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span> <span data-ttu-id="8c151-112">La valeur d’index 0 est retournée si aucun compteur n’a été sélectionné ; dans le cas contraire, l’index du compteur sélectionné est retourné.</span><span class="sxs-lookup"><span data-stu-id="8c151-112">An index value of 0 is returned if no counter was selected; otherwise, the index of the selected counter is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c151-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c151-113">Return value</span></span>

<span data-ttu-id="8c151-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8c151-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c151-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8c151-115">Remarks</span></span>

<span data-ttu-id="8c151-116">Lorsque cet événement est déclenché, le compteur sélectionné par l’utilisateur dans le graphique linéaire et l’histogramme est également sélectionné dans le volet légende.</span><span class="sxs-lookup"><span data-stu-id="8c151-116">When this event is triggered, the counter that the user selected in the line graph and histogram is also selected in the Legend pane.</span></span> <span data-ttu-id="8c151-117">Cela permet à l’utilisateur du moniteur système de voir plus facilement le compteur sélectionné lorsque plusieurs valeurs de compteur sont affichées.</span><span class="sxs-lookup"><span data-stu-id="8c151-117">This makes it easier for the user of the System Monitor to see which counter is selected when several counter values are displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c151-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c151-118">Requirements</span></span>



| <span data-ttu-id="8c151-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c151-119">Requirement</span></span> | <span data-ttu-id="8c151-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c151-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c151-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c151-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c151-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c151-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8c151-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c151-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c151-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c151-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c151-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8c151-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c151-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8c151-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





