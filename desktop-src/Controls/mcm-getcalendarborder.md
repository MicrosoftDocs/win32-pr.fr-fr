---
title: Message MCM_GETCALENDARBORDER (commctrl. h)
description: Obtient la taille de la bordure, en pixels. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCurrentView.
ms.assetid: 68366ee1-7511-46a5-aab0-a42fb80c265f
keywords:
- MCM_GETCALENDARBORDER les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581eeb5c060f725d3f884f4c19d7d3da3023c63a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508918"
---
# <a name="mcm_getcalendarborder-message"></a><span data-ttu-id="9160b-105">\_Message GETCALENDARBORDER MCM</span><span class="sxs-lookup"><span data-stu-id="9160b-105">MCM\_GETCALENDARBORDER message</span></span>

<span data-ttu-id="9160b-106">Obtient la taille de la bordure, en pixels.</span><span class="sxs-lookup"><span data-stu-id="9160b-106">Gets the size of the border, in pixels.</span></span> <span data-ttu-id="9160b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="9160b-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9160b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9160b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9160b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9160b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9160b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9160b-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9160b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9160b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9160b-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9160b-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9160b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9160b-113">Return value</span></span>

<span data-ttu-id="9160b-114">Taille de la bordure, en pixels.</span><span class="sxs-lookup"><span data-stu-id="9160b-114">Border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="9160b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9160b-115">Requirements</span></span>



| <span data-ttu-id="9160b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9160b-116">Requirement</span></span> | <span data-ttu-id="9160b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9160b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9160b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9160b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9160b-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9160b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9160b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9160b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9160b-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9160b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9160b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9160b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9160b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9160b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





