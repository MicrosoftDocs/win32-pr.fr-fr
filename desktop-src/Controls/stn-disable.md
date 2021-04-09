---
title: STN_DISABLE le code de notification (winuser. h)
description: Le \_ Code de notification de désactivation de STN est envoyé lorsqu’un contrôle statique est désactivé.
ms.assetid: 7ff0c191-4ff3-4a11-a418-8f45e16d0318
keywords:
- Contrôles Windows de code de notification STN_DISABLE
topic_type:
- apiref
api_name:
- STN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2763fce96b043ec6aebf5339a9f93d6fdf4a8abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103057"
---
# <a name="stn_disable-notification-code"></a><span data-ttu-id="fecd8-104">STN \_ désactiver le code de notification</span><span class="sxs-lookup"><span data-stu-id="fecd8-104">STN\_DISABLE notification code</span></span>

<span data-ttu-id="fecd8-105">Le \_ Code de notification de désactivation de STN est envoyé lorsqu’un contrôle statique est désactivé.</span><span class="sxs-lookup"><span data-stu-id="fecd8-105">The STN\_DISABLE notification code is sent when a static control is disabled.</span></span> <span data-ttu-id="fecd8-106">Le contrôle statique doit avoir le style [**SS \_ Notify**](static-control-styles.md) pour recevoir ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="fecd8-106">The static control must have the [**SS\_NOTIFY**](static-control-styles.md) style to receive this notification code.</span></span> <span data-ttu-id="fecd8-107">La fenêtre parente du contrôle reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="fecd8-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DISABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fecd8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fecd8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fecd8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fecd8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fecd8-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="fecd8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="fecd8-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="fecd8-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="fecd8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fecd8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fecd8-113">Handle vers le contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="fecd8-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fecd8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fecd8-114">Requirements</span></span>



| <span data-ttu-id="fecd8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fecd8-115">Requirement</span></span> | <span data-ttu-id="fecd8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fecd8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fecd8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fecd8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fecd8-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fecd8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fecd8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fecd8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fecd8-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fecd8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fecd8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="fecd8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fecd8-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fecd8-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fecd8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fecd8-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="fecd8-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="fecd8-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fecd8-125">STN \_ activer</span><span class="sxs-lookup"><span data-stu-id="fecd8-125">STN\_ENABLE</span></span>](stn-enable.md)
</dt> <dt>

<span data-ttu-id="fecd8-126">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="fecd8-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fecd8-127">Contrôles statiques</span><span class="sxs-lookup"><span data-stu-id="fecd8-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="fecd8-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="fecd8-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="fecd8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fecd8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fecd8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fecd8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fecd8-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="fecd8-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

