---
title: Message MCM_GETCALID (commctrl. h)
description: Obtient l’ID de calendrier pour le contrôle de calendrier donné. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCALID.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- MCM_GETCALID les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104038"
---
# <a name="mcm_getcalid-message"></a><span data-ttu-id="81b8b-105">\_Message GETCALID MCM</span><span class="sxs-lookup"><span data-stu-id="81b8b-105">MCM\_GETCALID message</span></span>

<span data-ttu-id="81b8b-106">Obtient l’ID de calendrier pour le contrôle de calendrier donné.</span><span class="sxs-lookup"><span data-stu-id="81b8b-106">Gets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="81b8b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) .</span><span class="sxs-lookup"><span data-stu-id="81b8b-107">You can send this message explicitly or by using the [**MonthCal\_GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="81b8b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81b8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81b8b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81b8b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81b8b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="81b8b-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="81b8b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81b8b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81b8b-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="81b8b-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81b8b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81b8b-113">Return value</span></span>

<span data-ttu-id="81b8b-114">ID du calendrier actuel.</span><span class="sxs-lookup"><span data-stu-id="81b8b-114">ID of the current calendar.</span></span> <span data-ttu-id="81b8b-115">Une des constantes d' [identificateurs de calendrier](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="81b8b-115">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="81b8b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81b8b-116">Requirements</span></span>



| <span data-ttu-id="81b8b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81b8b-117">Requirement</span></span> | <span data-ttu-id="81b8b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="81b8b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81b8b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81b8b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="81b8b-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81b8b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81b8b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81b8b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="81b8b-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81b8b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81b8b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="81b8b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="81b8b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81b8b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

