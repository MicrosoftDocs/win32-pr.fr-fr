---
title: EN_SEARCHWEB le code de notification (CommCtrl. h)
description: Envoyé lorsqu’un contrôle d’édition perd le focus clavier. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un \_ message WM Notify.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- Contrôles Windows de code de notification EN_SEARCHWEB
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464422"
---
# <a name="en_searchweb-notification-code"></a><span data-ttu-id="c9810-105">\_Code de notification en SEARCHWEB</span><span class="sxs-lookup"><span data-stu-id="c9810-105">EN\_SEARCHWEB notification code</span></span>

<span data-ttu-id="c9810-106">Envoyé après qu’un contrôle d’édition a effectué une recherche sur le Web lorsque la fonctionnalité « Rechercher sur le Web » est activée, consultez [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span><span class="sxs-lookup"><span data-stu-id="c9810-106">Sent after an edit control performed a web search when the "Search the web" feature is enabled, see [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span></span> <span data-ttu-id="c9810-107">La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c9810-107">The parent window of the edit control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="c9810-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9810-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9810-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9810-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9810-110">Handle du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="c9810-110">Handle to the edit control.</span></span>

</dd> <dt>

<span data-ttu-id="c9810-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9810-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9810-112">Pointeur vers une structure [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) .</span><span class="sxs-lookup"><span data-stu-id="c9810-112">A pointer to a [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9810-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9810-113">Requirements</span></span>



| <span data-ttu-id="c9810-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9810-114">Requirement</span></span> | <span data-ttu-id="c9810-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9810-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9810-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9810-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c9810-117">Applications de bureau Windows 10, 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9810-117">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c9810-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9810-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c9810-119">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9810-119">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c9810-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9810-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9810-121"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9810-121"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9810-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9810-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9810-123">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c9810-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c9810-124">**\_ENABLESEARCHWEB em**</span><span class="sxs-lookup"><span data-stu-id="c9810-124">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> <dt>

<span data-ttu-id="c9810-125">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="c9810-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c9810-126">**\_notification WM**</span><span class="sxs-lookup"><span data-stu-id="c9810-126">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





