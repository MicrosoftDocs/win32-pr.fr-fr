---
description: Envoyé une fois à une fenêtre, après la sortie de la boucle modale de redimensionnement ou de déplacement.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: Message WM_EXITSIZEMOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541867"
---
# <a name="wm_exitsizemove-message"></a><span data-ttu-id="43384-103">\_Message WM EXITSIZEMOVE</span><span class="sxs-lookup"><span data-stu-id="43384-103">WM\_EXITSIZEMOVE message</span></span>

<span data-ttu-id="43384-104">Envoyé une fois à une fenêtre, après la sortie de la boucle modale de redimensionnement ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="43384-104">Sent one time to a window, after it has exited the moving or sizing modal loop.</span></span> <span data-ttu-id="43384-105">La fenêtre entre dans la boucle modale de déplacement ou de redimensionnement lorsque l’utilisateur clique sur la barre de titre ou la bordure de redimensionnement de la fenêtre, ou lorsque la fenêtre passe le message [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) et que le paramètre *wParam* du message spécifie la valeur de la **\_ taille** de **SC \_ MOV** E ou SC.</span><span class="sxs-lookup"><span data-stu-id="43384-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOV** E or **SC\_SIZE** value.</span></span> <span data-ttu-id="43384-106">L’opération est terminée quand [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne.</span><span class="sxs-lookup"><span data-stu-id="43384-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="43384-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="43384-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a><span data-ttu-id="43384-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43384-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43384-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43384-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43384-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="43384-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="43384-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43384-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43384-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="43384-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43384-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43384-113">Return value</span></span>

<span data-ttu-id="43384-114">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="43384-114">Type: **LRESULT**</span></span>

<span data-ttu-id="43384-115">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="43384-115">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="43384-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43384-116">Requirements</span></span>



| <span data-ttu-id="43384-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43384-117">Requirement</span></span> | <span data-ttu-id="43384-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="43384-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43384-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43384-119">Minimum supported client</span></span><br/> | <span data-ttu-id="43384-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43384-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="43384-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43384-121">Minimum supported server</span></span><br/> | <span data-ttu-id="43384-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43384-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="43384-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="43384-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="43384-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43384-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43384-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43384-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="43384-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="43384-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="43384-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="43384-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="43384-128">**\_ENTERSIZEMOVE WM**</span><span class="sxs-lookup"><span data-stu-id="43384-128">**WM\_ENTERSIZEMOVE**</span></span>](wm-entersizemove.md)
</dt> <dt>

<span data-ttu-id="43384-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="43384-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="43384-130">Windows</span><span class="sxs-lookup"><span data-stu-id="43384-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
