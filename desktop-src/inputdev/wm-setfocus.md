---
title: Message WM_SETFOCUS (winuser. h)
description: Envoyé à une fenêtre après qu’il a obtenu le focus clavier.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- WM_SETFOCUS l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b304d7f7739ce551c1efc6a1d33a934c48dc8b4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466670"
---
# <a name="wm_setfocus-message"></a><span data-ttu-id="75f1a-104">\_Message WM SetFocus</span><span class="sxs-lookup"><span data-stu-id="75f1a-104">WM\_SETFOCUS message</span></span>

<span data-ttu-id="75f1a-105">Envoyé à une fenêtre après qu’il a obtenu le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="75f1a-105">Sent to a window after it has gained the keyboard focus.</span></span>


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a><span data-ttu-id="75f1a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75f1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f1a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75f1a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75f1a-108">Handle de la fenêtre qui a perdu le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="75f1a-108">A handle to the window that has lost the keyboard focus.</span></span> <span data-ttu-id="75f1a-109">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="75f1a-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="75f1a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75f1a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75f1a-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="75f1a-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75f1a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75f1a-112">Return value</span></span>

<span data-ttu-id="75f1a-113">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="75f1a-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="75f1a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="75f1a-114">Remarks</span></span>

<span data-ttu-id="75f1a-115">Pour afficher un signe insertion, une application doit appeler les fonctions de signe insertion appropriées lorsqu’elle reçoit le message **WM \_ SetFocus** .</span><span class="sxs-lookup"><span data-stu-id="75f1a-115">To display a caret, an application should call the appropriate caret functions when it receives the **WM\_SETFOCUS** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="75f1a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75f1a-116">Requirements</span></span>



| <span data-ttu-id="75f1a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75f1a-117">Requirement</span></span> | <span data-ttu-id="75f1a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="75f1a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75f1a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75f1a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="75f1a-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75f1a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="75f1a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75f1a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="75f1a-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75f1a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="75f1a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="75f1a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="75f1a-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75f1a-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f1a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75f1a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="75f1a-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="75f1a-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="75f1a-127">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="75f1a-127">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="75f1a-128">**\_KILLFOCUS WM**</span><span class="sxs-lookup"><span data-stu-id="75f1a-128">**WM\_KILLFOCUS**</span></span>](wm-killfocus.md)
</dt> <dt>

<span data-ttu-id="75f1a-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="75f1a-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="75f1a-130">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="75f1a-130">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

