---
title: BN_KILLFOCUS le code de notification (winuser. h)
description: Envoyé lorsqu’un bouton perd le focus clavier. Le bouton doit avoir le \_ style BS Notify pour envoyer ce code de notification. La fenêtre parente du bouton reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- Contrôles Windows de code de notification BN_KILLFOCUS
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3fb6737d88ccddedbba6db58ffd0f713da7a8a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464666"
---
# <a name="bn_killfocus-notification-code"></a><span data-ttu-id="25c33-106">\_Code de notification KILLFOCUSy</span><span class="sxs-lookup"><span data-stu-id="25c33-106">BN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="25c33-107">Envoyé lorsqu’un bouton perd le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="25c33-107">Sent when a button loses the keyboard focus.</span></span> <span data-ttu-id="25c33-108">Le bouton doit avoir le style [**BS \_ Notify**](button-styles.md) pour envoyer ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="25c33-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="25c33-109">La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="25c33-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="25c33-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25c33-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25c33-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25c33-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25c33-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton.</span><span class="sxs-lookup"><span data-stu-id="25c33-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="25c33-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="25c33-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="25c33-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25c33-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25c33-115">Handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="25c33-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25c33-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25c33-116">Requirements</span></span>



| <span data-ttu-id="25c33-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25c33-117">Requirement</span></span> | <span data-ttu-id="25c33-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="25c33-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25c33-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25c33-119">Minimum supported client</span></span><br/> | <span data-ttu-id="25c33-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25c33-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="25c33-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25c33-121">Minimum supported server</span></span><br/> | <span data-ttu-id="25c33-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25c33-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="25c33-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="25c33-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="25c33-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25c33-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25c33-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25c33-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c33-126">-e \_ SetFocus</span><span class="sxs-lookup"><span data-stu-id="25c33-126">BN\_SETFOCUS</span></span>](bn-setfocus.md)
</dt> </dl>

 

