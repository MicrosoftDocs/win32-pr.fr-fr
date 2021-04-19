---
title: Message MCM_SETFIRSTDAYOFWEEK (commctrl. h)
description: Définit le premier jour de la semaine pour un contrôle de calendrier mensuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetFirstDayOfWeek.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- MCM_SETFIRSTDAYOFWEEK les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509944"
---
# <a name="mcm_setfirstdayofweek-message"></a><span data-ttu-id="88b4f-105">\_Message SETFIRSTDAYOFWEEK MCM</span><span class="sxs-lookup"><span data-stu-id="88b4f-105">MCM\_SETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="88b4f-106">Définit le premier jour de la semaine pour un contrôle de calendrier mensuel.</span><span class="sxs-lookup"><span data-stu-id="88b4f-106">Sets the first day of the week for a month calendar control.</span></span> <span data-ttu-id="88b4f-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) .</span><span class="sxs-lookup"><span data-stu-id="88b4f-107">You can send this message explicitly or by using the [**MonthCal\_SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="88b4f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88b4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88b4f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88b4f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="88b4f-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="88b4f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="88b4f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88b4f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88b4f-112">Valeur de type **int** représentant le jour à définir comme premier jour de la semaine, où 0 est lundi, 1 est mardi, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="88b4f-112">Value of type **int** representing which day is to be set as the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88b4f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88b4f-113">Return value</span></span>

<span data-ttu-id="88b4f-114">Retourne une valeur **DWORD** qui contient deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="88b4f-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="88b4f-115">Le mot de poids fort est une valeur **bool** différente de zéro si le premier jour de la semaine précédent n’est pas égal aux paramètres régionaux \_ IFIRSTDAYOFWEEK, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="88b4f-115">The high word is a **BOOL** value that is nonzero if the previous first day of the week did not equal LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="88b4f-116">Le mot de poids faible est une valeur INT qui représente le premier jour de la semaine précédent.</span><span class="sxs-lookup"><span data-stu-id="88b4f-116">The low word is an INT value that represents the previous first day of the week.</span></span>

## <a name="remarks"></a><span data-ttu-id="88b4f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="88b4f-117">Remarks</span></span>

<span data-ttu-id="88b4f-118">Si le premier jour de la semaine est défini sur une valeur autre que la valeur par défaut (paramètres régionaux \_ IFIRSTDAYOFWEEK), le contrôle ne met pas automatiquement à jour les modifications de premier jour de la semaine en fonction des modifications de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="88b4f-118">If the first day of the week is set to anything other than the default (LOCALE\_IFIRSTDAYOFWEEK), the control will not automatically update first-day-of-the-week changes based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="88b4f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88b4f-119">Requirements</span></span>



| <span data-ttu-id="88b4f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88b4f-120">Requirement</span></span> | <span data-ttu-id="88b4f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="88b4f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88b4f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88b4f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="88b4f-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88b4f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88b4f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88b4f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="88b4f-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88b4f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88b4f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="88b4f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="88b4f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="88b4f-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





