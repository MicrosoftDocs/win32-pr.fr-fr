---
title: Message WM_GETDPISCALEDSIZE (winuser. h)
description: Ce message indique au système d’exploitation que la fenêtre sera dimensionnée sur une dimension autre que la valeur par défaut.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE message haute résolution
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465402"
---
# <a name="wm_getdpiscaledsize-message"></a><span data-ttu-id="ef918-104">\_Message WM GETDPISCALEDSIZE</span><span class="sxs-lookup"><span data-stu-id="ef918-104">WM\_GETDPISCALEDSIZE message</span></span>

<span data-ttu-id="ef918-105">Ce message indique au système d’exploitation que la fenêtre sera dimensionnée sur une dimension autre que la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ef918-105">This message tells the operating system that the window will be sized to dimensions other than the default.</span></span>

<span data-ttu-id="ef918-106">Ce message est envoyé aux fenêtres de niveau supérieur avec un [ \_ \_ contexte de détection PPP](dpi-awareness-context.md) de par moniteur v2 avant l’envoi d’un message [**\_ DPICHANGED WM**](wm-dpichanged.md) et permet à la fenêtre de calculer sa taille souhaitée pour la modification de la valeur PPP en attente.</span><span class="sxs-lookup"><span data-stu-id="ef918-106">This message is sent to top-level windows with a [DPI\_AWARENESS\_CONTEXT](dpi-awareness-context.md) of Per Monitor v2 before a [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent, and allows the window to compute its desired size for the pending DPI change.</span></span> <span data-ttu-id="ef918-107">Comme la mise à l’échelle PPP linéaire est le comportement par défaut, cela n’est utile que dans les scénarios où la fenêtre souhaite évoluer de manière non linéaire.</span><span class="sxs-lookup"><span data-stu-id="ef918-107">As linear DPI scaling is the default behavior, this is only useful in scenarios where the window wants to scale non-linearly.</span></span> <span data-ttu-id="ef918-108">Si l’application répond à ce message, la taille résultante sera le rectangle candidat envoyer à **WM \_ DPICHANGED**.</span><span class="sxs-lookup"><span data-stu-id="ef918-108">If the application responds to this message, the resulting size will be the candidate rectangle send to **WM\_DPICHANGED**.</span></span>

<span data-ttu-id="ef918-109">Utilisez ce message pour modifier la taille du Rect fourni avec [**WM \_ DPICHANGED**](wm-dpichanged.md).</span><span class="sxs-lookup"><span data-stu-id="ef918-109">Use this message to alter the size of the rect that is provided with [**WM\_DPICHANGED**](wm-dpichanged.md).</span></span>


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a><span data-ttu-id="ef918-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef918-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef918-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef918-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef918-112">WPARAM contient une valeur PPP.</span><span class="sxs-lookup"><span data-stu-id="ef918-112">The WPARAM contains a DPI value.</span></span> <span data-ttu-id="ef918-113">La taille de fenêtre mise à l’échelle que l’application doit définir doit être calculée comme si la fenêtre devait basculer vers cette PPP.</span><span class="sxs-lookup"><span data-stu-id="ef918-113">The scaled window size that the application would set needs to be computed as if the window were to switch to this DPI.</span></span>

</dd> <dt>

<span data-ttu-id="ef918-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef918-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef918-115">Le LPARAM est un pointeur in/out vers une structure de taille.</span><span class="sxs-lookup"><span data-stu-id="ef918-115">The LPARAM is an in/out pointer to a SIZE struct.</span></span> <span data-ttu-id="ef918-116">La \_ valeur de dans \_ le lParam correspond à la taille d’attente de la fenêtre après un déplacement initié par l’utilisateur ou un appel à [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="ef918-116">The \_In\_ value in the LPARAM is the pending size of the window after a user-initiated move or a call to [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="ef918-117">Si la fenêtre est redimensionnée, cette taille n’est pas nécessairement la même que la taille actuelle de la fenêtre au moment de la réception de ce message.</span><span class="sxs-lookup"><span data-stu-id="ef918-117">If the window is being resized, this size is not necessarily the same as the window's current size at the time this message is received.</span></span>

<span data-ttu-id="ef918-118">L' \_ \_ application doit écrire la valeur out dans lParam pour spécifier la taille de fenêtre mise à l’échelle souhaitée correspondant à la valeur DPI fournie dans wParam.</span><span class="sxs-lookup"><span data-stu-id="ef918-118">The \_Out\_ value in the LPARAM should be written to by the application to specify the desired scaled window size corresponding to the provided DPI value in the WPARAM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef918-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef918-119">Return value</span></span>

<span data-ttu-id="ef918-120">La fonction retourne une valeur BOOLÉENNE.</span><span class="sxs-lookup"><span data-stu-id="ef918-120">The function returns a BOOL.</span></span> <span data-ttu-id="ef918-121">Le retour de la valeur TRUE indique qu’une nouvelle taille a été calculée.</span><span class="sxs-lookup"><span data-stu-id="ef918-121">Returning TRUE indicates that a new size has been computed.</span></span> <span data-ttu-id="ef918-122">Si la valeur renvoyée est FALSe, cela signifie que le message ne sera pas géré et que la mise à l’échelle PPP linéaire par défaut s’appliquera à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ef918-122">Returning FALSE indicates that the message will not be handled, and the default linear DPI scaling will apply to the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef918-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ef918-123">Remarks</span></span>

<span data-ttu-id="ef918-124">Ce message est envoyé uniquement aux fenêtres de niveau supérieur qui ont un contexte de reconnaissance PPP de par moniteur v2.</span><span class="sxs-lookup"><span data-stu-id="ef918-124">This message is only sent to top-level windows which have a DPI awareness context of Per Monitor v2.</span></span>

<span data-ttu-id="ef918-125">Cet événement est nécessaire pour faciliter la mise à l’échelle non linéaire, et garantit que la position de Windows reste constante en relation avec le curseur et en cas de déplacement entre les moniteurs.</span><span class="sxs-lookup"><span data-stu-id="ef918-125">This event is necessary to facilitate graceful non-linear scaling, and ensures that the windows's position remains constant in relationship to the cursor and when moving back and forth across monitors.</span></span>

<span data-ttu-id="ef918-126">Il n’existe pas de gestion par défaut spécifique de ce message dans [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="ef918-126">There is no specific default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="ef918-127">Comme pour tous les messages qu’il ne gère pas explicitement, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) retourne zéro pour ce message.</span><span class="sxs-lookup"><span data-stu-id="ef918-127">As for all messages it does not explicitly handle, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will return zero for this message.</span></span> <span data-ttu-id="ef918-128">Comme indiqué ci-dessus, ce retour indique au système d’utiliser le comportement linéaire par défaut.</span><span class="sxs-lookup"><span data-stu-id="ef918-128">As noted above, this return tells the system to use the default linear behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef918-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef918-129">Requirements</span></span>



| <span data-ttu-id="ef918-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef918-130">Requirement</span></span> | <span data-ttu-id="ef918-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef918-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ef918-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef918-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ef918-133">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef918-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ef918-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef918-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ef918-135">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef918-135">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ef918-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef918-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef918-137"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef918-137"><dt>Winuser.h</dt></span></span> </dl> |



 

