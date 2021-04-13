---
title: PSN_WIZFINISH le code de notification (Prsht. h)
description: Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton Terminer dans un Assistant. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- Contrôles Windows de code de notification PSN_WIZFINISH
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466091"
---
# <a name="psn_wizfinish-notification-code"></a><span data-ttu-id="1d3d5-105">\_Code de notification PSN WIZFINISH</span><span class="sxs-lookup"><span data-stu-id="1d3d5-105">PSN\_WIZFINISH notification code</span></span>

<span data-ttu-id="1d3d5-106">Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton **Terminer** dans un Assistant.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-106">Notifies a page that the user has clicked the **Finish** button in a wizard.</span></span> <span data-ttu-id="1d3d5-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1d3d5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1d3d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d3d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d3d5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d3d5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d3d5-110">Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="1d3d5-111">Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="1d3d5-112">Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d3d5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d3d5-113">Return value</span></span>

-   <span data-ttu-id="1d3d5-114">Retourne la **valeur true** pour empêcher la fin de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-114">Returns **TRUE** to prevent the wizard from finishing.</span></span>
-   [<span data-ttu-id="1d3d5-115">Version 5,80.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-115">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="1d3d5-116">et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-116">and later.</span></span> <span data-ttu-id="1d3d5-117">Retourne un handle de fenêtre pour empêcher la fin de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-117">Returns a window handle to prevent the wizard from finishing.</span></span> <span data-ttu-id="1d3d5-118">L’Assistant va définir le focus sur cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-118">The wizard will set the focus to that window.</span></span> <span data-ttu-id="1d3d5-119">La fenêtre doit appartenir à la page de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-119">The window must be owned by the wizard page.</span></span>
-   <span data-ttu-id="1d3d5-120">Retourne **false** pour permettre à l’Assistant de se terminer.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-120">Returns **FALSE** to allow the wizard to finish.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d3d5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="1d3d5-121">Remarks</span></span>

<span data-ttu-id="1d3d5-122">Pour définir la valeur de retour, la procédure de la boîte de dialogue de la page doit utiliser la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur MSGRESULT de la boîte de \_ dialogue, et la procédure de boîte de dialogue doit retourner **true**.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

[<span data-ttu-id="1d3d5-123">Version 5,80.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-123">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="1d3d5-124">Si votre application retourne la **valeur true** pour empêcher la finition d’un Assistant, elle n’a aucun contrôle sur la fenêtre sur laquelle la page reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-124">If your application returns **TRUE** to prevent a wizard from finishing, it has no control over which window on the page receives focus.</span></span> <span data-ttu-id="1d3d5-125">Normalement, les applications qui doivent arrêter un Assistant peuvent le faire en retournant le handle de la fenêtre sur la page de l’Assistant qui doit recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="1d3d5-125">Applications that need to stop a wizard from finishing should normally do so by returning the handle of the window on the wizard page that is to receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d3d5-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d3d5-126">Requirements</span></span>



| <span data-ttu-id="1d3d5-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d3d5-127">Requirement</span></span> | <span data-ttu-id="1d3d5-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d3d5-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d3d5-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d3d5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1d3d5-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d3d5-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1d3d5-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d3d5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1d3d5-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d3d5-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1d3d5-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d3d5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d3d5-134"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d3d5-134"><dt>Prsht.h</dt></span></span> </dl> |



 

