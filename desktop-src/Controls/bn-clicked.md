---
title: BN_CLICKED le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur clique sur un bouton. La fenêtre parente du bouton reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 74847549-b92f-4981-a979-d0b2a8a5539a
keywords:
- Contrôles Windows de code de notification BN_CLICKED
topic_type:
- apiref
api_name:
- BN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894837c9a930c6a5f6d124b6b9e983465ef3beac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103233"
---
# <a name="bn_clicked-notification-code"></a><span data-ttu-id="5e1db-105">\_Code de notification sur lequel vous avez cliqué</span><span class="sxs-lookup"><span data-stu-id="5e1db-105">BN\_CLICKED notification code</span></span>

<span data-ttu-id="5e1db-106">Envoyé lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="5e1db-106">Sent when the user clicks a button.</span></span>

<span data-ttu-id="5e1db-107">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="5e1db-107">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_CLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="5e1db-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e1db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e1db-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e1db-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e1db-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="5e1db-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="5e1db-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="5e1db-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5e1db-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e1db-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e1db-113">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="5e1db-113">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e1db-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5e1db-114">Remarks</span></span>

<span data-ttu-id="5e1db-115">Un bouton désactivé n’envoie pas de \_ Code de notification sur lequel un clic a été effectué dans sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="5e1db-115">A disabled button does not send a BN\_CLICKED notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e1db-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e1db-116">Requirements</span></span>



| <span data-ttu-id="5e1db-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e1db-117">Requirement</span></span> | <span data-ttu-id="5e1db-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e1db-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e1db-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e1db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5e1db-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e1db-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5e1db-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e1db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5e1db-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e1db-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e1db-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e1db-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e1db-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e1db-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e1db-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e1db-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e1db-126">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="5e1db-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="5e1db-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e1db-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5e1db-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e1db-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5e1db-129">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="5e1db-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

