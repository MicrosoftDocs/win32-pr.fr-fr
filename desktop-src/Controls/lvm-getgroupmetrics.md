---
title: Message LVM_GETGROUPMETRICS (commctrl. h)
description: Obtient des informations sur l’affichage des groupes.
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- LVM_GETGROUPMETRICS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5af8ec50fe74ab90a0f3e44a69e2cbc7dda583e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942654"
---
# <a name="lvm_getgroupmetrics-message"></a><span data-ttu-id="e8060-104">\_Message GETGROUPMETRICS LVM</span><span class="sxs-lookup"><span data-stu-id="e8060-104">LVM\_GETGROUPMETRICS message</span></span>

<span data-ttu-id="e8060-105">Obtient des informations sur l’affichage des groupes.</span><span class="sxs-lookup"><span data-stu-id="e8060-105">Gets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8060-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8060-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8060-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8060-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e8060-108">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e8060-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="e8060-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8060-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e8060-110">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> qui reçoit les métriques récupérées.</span><span class="sxs-lookup"><span data-stu-id="e8060-110">A pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that receives the retrieved metrics.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8060-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8060-111">Return value</span></span>

<span data-ttu-id="e8060-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="e8060-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8060-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e8060-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8060-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="e8060-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e8060-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e8060-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8060-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8060-116">Requirements</span></span>



| <span data-ttu-id="e8060-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8060-117">Requirement</span></span> | <span data-ttu-id="e8060-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8060-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8060-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8060-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8060-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8060-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8060-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8060-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8060-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8060-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8060-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8060-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8060-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8060-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





