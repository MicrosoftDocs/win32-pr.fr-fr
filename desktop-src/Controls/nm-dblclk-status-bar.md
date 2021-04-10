---
title: NM_DBLCLK (barre d’État) Code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle de barre d’État que l’utilisateur a double-cliqué dans le contrôle avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 4c02c76d-2bdb-48ef-aa8e-635d0e200eb1
keywords:
- NM_DBLCLK (barre d’État) contrôles Windows de code de notification
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28866effbc4143dc9d0d5a3800f88711c99f88db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941667"
---
# <a name="nm_dblclk-status-bar-notification-code"></a><span data-ttu-id="a6bcb-105">\_DBLCLK nm (barre d’État) Code de notification</span><span class="sxs-lookup"><span data-stu-id="a6bcb-105">NM\_DBLCLK (status bar) notification code</span></span>

<span data-ttu-id="a6bcb-106">Notifie la fenêtre parente d’un contrôle de barre d’État que l’utilisateur a double-cliqué dans le contrôle avec le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-106">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="a6bcb-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a6bcb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    LPNMMOUSE lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a6bcb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6bcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6bcb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6bcb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6bcb-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="a6bcb-111">Le membre **dwItemSpec** contient l’index de la section sur laquelle l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6bcb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6bcb-112">Return value</span></span>

<span data-ttu-id="a6bcb-113">Retourne la **valeur true** pour indiquer que le clic de souris a été géré et supprimer le traitement par défaut par le système.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="a6bcb-114">Retourne **false** pour autoriser le traitement par défaut du clic.</span><span class="sxs-lookup"><span data-stu-id="a6bcb-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6bcb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6bcb-115">Requirements</span></span>



| <span data-ttu-id="a6bcb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6bcb-116">Requirement</span></span> | <span data-ttu-id="a6bcb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6bcb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bcb-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6bcb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6bcb-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6bcb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6bcb-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6bcb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6bcb-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6bcb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6bcb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6bcb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6bcb-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6bcb-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





