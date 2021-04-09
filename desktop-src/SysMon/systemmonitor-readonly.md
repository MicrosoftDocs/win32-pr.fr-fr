---
title: SystemMonitor. ReadOnly, propriété
description: Récupère ou définit une valeur qui détermine si un utilisateur peut modifier les valeurs de propriété du contrôle.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Propriété ReadOnly SysMon
- Propriété ReadOnly SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété ReadOnly
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942087"
---
# <a name="systemmonitorreadonly-property"></a><span data-ttu-id="17e6a-106">SystemMonitor. ReadOnly, propriété</span><span class="sxs-lookup"><span data-stu-id="17e6a-106">SystemMonitor.ReadOnly property</span></span>

<span data-ttu-id="17e6a-107">Récupère ou définit une valeur qui détermine si un utilisateur peut modifier les valeurs de propriété du contrôle.</span><span class="sxs-lookup"><span data-stu-id="17e6a-107">Retrieves or sets a value that determines whether a user can modify the property values of the control.</span></span>

<span data-ttu-id="17e6a-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="17e6a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e6a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17e6a-109">Syntax</span></span>


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a><span data-ttu-id="17e6a-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="17e6a-110">Property value</span></span>

<span data-ttu-id="17e6a-111">True si vous ne souhaitez pas que l’utilisateur modifie les valeurs de propriété du contrôle ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="17e6a-111">True if you do not want the user to modify the property values of the control; otherwise, false.</span></span> <span data-ttu-id="17e6a-112">La valeur par défaut est false, ce qui signifie que les utilisateurs peuvent modifier les valeurs de propriété du contrôle.</span><span class="sxs-lookup"><span data-stu-id="17e6a-112">The default value is false, meaning that users can modify the property values of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e6a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="17e6a-113">Remarks</span></span>

<span data-ttu-id="17e6a-114">Lorsque la valeur de cette propriété est true, les conditions suivantes sont appliquées :</span><span class="sxs-lookup"><span data-stu-id="17e6a-114">When the value of this property is True, the following conditions are in effect:</span></span>

-   <span data-ttu-id="17e6a-115">L’utilisateur ne peut pas utiliser le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="17e6a-115">The user cannot use the context menu.</span></span>
-   <span data-ttu-id="17e6a-116">Les boutons de barre d’outils suivants sont désactivés :</span><span class="sxs-lookup"><span data-stu-id="17e6a-116">The following toolbar buttons are disabled:</span></span>
    -   <span data-ttu-id="17e6a-117">Nouvel ensemble de compteurs</span><span class="sxs-lookup"><span data-stu-id="17e6a-117">New Counter Set</span></span>
    -   <span data-ttu-id="17e6a-118">Afficher l'activité actuelle</span><span class="sxs-lookup"><span data-stu-id="17e6a-118">View Current Activity</span></span>
    -   <span data-ttu-id="17e6a-119">Afficher les données du fichier journal</span><span class="sxs-lookup"><span data-stu-id="17e6a-119">View Log File Data</span></span>
    -   <span data-ttu-id="17e6a-120">Ajouter</span><span class="sxs-lookup"><span data-stu-id="17e6a-120">Add</span></span>
    -   <span data-ttu-id="17e6a-121">DELETE</span><span class="sxs-lookup"><span data-stu-id="17e6a-121">Delete</span></span>
    -   <span data-ttu-id="17e6a-122">Coller la liste des compteurs</span><span class="sxs-lookup"><span data-stu-id="17e6a-122">Paste Counter List</span></span>
    -   <span data-ttu-id="17e6a-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="17e6a-123">Properties</span></span>

<span data-ttu-id="17e6a-124">Notez que cette propriété affecte uniquement la capacité de l’utilisateur à modifier les valeurs de propriété par le biais de l’interface utilisateur, mais elle ne vous empêche pas de modifier par programmation les valeurs de propriété ou les compteurs.</span><span class="sxs-lookup"><span data-stu-id="17e6a-124">Note that this property affects only the user's ability to modify property values through the user interface, it does not prevent you from programmatically modifying property values or counters.</span></span>

## <a name="requirements"></a><span data-ttu-id="17e6a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17e6a-125">Requirements</span></span>



| <span data-ttu-id="17e6a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17e6a-126">Requirement</span></span> | <span data-ttu-id="17e6a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="17e6a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17e6a-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17e6a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="17e6a-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17e6a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="17e6a-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17e6a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="17e6a-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17e6a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17e6a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="17e6a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17e6a-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="17e6a-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17e6a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17e6a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e6a-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="17e6a-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





