---
title: SystemMonitor. ShowValueBar, propriété
description: Récupère ou définit une valeur qui détermine si la barre de valeur (l’ensemble de valeurs statistiques sous le graphique) est affichée sur le contrôle.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Propriété ShowValueBar SysMon
- Propriété ShowValueBar SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, propriété ShowValueBar
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740621"
---
# <a name="systemmonitorshowvaluebar-property"></a><span data-ttu-id="b1a48-106">SystemMonitor. ShowValueBar, propriété</span><span class="sxs-lookup"><span data-stu-id="b1a48-106">SystemMonitor.ShowValueBar property</span></span>

<span data-ttu-id="b1a48-107">Récupère ou définit une valeur qui détermine si la barre de valeur (l’ensemble de valeurs statistiques sous le graphique) est affichée sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b1a48-107">Retrieves or sets a value that determines whether the value bar (the set of statistical values below the graph) is displayed on the control.</span></span>

<span data-ttu-id="b1a48-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b1a48-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a48-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1a48-109">Syntax</span></span>


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b1a48-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b1a48-110">Property value</span></span>

<span data-ttu-id="b1a48-111">True indique que la barre de valeurs est affichée sur le contrôle ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="b1a48-111">True indicates that the value bar is displayed on the control; otherwise false.</span></span> <span data-ttu-id="b1a48-112">La valeur par défaut de cette propriété est True.</span><span class="sxs-lookup"><span data-stu-id="b1a48-112">The default value for this property is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1a48-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b1a48-113">Remarks</span></span>

<span data-ttu-id="b1a48-114">Les statistiques affichées incluent la dernière valeur, la valeur moyenne et les valeurs minimale et maximale du compteur actuellement sélectionné sur l’intervalle de temps affiché.</span><span class="sxs-lookup"><span data-stu-id="b1a48-114">The displayed statistics include the last value, the average value, and the minimum and maximum values of the currently selected counter over the displayed time interval.</span></span> <span data-ttu-id="b1a48-115">Pour sélectionner les valeurs de compteur à afficher, l’utilisateur doit sélectionner le compteur dans le volet légende du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b1a48-115">To select the counter values to display, the user must select the counter in the Legend pane of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1a48-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1a48-116">Requirements</span></span>



| <span data-ttu-id="b1a48-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1a48-117">Requirement</span></span> | <span data-ttu-id="b1a48-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1a48-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a48-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1a48-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a48-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1a48-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b1a48-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1a48-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a48-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1a48-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1a48-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b1a48-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1a48-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b1a48-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1a48-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1a48-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a48-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="b1a48-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





