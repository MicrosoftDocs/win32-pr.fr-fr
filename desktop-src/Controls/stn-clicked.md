---
title: STN_CLICKED le code de notification (winuser. h)
description: Le \_ Code de notification cliqué sur le STN est envoyé lorsque l’utilisateur clique sur un contrôle statique avec le style de notification SS \_ . La fenêtre parente du contrôle reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- Contrôles Windows de code de notification STN_CLICKED
topic_type:
- apiref
api_name:
- STN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91f63bc496469f6edc26b4f9176f3f9157464bdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843137"
---
# <a name="stn_clicked-notification-code"></a><span data-ttu-id="d07f0-105">STN \_ a cliqué sur le code de notification</span><span class="sxs-lookup"><span data-stu-id="d07f0-105">STN\_CLICKED notification code</span></span>

<span data-ttu-id="d07f0-106">Le \_ Code de notification cliqué sur le STN est envoyé lorsque l’utilisateur clique sur un contrôle statique avec le style de notification [**SS \_**](static-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d07f0-106">The STN\_CLICKED notification code is sent when the user clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="d07f0-107">La fenêtre parente du contrôle reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d07f0-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d07f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d07f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d07f0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d07f0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d07f0-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="d07f0-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="d07f0-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="d07f0-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d07f0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d07f0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d07f0-113">Handle vers le contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="d07f0-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d07f0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d07f0-114">Requirements</span></span>



| <span data-ttu-id="d07f0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d07f0-115">Requirement</span></span> | <span data-ttu-id="d07f0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d07f0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07f0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d07f0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d07f0-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d07f0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d07f0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d07f0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d07f0-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d07f0-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d07f0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d07f0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d07f0-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d07f0-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d07f0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d07f0-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="d07f0-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d07f0-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d07f0-125">STN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="d07f0-125">STN\_DBLCLK</span></span>](stn-dblclk.md)
</dt> <dt>

<span data-ttu-id="d07f0-126">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d07f0-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d07f0-127">Contrôles statiques</span><span class="sxs-lookup"><span data-stu-id="d07f0-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="d07f0-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="d07f0-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d07f0-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d07f0-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d07f0-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d07f0-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d07f0-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="d07f0-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

