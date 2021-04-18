---
description: Envoyé une fois à une fenêtre après l’entrée dans la boucle modale de redimensionnement ou de déplacement.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Message WM_ENTERSIZEMOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536177"
---
# <a name="wm_entersizemove-message"></a><span data-ttu-id="c1307-103">\_Message WM ENTERSIZEMOVE</span><span class="sxs-lookup"><span data-stu-id="c1307-103">WM\_ENTERSIZEMOVE message</span></span>

<span data-ttu-id="c1307-104">Envoyé une fois à une fenêtre après l’entrée dans la boucle modale de redimensionnement ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="c1307-104">Sent one time to a window after it enters the moving or sizing modal loop.</span></span> <span data-ttu-id="c1307-105">La fenêtre passe à la boucle modale de déplacement ou de redimensionnement quand l’utilisateur clique sur la barre de titre ou la bordure de redimensionnement de la fenêtre, ou lorsque la fenêtre passe le message [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) et que le paramètre *wParam* du message spécifie la valeur **SC \_ Move** ou **SC \_ Size** .</span><span class="sxs-lookup"><span data-stu-id="c1307-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOVE** or **SC\_SIZE** value.</span></span> <span data-ttu-id="c1307-106">L’opération est terminée quand [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne.</span><span class="sxs-lookup"><span data-stu-id="c1307-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="c1307-107">Le système envoie le message **WM \_ ENTERSIZEMOVE** , que le glissement de fenêtres entières soit activé ou non.</span><span class="sxs-lookup"><span data-stu-id="c1307-107">The system sends the **WM\_ENTERSIZEMOVE** message regardless of whether the dragging of full windows is enabled.</span></span>

<span data-ttu-id="c1307-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c1307-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENTERSIZEMOVE                0x0231
```



## <a name="parameters"></a><span data-ttu-id="c1307-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1307-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1307-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1307-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1307-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c1307-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1307-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1307-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1307-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c1307-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1307-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1307-114">Return value</span></span>

<span data-ttu-id="c1307-115">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c1307-115">Type: **LRESULT**</span></span>

<span data-ttu-id="c1307-116">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="c1307-116">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1307-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1307-117">Requirements</span></span>



| <span data-ttu-id="c1307-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1307-118">Requirement</span></span> | <span data-ttu-id="c1307-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1307-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1307-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1307-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c1307-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1307-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c1307-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1307-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c1307-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1307-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1307-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1307-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1307-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1307-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1307-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1307-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1307-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c1307-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c1307-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c1307-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c1307-129">**\_EXITSIZEMOVE WM**</span><span class="sxs-lookup"><span data-stu-id="c1307-129">**WM\_EXITSIZEMOVE**</span></span>](wm-exitsizemove.md)
</dt> <dt>

[<span data-ttu-id="c1307-130">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="c1307-130">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)
</dt> <dt>

<span data-ttu-id="c1307-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c1307-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c1307-132">Windows</span><span class="sxs-lookup"><span data-stu-id="c1307-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
