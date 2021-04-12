---
title: Message LVM_SETGROUPMETRICS (commctrl. h)
description: Définit des informations sur l’affichage des groupes.
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- LVM_SETGROUPMETRICS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215962e6f84aac83a2151b46f489938b575303c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317117"
---
# <a name="lvm_setgroupmetrics-message"></a><span data-ttu-id="b16c7-104">\_Message SETGROUPMETRICS LVM</span><span class="sxs-lookup"><span data-stu-id="b16c7-104">LVM\_SETGROUPMETRICS message</span></span>

<span data-ttu-id="b16c7-105">Définit des informations sur l’affichage des groupes.</span><span class="sxs-lookup"><span data-stu-id="b16c7-105">Sets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="b16c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b16c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b16c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b16c7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b16c7-108">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b16c7-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="b16c7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b16c7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b16c7-110">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> qui contient les métriques à définir.</span><span class="sxs-lookup"><span data-stu-id="b16c7-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that contains the metrics to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b16c7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b16c7-111">Return value</span></span>

<span data-ttu-id="b16c7-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="b16c7-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b16c7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b16c7-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b16c7-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="b16c7-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b16c7-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b16c7-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b16c7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b16c7-116">Requirements</span></span>



| <span data-ttu-id="b16c7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b16c7-117">Requirement</span></span> | <span data-ttu-id="b16c7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b16c7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b16c7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b16c7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b16c7-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b16c7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b16c7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b16c7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b16c7-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b16c7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b16c7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b16c7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b16c7-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b16c7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





