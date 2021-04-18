---
title: BN_SETFOCUS le code de notification (winuser. h)
description: Envoyé lorsqu’un bouton reçoit le focus clavier. Le bouton doit avoir le \_ style BS Notify pour envoyer ce code de notification. La fenêtre parente du bouton reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- Contrôles Windows de code de notification BN_SETFOCUS
topic_type:
- apiref
api_name:
- BN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb9204f5b23b62b6cee9fb2652a16d546f6ef62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512553"
---
# <a name="bn_setfocus-notification-code"></a><span data-ttu-id="62694-106">Code de notification de l’e/ \_ SetFocus</span><span class="sxs-lookup"><span data-stu-id="62694-106">BN\_SETFOCUS notification code</span></span>

<span data-ttu-id="62694-107">Envoyé lorsqu’un bouton reçoit le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="62694-107">Sent when a button receives the keyboard focus.</span></span> <span data-ttu-id="62694-108">Le bouton doit avoir le style [**BS \_ Notify**](button-styles.md) pour envoyer ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="62694-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="62694-109">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="62694-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="62694-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62694-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62694-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62694-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62694-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="62694-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="62694-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="62694-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="62694-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62694-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62694-115">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="62694-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62694-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62694-116">Requirements</span></span>



| <span data-ttu-id="62694-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62694-117">Requirement</span></span> | <span data-ttu-id="62694-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="62694-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62694-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62694-119">Minimum supported client</span></span><br/> | <span data-ttu-id="62694-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62694-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="62694-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62694-121">Minimum supported server</span></span><br/> | <span data-ttu-id="62694-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62694-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62694-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="62694-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="62694-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62694-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62694-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62694-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62694-126">\_KILLFOCUS.</span><span class="sxs-lookup"><span data-stu-id="62694-126">BN\_KILLFOCUS</span></span>](bn-killfocus.md)
</dt> </dl>

 

