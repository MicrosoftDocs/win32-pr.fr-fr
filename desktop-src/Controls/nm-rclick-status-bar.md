---
title: NM_RCLICK (barre d’État) Code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle de barre d’État sur lequel l’utilisateur a cliqué avec le bouton droit de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- NM_RCLICK (barre d’État) contrôles Windows de code de notification
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326ac6600716419648ecfacf25cd8423551fd03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317525"
---
# <a name="nm_rclick-status-bar-notification-code"></a><span data-ttu-id="1f080-105">\_RCLICK nm (barre d’État) Code de notification</span><span class="sxs-lookup"><span data-stu-id="1f080-105">NM\_RCLICK (status bar) notification code</span></span>

<span data-ttu-id="1f080-106">Notifie la fenêtre parente d’un contrôle de barre d’État sur lequel l’utilisateur a cliqué avec le bouton droit de la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="1f080-106">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="1f080-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1f080-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1f080-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f080-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f080-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f080-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f080-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="1f080-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f080-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f080-111">Return value</span></span>

<span data-ttu-id="1f080-112">Retourne la **valeur true** pour indiquer que le clic de souris a été géré et supprimer le traitement par défaut par le système.</span><span class="sxs-lookup"><span data-stu-id="1f080-112">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="1f080-113">Retourne **false** pour autoriser le traitement par défaut du clic.</span><span class="sxs-lookup"><span data-stu-id="1f080-113">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f080-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f080-114">Requirements</span></span>



| <span data-ttu-id="1f080-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f080-115">Requirement</span></span> | <span data-ttu-id="1f080-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f080-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f080-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f080-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1f080-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f080-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f080-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f080-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1f080-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f080-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f080-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f080-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f080-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f080-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





