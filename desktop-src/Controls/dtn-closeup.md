---
title: DTN_CLOSEUP le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur ferme le calendrier du mois déroulant.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- Contrôles Windows de code de notification DTN_CLOSEUP
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742829"
---
# <a name="dtn_closeup-notification-code"></a><span data-ttu-id="a89cc-104">\_Code de notification DTN gros plan</span><span class="sxs-lookup"><span data-stu-id="a89cc-104">DTN\_CLOSEUP notification code</span></span>

<span data-ttu-id="a89cc-105">Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur ferme le calendrier du mois déroulant.</span><span class="sxs-lookup"><span data-stu-id="a89cc-105">Sent by a date and time picker (DTP) control when the user closes the drop-down month calendar.</span></span> <span data-ttu-id="a89cc-106">Le calendrier du mois est fermé lorsque l’utilisateur choisit une date dans le calendrier du mois ou clique sur la flèche déroulante pendant que le calendrier est ouvert.</span><span class="sxs-lookup"><span data-stu-id="a89cc-106">The month calendar is closed when the user chooses a date from the month calendar or clicks the drop-down arrow while the calendar is open.</span></span> <span data-ttu-id="a89cc-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a89cc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="a89cc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a89cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a89cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a89cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a89cc-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur la notification.</span><span class="sxs-lookup"><span data-stu-id="a89cc-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a89cc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a89cc-111">Return value</span></span>

<span data-ttu-id="a89cc-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="a89cc-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="a89cc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a89cc-113">Remarks</span></span>

<span data-ttu-id="a89cc-114">Les contrôles de PAO ne maintiennent pas un contrôle Month Calendar enfant statique.</span><span class="sxs-lookup"><span data-stu-id="a89cc-114">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="a89cc-115">Le contrôle PAO détruit le contrôle Month Calendar enfant avant d’envoyer ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="a89cc-115">The DTP control destroys the child month calendar control prior to sending this notification code.</span></span> <span data-ttu-id="a89cc-116">Par conséquent, votre application ne doit pas s’appuyer sur un handle de fenêtre statique pour le calendrier de mois enfant du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a89cc-116">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="a89cc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a89cc-117">Requirements</span></span>



| <span data-ttu-id="a89cc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a89cc-118">Requirement</span></span> | <span data-ttu-id="a89cc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a89cc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a89cc-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a89cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a89cc-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a89cc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a89cc-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a89cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a89cc-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a89cc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a89cc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a89cc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a89cc-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a89cc-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a89cc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a89cc-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a89cc-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a89cc-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a89cc-128">\_liste déroulante DTN</span><span class="sxs-lookup"><span data-stu-id="a89cc-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="a89cc-129">**DTM \_ GETMONTHCAL**</span><span class="sxs-lookup"><span data-stu-id="a89cc-129">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

 





