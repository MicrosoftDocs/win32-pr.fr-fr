---
title: Message MCM_GETFIRSTDAYOFWEEK (commctrl. h)
description: Récupère le premier jour de la semaine pour un contrôle de calendrier mensuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetFirstDayOfWeek.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- MCM_GETFIRSTDAYOFWEEK les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511781"
---
# <a name="mcm_getfirstdayofweek-message"></a><span data-ttu-id="520ab-105">\_Message GETFIRSTDAYOFWEEK MCM</span><span class="sxs-lookup"><span data-stu-id="520ab-105">MCM\_GETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="520ab-106">Récupère le premier jour de la semaine pour un contrôle de calendrier mensuel.</span><span class="sxs-lookup"><span data-stu-id="520ab-106">Retrieves the first day of the week for a month calendar control.</span></span> <span data-ttu-id="520ab-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) .</span><span class="sxs-lookup"><span data-stu-id="520ab-107">You can send this message explicitly or by using the [**MonthCal\_GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="520ab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="520ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="520ab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="520ab-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="520ab-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="520ab-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="520ab-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="520ab-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="520ab-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="520ab-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="520ab-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="520ab-113">Return value</span></span>

<span data-ttu-id="520ab-114">Retourne une valeur **DWORD** qui contient deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="520ab-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="520ab-115">Le mot de poids fort est une valeur **bool** différente de zéro si le premier jour de la semaine est défini sur une valeur autre que locale \_ IFIRSTDAYOFWEEK, ou sur zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="520ab-115">The high word is a **BOOL** value that is nonzero if the first day of the week is set to something other than LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="520ab-116">Le mot de poids faible est une valeur INT qui représente le premier jour de la semaine, où 0 est lundi, 1 est mardi, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="520ab-116">The low word is an INT value that represents the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="520ab-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="520ab-117">Requirements</span></span>



| <span data-ttu-id="520ab-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="520ab-118">Requirement</span></span> | <span data-ttu-id="520ab-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="520ab-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="520ab-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="520ab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="520ab-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="520ab-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="520ab-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="520ab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="520ab-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="520ab-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="520ab-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="520ab-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="520ab-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="520ab-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





