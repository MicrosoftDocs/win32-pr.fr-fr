---
title: Message MCM_SETCALID (commctrl. h)
description: Définit l’ID de calendrier pour le contrôle de calendrier donné. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetCALID.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- MCM_SETCALID les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032493"
---
# <a name="mcm_setcalid-message"></a><span data-ttu-id="7019e-105">\_Message SETCALID MCM</span><span class="sxs-lookup"><span data-stu-id="7019e-105">MCM\_SETCALID message</span></span>

<span data-ttu-id="7019e-106">Définit l’ID de calendrier pour le contrôle de calendrier donné.</span><span class="sxs-lookup"><span data-stu-id="7019e-106">Sets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="7019e-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) .</span><span class="sxs-lookup"><span data-stu-id="7019e-107">You can send this message explicitly or by using the [**MonthCal\_SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7019e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7019e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7019e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7019e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7019e-110">ID de calendrier.</span><span class="sxs-lookup"><span data-stu-id="7019e-110">The calendar ID.</span></span> <span data-ttu-id="7019e-111">Une des constantes d' [identificateurs de calendrier](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="7019e-111">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

</dd> <dt>

<span data-ttu-id="7019e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7019e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7019e-113">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7019e-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7019e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7019e-114">Return value</span></span>

<span data-ttu-id="7019e-115">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7019e-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="7019e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7019e-116">Requirements</span></span>



| <span data-ttu-id="7019e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7019e-117">Requirement</span></span> | <span data-ttu-id="7019e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7019e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7019e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7019e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7019e-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7019e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7019e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7019e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7019e-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7019e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7019e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7019e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7019e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7019e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

