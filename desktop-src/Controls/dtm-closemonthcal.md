---
title: Message DTM_CLOSEMONTHCAL (commctrl. h)
description: Ferme un contrôle de sélecteur de dates et d’heures (PAO). Envoyez ce message explicitement ou à l’aide de la \_ macro DateTime CloseMonthCal.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- DTM_CLOSEMONTHCAL les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032438"
---
# <a name="dtm_closemonthcal-message"></a><span data-ttu-id="229ec-105">\_Message DTM CLOSEMONTHCAL</span><span class="sxs-lookup"><span data-stu-id="229ec-105">DTM\_CLOSEMONTHCAL message</span></span>

<span data-ttu-id="229ec-106">Ferme un contrôle de sélecteur de dates et d’heures (PAO).</span><span class="sxs-lookup"><span data-stu-id="229ec-106">Closes a date and time picker (DTP) control.</span></span> <span data-ttu-id="229ec-107">Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .</span><span class="sxs-lookup"><span data-stu-id="229ec-107">Send this message explicitly or by using the [**DateTime\_CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="229ec-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="229ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="229ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="229ec-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="229ec-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="229ec-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="229ec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="229ec-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="229ec-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="229ec-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="229ec-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="229ec-113">Return value</span></span>

<span data-ttu-id="229ec-114">Retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="229ec-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="229ec-115">Notes</span><span class="sxs-lookup"><span data-stu-id="229ec-115">Remarks</span></span>

<span data-ttu-id="229ec-116">Détruit le contrôle et envoie une notification [DTN \_ gros plan](dtn-closeup.md) que le contrôle se ferme, par opposition au fait que le contrôle est en cours d’ouverture (en le déplaçant dans la notification de [ \_ liste déroulante DTN](dtn-dropdown.md) ) vers le parent du contrôle.</span><span class="sxs-lookup"><span data-stu-id="229ec-116">Destroys the control and sends a [DTN\_CLOSEUP](dtn-closeup.md) notification that the control is closing as opposed to the control is opening (dropping-down as in the [DTN\_DROPDOWN](dtn-dropdown.md) notification) to the control's parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="229ec-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="229ec-117">Requirements</span></span>



| <span data-ttu-id="229ec-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="229ec-118">Requirement</span></span> | <span data-ttu-id="229ec-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="229ec-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="229ec-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="229ec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="229ec-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="229ec-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="229ec-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="229ec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="229ec-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="229ec-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="229ec-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="229ec-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="229ec-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="229ec-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229ec-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="229ec-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="229ec-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="229ec-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="229ec-128">\_liste déroulante DTN</span><span class="sxs-lookup"><span data-stu-id="229ec-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="229ec-129">DTN \_ gros plan</span><span class="sxs-lookup"><span data-stu-id="229ec-129">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> </dl>

 

 





