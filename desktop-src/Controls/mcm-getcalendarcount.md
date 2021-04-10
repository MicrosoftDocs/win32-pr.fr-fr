---
title: Message MCM_GETCALENDARCOUNT (commctrl. h)
description: Obtient le nombre de calendriers actuellement affichés dans le contrôle calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCalendarCount.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- MCM_GETCALENDARCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104806"
---
# <a name="mcm_getcalendarcount-message"></a><span data-ttu-id="e3878-105">\_Message GETCALENDARCOUNT MCM</span><span class="sxs-lookup"><span data-stu-id="e3878-105">MCM\_GETCALENDARCOUNT message</span></span>

<span data-ttu-id="e3878-106">Obtient le nombre de calendriers actuellement affichés dans le contrôle calendrier.</span><span class="sxs-lookup"><span data-stu-id="e3878-106">Gets the number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="e3878-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) .</span><span class="sxs-lookup"><span data-stu-id="e3878-107">You can send this message explicitly or by using the [**MonthCal\_GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3878-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3878-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3878-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3878-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3878-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e3878-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e3878-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3878-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3878-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e3878-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3878-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3878-113">Return value</span></span>

<span data-ttu-id="e3878-114">Nombre de calendriers actuellement affichés dans le contrôle calendrier.</span><span class="sxs-lookup"><span data-stu-id="e3878-114">Number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="e3878-115">Le nombre maximal de calendriers autorisés est 12.</span><span class="sxs-lookup"><span data-stu-id="e3878-115">The maximum number of allowed calendars is 12.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3878-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3878-116">Requirements</span></span>



| <span data-ttu-id="e3878-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3878-117">Requirement</span></span> | <span data-ttu-id="e3878-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3878-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3878-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3878-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e3878-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3878-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3878-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3878-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e3878-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3878-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3878-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3878-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3878-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3878-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





