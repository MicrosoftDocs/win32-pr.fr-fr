---
title: Message DTM_GETMONTHCAL (commctrl. h)
description: Obtient le handle vers le contrôle de calendrier mensuel de l’enfant du sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetMonthCal.
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- DTM_GETMONTHCAL les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942491"
---
# <a name="dtm_getmonthcal-message"></a><span data-ttu-id="064ed-105">\_Message DTM GETMONTHCAL</span><span class="sxs-lookup"><span data-stu-id="064ed-105">DTM\_GETMONTHCAL message</span></span>

<span data-ttu-id="064ed-106">Obtient le handle vers le contrôle de calendrier mensuel de l’enfant du sélecteur de dates et d’heures (PAO).</span><span class="sxs-lookup"><span data-stu-id="064ed-106">Gets the handle to a date and time picker's (DTP) child month calendar control.</span></span> <span data-ttu-id="064ed-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) .</span><span class="sxs-lookup"><span data-stu-id="064ed-107">You can send this message explicitly or use the [**DateTime\_GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="064ed-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="064ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="064ed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="064ed-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="064ed-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="064ed-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="064ed-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="064ed-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="064ed-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="064ed-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="064ed-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="064ed-113">Return value</span></span>

<span data-ttu-id="064ed-114">Retourne le handle du contrôle calendrier mensuel enfant d’un contrôle PAO en cas de réussite, ou **null** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="064ed-114">Returns the handle to a DTP control's child month calendar control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="064ed-115">Notes</span><span class="sxs-lookup"><span data-stu-id="064ed-115">Remarks</span></span>

<span data-ttu-id="064ed-116">Les contrôles de PAO créent un contrôle calendrier mensuel enfant lorsque l’utilisateur clique sur la flèche déroulante (notification de[ \_ liste déroulante DTN](dtn-dropdown.md) ).</span><span class="sxs-lookup"><span data-stu-id="064ed-116">DTP controls create a child month calendar control when the user clicks the drop-down arrow ([DTN\_DROPDOWN](dtn-dropdown.md) notification).</span></span> <span data-ttu-id="064ed-117">Lorsque le calendrier mensuel n’est plus nécessaire, il est détruit (une notification [DTN \_ gros plan](dtn-closeup.md) est envoyée lors de la destruction).</span><span class="sxs-lookup"><span data-stu-id="064ed-117">When the month calendar is no longer needed, it is destroyed (a [DTN\_CLOSEUP](dtn-closeup.md) notification is sent on destruction).</span></span> <span data-ttu-id="064ed-118">Par conséquent, votre application ne doit pas s’appuyer sur un handle statique du calendrier du mois enfant du contrôle PAO.</span><span class="sxs-lookup"><span data-stu-id="064ed-118">So your application must not rely on a static handle to the DTP control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="064ed-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="064ed-119">Requirements</span></span>



| <span data-ttu-id="064ed-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="064ed-120">Requirement</span></span> | <span data-ttu-id="064ed-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="064ed-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="064ed-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="064ed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="064ed-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="064ed-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="064ed-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="064ed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="064ed-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="064ed-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="064ed-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="064ed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="064ed-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="064ed-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="064ed-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="064ed-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="064ed-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="064ed-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="064ed-130">DTN \_ gros plan</span><span class="sxs-lookup"><span data-stu-id="064ed-130">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="064ed-131">\_liste déroulante DTN</span><span class="sxs-lookup"><span data-stu-id="064ed-131">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> </dl>

 

 





