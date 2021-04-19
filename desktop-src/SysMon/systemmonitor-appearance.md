---
title: SystemMonitor. Appearance, propriété
description: Récupère ou définit l’apparence du contrôle pour inclure ou omettre les effets d’affichage en trois dimensions.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Propriété d’apparence SysMon
- Propriété Appearance SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété Appearance
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510117"
---
# <a name="systemmonitorappearance-property"></a><span data-ttu-id="e8a72-106">SystemMonitor. Appearance, propriété</span><span class="sxs-lookup"><span data-stu-id="e8a72-106">SystemMonitor.Appearance property</span></span>

<span data-ttu-id="e8a72-107">Récupère ou définit l’apparence du contrôle pour inclure ou omettre les effets d’affichage en trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="e8a72-107">Retrieves or sets the control's appearance to include or omit three-dimensional display effects.</span></span>

<span data-ttu-id="e8a72-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e8a72-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a72-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8a72-109">Syntax</span></span>


```VB
Property Appearance As Long
```



## <a name="property-value"></a><span data-ttu-id="e8a72-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e8a72-110">Property value</span></span>

<span data-ttu-id="e8a72-111">Valeur d’apparence qui détermine si le contrôle est peint avec des effets en trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="e8a72-111">Appearance value that determines if the control is painted with three-dimensional effects.</span></span>

<span data-ttu-id="e8a72-112">Vous pouvez définir cette propriété sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e8a72-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="e8a72-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8a72-113">Value</span></span>                                                                        | <span data-ttu-id="e8a72-114">Signification</span><span class="sxs-lookup"><span data-stu-id="e8a72-114">Meaning</span></span>                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8a72-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e8a72-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="e8a72-116">Peint le contrôle sans effets visuels.</span><span class="sxs-lookup"><span data-stu-id="e8a72-116">Paints the control without visual effects.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e8a72-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e8a72-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="e8a72-118">Peint le contrôle avec des effets en trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="e8a72-118">Paints the control with three-dimensional effects.</span></span> <span data-ttu-id="e8a72-119">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e8a72-119">This is the default value.</span></span><br/> |



 

## <a name="exceptions"></a><span data-ttu-id="e8a72-120">Exceptions</span><span class="sxs-lookup"><span data-stu-id="e8a72-120">Exceptions</span></span>



| <span data-ttu-id="e8a72-121">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="e8a72-121">Exception type</span></span>               | <span data-ttu-id="e8a72-122">Condition</span><span class="sxs-lookup"><span data-stu-id="e8a72-122">Condition</span></span>                                    |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="e8a72-123">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="e8a72-123">**System.ArgumentException**</span></span> | <span data-ttu-id="e8a72-124">La valeur d’apparence spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e8a72-124">The specified appearance value is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e8a72-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e8a72-125">Remarks</span></span>

<span data-ttu-id="e8a72-126">Il s’agit d’une propriété ambiante.</span><span class="sxs-lookup"><span data-stu-id="e8a72-126">This is an ambient property.</span></span> <span data-ttu-id="e8a72-127">La valeur de cette propriété est déterminée par le conteneur.</span><span class="sxs-lookup"><span data-stu-id="e8a72-127">The value of this property is determined by the container.</span></span> <span data-ttu-id="e8a72-128">La définition de la valeur de cette propriété peut affecter l’illusion du contrôle et du conteneur en tant qu’application unique.</span><span class="sxs-lookup"><span data-stu-id="e8a72-128">Setting the value of this property could affect the illusion of the control and container being a single application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a72-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8a72-129">Requirements</span></span>



| <span data-ttu-id="e8a72-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8a72-130">Requirement</span></span> | <span data-ttu-id="e8a72-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8a72-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a72-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8a72-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a72-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8a72-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e8a72-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8a72-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a72-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8a72-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8a72-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e8a72-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8a72-137"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e8a72-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a72-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8a72-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a72-139">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="e8a72-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





