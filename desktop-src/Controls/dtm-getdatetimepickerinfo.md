---
title: Message DTM_GETDATETIMEPICKERINFO (commctrl. h)
description: Obtient des informations sur un contrôle de sélecteur de dates et d’heures (PAO).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- DTM_GETDATETIMEPICKERINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464434"
---
# <a name="dtm_getdatetimepickerinfo-message"></a><span data-ttu-id="4b48f-104">\_Message DTM GETDATETIMEPICKERINFO</span><span class="sxs-lookup"><span data-stu-id="4b48f-104">DTM\_GETDATETIMEPICKERINFO message</span></span>

<span data-ttu-id="4b48f-105">Obtient des informations sur un contrôle de sélecteur de dates et d’heures (PAO).</span><span class="sxs-lookup"><span data-stu-id="4b48f-105">Gets information on a date and time picker (DTP) control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b48f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b48f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b48f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b48f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b48f-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4b48f-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b48f-109">*lParam* \[in\]</span></span>
</dt> <dd> <span data-ttu-id="4b48f-110">Pointeur vers <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> pour recevoir les informations.</span><span class="sxs-lookup"><span data-stu-id="4b48f-110">A pointer to <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> to receive the information.</span></span> <span data-ttu-id="4b48f-111">L’appelant est chargé d’allouer la mémoire pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="4b48f-111">The caller is responsible for allocating the memory for this structure.</span></span> <span data-ttu-id="4b48f-112">Définissez le membre **cbSize** de la structure sur sizeof (DATETIMEPICKERINFO) avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="4b48f-112">Set the **cbSize** member of the structure to sizeof(DATETIMEPICKERINFO) before sending this message.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b48f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b48f-113">Return value</span></span>

<span data-ttu-id="4b48f-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="4b48f-114">Return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b48f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b48f-115">Requirements</span></span>



| <span data-ttu-id="4b48f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b48f-116">Requirement</span></span> | <span data-ttu-id="4b48f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b48f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b48f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b48f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4b48f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b48f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b48f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b48f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4b48f-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b48f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b48f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b48f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b48f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b48f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





