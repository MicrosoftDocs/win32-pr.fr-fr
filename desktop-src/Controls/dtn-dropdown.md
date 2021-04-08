---
title: DTN_DROPDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur active le calendrier du mois de la liste déroulante. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- Contrôles Windows de code de notification DTN_DROPDOWN
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843937"
---
# <a name="dtn_dropdown-notification-code"></a><span data-ttu-id="8449b-105">\_Code de notification de liste déroulante DTN</span><span class="sxs-lookup"><span data-stu-id="8449b-105">DTN\_DROPDOWN notification code</span></span>

<span data-ttu-id="8449b-106">Envoyé par un contrôle de sélecteur de date et heure (PAO) lorsque l’utilisateur active le calendrier du mois de la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="8449b-106">Sent by a date and time picker (DTP) control when the user activates the drop-down month calendar.</span></span> <span data-ttu-id="8449b-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8449b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="8449b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8449b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8449b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8449b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8449b-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur la notification.</span><span class="sxs-lookup"><span data-stu-id="8449b-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8449b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8449b-111">Return value</span></span>

<span data-ttu-id="8449b-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8449b-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8449b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8449b-113">Remarks</span></span>

<span data-ttu-id="8449b-114">L’une des tâches que votre gestionnaire de notification peut avoir à effectuer consiste à personnaliser le contrôle de mois-calendrier déroulant.</span><span class="sxs-lookup"><span data-stu-id="8449b-114">One task that your notification handler may need to perform is to customize the dropdown month-calendar control.</span></span> <span data-ttu-id="8449b-115">Par exemple, si vous ne souhaitez pas « atteindre aujourd’hui », vous devez définir le style [**MCS \_ notoday**](month-calendar-control-styles.md)  du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8449b-115">For instance, if you do not want "Go To Today," you need to set the control's [**MCS\_NOTODAY**](month-calendar-control-styles.md)  style.</span></span> <span data-ttu-id="8449b-116">Pour récupérer un handle pour le contrôle Month-Calendar, envoyez au contrôle de PAO un message [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md) .</span><span class="sxs-lookup"><span data-stu-id="8449b-116">To retrieve a handle to the month-calendar control, send the DTP control a [**DTM\_GETMONTHCAL**](dtm-getmonthcal.md) message.</span></span> <span data-ttu-id="8449b-117">Vous pouvez ensuite utiliser ce handle et [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour définir le style Month-Calendar souhaité.</span><span class="sxs-lookup"><span data-stu-id="8449b-117">You can then use this handle and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) to set the desired month-calendar style.</span></span>

<span data-ttu-id="8449b-118">Les contrôles de PAO ne maintiennent pas un contrôle Month Calendar enfant statique.</span><span class="sxs-lookup"><span data-stu-id="8449b-118">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="8449b-119">Le contrôle PAO crée un nouveau contrôle Month Calendar avant d’envoyer ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="8449b-119">The DTP control creates a new month calendar control before sending this notification code.</span></span> <span data-ttu-id="8449b-120">En outre, le contrôle de PAO détruit le contrôle enfant lorsqu’il n’est pas actif (visible).</span><span class="sxs-lookup"><span data-stu-id="8449b-120">Additionally, the DTP control destroys the child control when it is not active (visible).</span></span> <span data-ttu-id="8449b-121">Par conséquent, votre application ne doit pas s’appuyer sur un handle de fenêtre statique pour le calendrier de mois enfant du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8449b-121">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="8449b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8449b-122">Requirements</span></span>



| <span data-ttu-id="8449b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8449b-123">Requirement</span></span> | <span data-ttu-id="8449b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="8449b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8449b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8449b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8449b-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8449b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8449b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8449b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8449b-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8449b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8449b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="8449b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8449b-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8449b-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8449b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8449b-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="8449b-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="8449b-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8449b-133">DTN \_ gros plan</span><span class="sxs-lookup"><span data-stu-id="8449b-133">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="8449b-134">**DTM \_ GETMONTHCAL**</span><span class="sxs-lookup"><span data-stu-id="8449b-134">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

