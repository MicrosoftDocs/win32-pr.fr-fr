---
title: ACN_STOP le code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle d’animation que le clip AVI associé a cessé de fonctionner. Ce code de notification est envoyé sous la forme d’un \_ message de commande WM.
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- Contrôles Windows de code de notification ACN_STOP
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cbdb27677439b7f08b489cba9024d44f3ebee6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032567"
---
# <a name="acn_stop-notification-code"></a><span data-ttu-id="e08c3-105">ACN \_ arrêter le code de notification</span><span class="sxs-lookup"><span data-stu-id="e08c3-105">ACN\_STOP notification code</span></span>

<span data-ttu-id="e08c3-106">Notifie la fenêtre parente d’un contrôle d’animation que le clip AVI associé a cessé de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="e08c3-106">Notifies the parent window of an animation control that the associated AVI clip has stopped playing.</span></span> <span data-ttu-id="e08c3-107">Ce code de notification est envoyé sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e08c3-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e08c3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e08c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e08c3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e08c3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e08c3-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="e08c3-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="e08c3-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="e08c3-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e08c3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e08c3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e08c3-113">**HWND** qui spécifie le handle du contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="e08c3-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e08c3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e08c3-114">Requirements</span></span>



| <span data-ttu-id="e08c3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e08c3-115">Requirement</span></span> | <span data-ttu-id="e08c3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e08c3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e08c3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e08c3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e08c3-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e08c3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e08c3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e08c3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e08c3-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e08c3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e08c3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e08c3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e08c3-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e08c3-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

