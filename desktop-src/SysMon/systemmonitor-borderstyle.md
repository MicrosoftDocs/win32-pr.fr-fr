---
title: SystemMonitor. BorderStyle, propriété
description: Récupère ou définit le style de bordure du contrôle.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- Propriété BorderStyle SysMon
- Propriété BorderStyle SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété BorderStyle
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843473"
---
# <a name="systemmonitorborderstyle-property"></a><span data-ttu-id="e664b-106">SystemMonitor. BorderStyle, propriété</span><span class="sxs-lookup"><span data-stu-id="e664b-106">SystemMonitor.BorderStyle property</span></span>

<span data-ttu-id="e664b-107">Récupère ou définit le style de bordure du contrôle.</span><span class="sxs-lookup"><span data-stu-id="e664b-107">Retrieves or sets the border style of the control.</span></span>

<span data-ttu-id="e664b-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e664b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e664b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e664b-109">Syntax</span></span>


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="e664b-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e664b-110">Property value</span></span>

<span data-ttu-id="e664b-111">Style de bordure du contrôle.</span><span class="sxs-lookup"><span data-stu-id="e664b-111">Border style of the control.</span></span>

<span data-ttu-id="e664b-112">Vous pouvez définir cette propriété sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e664b-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="e664b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e664b-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="e664b-114">Signification</span><span class="sxs-lookup"><span data-stu-id="e664b-114">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <span data-ttu-id="e664b-115"><dt>**System. Windows. Forms. FormBorderStyle. VbBSNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e664b-115"><dt>**System.Windows.Forms.FormBorderStyle.VbBSNone**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="e664b-116">Aucune bordure.</span><span class="sxs-lookup"><span data-stu-id="e664b-116">No border.</span></span> <span data-ttu-id="e664b-117">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e664b-117">This is the default value.</span></span><br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <span data-ttu-id="e664b-118"><dt>**System. Windows. Forms. FormBorderStyle. VbFixedSingle**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e664b-118"><dt>**System.Windows.Forms.FormBorderStyle.VbFixedSingle**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e664b-119">Fixe, bordure simple.</span><span class="sxs-lookup"><span data-stu-id="e664b-119">Fixed, single border.</span></span><br/>                 |



 

## <a name="exceptions"></a><span data-ttu-id="e664b-120">Exceptions</span><span class="sxs-lookup"><span data-stu-id="e664b-120">Exceptions</span></span>



| <span data-ttu-id="e664b-121">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="e664b-121">Exception type</span></span>               | <span data-ttu-id="e664b-122">Condition</span><span class="sxs-lookup"><span data-stu-id="e664b-122">Condition</span></span>                                |
|------------------------------|------------------------------------------|
| <span data-ttu-id="e664b-123">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="e664b-123">**System.ArgumentException**</span></span> | <span data-ttu-id="e664b-124">Le style de bordure spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e664b-124">The specified border style is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e664b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e664b-125">Requirements</span></span>



| <span data-ttu-id="e664b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e664b-126">Requirement</span></span> | <span data-ttu-id="e664b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e664b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e664b-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e664b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e664b-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e664b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e664b-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e664b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e664b-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e664b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e664b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e664b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e664b-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e664b-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e664b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e664b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e664b-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="e664b-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





