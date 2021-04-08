---
title: Message WM_DPICHANGED_BEFOREPARENT (winuser. h)
description: Pour les fenêtres de niveau supérieur par moniteur v2, ce message est envoyé à tous les HWND dans l’arborescence HWDN enfant de la fenêtre qui subit une modification PPP. | Message WM_DPICHANGED_BEFOREPARENT (winuser. h)
ms.assetid: EC8CC313-565F-451F-AE18-66F3B63303CE
keywords:
- WM_DPICHANGED_BEFOREPARENT message haute résolution
topic_type:
- apiref
api_name:
- WM_DPICHANGED_BEFOREPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16641916cb16b789f2349a53b09dbd2af5f520f3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953752"
---
# <a name="wm_dpichanged_beforeparent-message"></a><span data-ttu-id="6f612-105">\_ \_ Message BEFOREPARENT WM DPICHANGED</span><span class="sxs-lookup"><span data-stu-id="6f612-105">WM\_DPICHANGED\_BEFOREPARENT message</span></span>

<span data-ttu-id="6f612-106">Pour les fenêtres de niveau supérieur [par moniteur v2](dpi-awareness-context.md) , ce message est envoyé à tous les HWND dans l’arborescence HWDN enfant de la fenêtre qui subit une modification PPP.</span><span class="sxs-lookup"><span data-stu-id="6f612-106">For [Per Monitor v2](dpi-awareness-context.md) top-level windows, this message is sent to all HWNDs in the child HWDN tree of the window that is undergoing a DPI change.</span></span> <span data-ttu-id="6f612-107">Ce message s’affiche avant que la fenêtre de niveau supérieur ne reçoive le [**WM \_ DPICHANGED**](wm-dpichanged.md)et parcourt l’arborescence enfant du bas vers le haut.</span><span class="sxs-lookup"><span data-stu-id="6f612-107">This message occurs before the top-level window receives [**WM\_DPICHANGED**](wm-dpichanged.md), and traverses the child tree from the bottom up.</span></span>


```C++
#define WM_DPICHANGED_BEFOREPARENT       0x02E2
```



## <a name="parameters"></a><span data-ttu-id="6f612-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f612-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f612-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f612-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f612-110">Cette valeur n’est pas utilisée et sera égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="6f612-110">This value is unused and will be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6f612-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f612-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f612-112">Cette valeur n’est pas utilisée et sera égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="6f612-112">This value is unused and will be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f612-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f612-113">Return value</span></span>

<span data-ttu-id="6f612-114">Cette valeur n’est pas utilisée et est ignorée par le système.</span><span class="sxs-lookup"><span data-stu-id="6f612-114">This value is unused and ignored by the system.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f612-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6f612-115">Remarks</span></span>

<span data-ttu-id="6f612-116">Il n’y a pas de gestion par défaut de ce message dans [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="6f612-116">There is no default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="6f612-117">Ce message est envoyé uniquement lorsque la fenêtre de niveau supérieur a un contexte de sensibilisation en DPI de PMv2.</span><span class="sxs-lookup"><span data-stu-id="6f612-117">This message is only sent when the top-level window has a DPI awareness context of PMv2.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f612-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f612-118">Requirements</span></span>



| <span data-ttu-id="6f612-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f612-119">Requirement</span></span> | <span data-ttu-id="6f612-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f612-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6f612-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f612-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6f612-122">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f612-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6f612-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f612-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6f612-124">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f612-124">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6f612-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f612-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f612-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f612-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f612-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f612-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f612-128">**\_DPICHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="6f612-128">**WM\_DPICHANGED**</span></span>](wm-dpichanged.md)
</dt> <dt>

[<span data-ttu-id="6f612-129">**\_DPICHANGED WM \_ AFTERPARENT**</span><span class="sxs-lookup"><span data-stu-id="6f612-129">**WM\_DPICHANGED\_AFTERPARENT**</span></span>](wm-dpichanged-afterparent.md)
</dt> </dl>

 

