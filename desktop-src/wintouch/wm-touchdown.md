---
title: Message WM_TOUCH (winuser. h)
description: Notifie la fenêtre lorsqu’un ou plusieurs points tactiles, tels qu’un doigt ou un stylet, touche une surface de digitaliseur tactile.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH message Windows tactile
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b6242d43b661240d946d2883237640d1bc92b3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384936"
---
# <a name="wm_touch-message"></a><span data-ttu-id="e7f84-104">\_Message WM Touch</span><span class="sxs-lookup"><span data-stu-id="e7f84-104">WM\_TOUCH message</span></span>

<span data-ttu-id="e7f84-105">Notifie la fenêtre lorsqu’un ou plusieurs points tactiles, tels qu’un doigt ou un stylet, touche une surface de digitaliseur tactile.</span><span class="sxs-lookup"><span data-stu-id="e7f84-105">Notifies the window when one or more touch points, such as a finger or pen, touches a touch-sensitive digitizer surface.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7f84-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7f84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7f84-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7f84-108">Le mot de poids faible contient le nombre de points tactiles associés à ce message.</span><span class="sxs-lookup"><span data-stu-id="e7f84-108">The low-order word contains the number of touch points associated with this message.</span></span> <span data-ttu-id="e7f84-109">Le mot de poids fort est réservé à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e7f84-109">The high-order word is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="e7f84-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7f84-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7f84-111">Contient une poignée d’entrée tactile qui peut être utilisée dans un appel à [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) pour récupérer des informations détaillées sur les points tactiles associés à ce message.</span><span class="sxs-lookup"><span data-stu-id="e7f84-111">Contains a touch input handle that can be used in a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) to retrieve detailed information about the touch points associated with this message.</span></span>

<span data-ttu-id="e7f84-112">Ce handle est valide uniquement dans le processus actuel et ne doit pas être passé entre processus, sauf en tant que **lParam** dans un appel **SendMessage** ou **PostMessage** .</span><span class="sxs-lookup"><span data-stu-id="e7f84-112">This handle is valid only within the current process and should not be passed cross-process except as the **LPARAM** in a **SendMessage** or **PostMessage** call.</span></span>

<span data-ttu-id="e7f84-113">Lorsque l’application n’a plus besoin de ce handle, l’application doit appeler **CloseTouchInputHandle** pour libérer la mémoire de processus associée à ce descripteur.</span><span class="sxs-lookup"><span data-stu-id="e7f84-113">When the application no longer requires this handle, the application must call **CloseTouchInputHandle** to free the process memory associated with this handle.</span></span> <span data-ttu-id="e7f84-114">Si ce n’est pas le cas, cela peut entraîner une fuite de mémoire d’application.</span><span class="sxs-lookup"><span data-stu-id="e7f84-114">Failing to do so can result in an application memory leak.</span></span>

<span data-ttu-id="e7f84-115">Notez que le handle d’entrée tactile dans ce paramètre n’est plus valide une fois que le message a été passé à [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="e7f84-115">Note that the touch input handle in this parameter is no longer valid after the message has been passed to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="e7f84-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) va fermer et invalider ce handle.</span><span class="sxs-lookup"><span data-stu-id="e7f84-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will close and invalidate this handle.</span></span>

<span data-ttu-id="e7f84-117">Notez également que le handle d’entrée tactile dans ce paramètre n’est plus valide une fois que le message a été transféré à l’aide de [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage** ou de l’une de ses variantes.</span><span class="sxs-lookup"><span data-stu-id="e7f84-117">Note also that the touch input handle in this parameter is no longer valid after the message has been forwarded using [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage**, or one of their variants.</span></span> <span data-ttu-id="e7f84-118">Ces fonctions vont fermer et invalider ce handle.</span><span class="sxs-lookup"><span data-stu-id="e7f84-118">These functions will close and invalidate this handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f84-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7f84-119">Return value</span></span>

<span data-ttu-id="e7f84-120">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="e7f84-120">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="e7f84-121">Si l’application ne traite pas le message, elle doit appeler [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="e7f84-121">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="e7f84-122">Si ce n’est pas le cas, l’application subit une fuite de mémoire, car le handle d’entrée tactile n’est pas fermé et la mémoire de processus associée n’est pas libérée.</span><span class="sxs-lookup"><span data-stu-id="e7f84-122">Not doing so causes the application to leak memory because the touch input handle is not closed and associated process memory is not freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7f84-123">Notes</span><span class="sxs-lookup"><span data-stu-id="e7f84-123">Remarks</span></span>

<span data-ttu-id="e7f84-124">**WM \_ Les messages TACTILEs** ne respectent pas les régions **HTTRANSPARENT** des fenêtres.</span><span class="sxs-lookup"><span data-stu-id="e7f84-124">**WM\_TOUCH** messages do not respect **HTTRANSPARENT** regions of windows.</span></span> <span data-ttu-id="e7f84-125">Si une fenêtre retourne **HTTRANSPARENT** en réponse à un message **WM \_ NCHITTEST** , les messages de la souris sont dirigés vers le parent et les messages **WM \_ Touch** sont directement dirigés vers la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e7f84-125">If a window returns **HTTRANSPARENT** in response to a **WM\_NCHITTEST** message, mouse messages go to the parent, and **WM\_TOUCH** messages go directly to the window.</span></span>

## <a name="examples"></a><span data-ttu-id="e7f84-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="e7f84-126">Examples</span></span>

<span data-ttu-id="e7f84-127">Le code suivant est un exemple qui montre comment obtenir des informations détaillées sur les entrées tactiles associées à ce message.</span><span class="sxs-lookup"><span data-stu-id="e7f84-127">The following code is an example of how to obtain detailed touch input information associated with this message.</span></span>


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a><span data-ttu-id="e7f84-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7f84-128">Requirements</span></span>



| <span data-ttu-id="e7f84-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7f84-129">Requirement</span></span> | <span data-ttu-id="e7f84-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7f84-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f84-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f84-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e7f84-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7f84-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e7f84-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f84-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e7f84-134">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7f84-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="e7f84-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7f84-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7f84-136"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7f84-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7f84-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f84-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f84-138">Messages</span><span class="sxs-lookup"><span data-stu-id="e7f84-138">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="e7f84-139">Guide de programmation des manipulations et de l’inertie</span><span class="sxs-lookup"><span data-stu-id="e7f84-139">Manipulations and Inertia Programming Guide</span></span>](manipulation-and-inertia.md)
</dt> <dt>

[<span data-ttu-id="e7f84-140">Guide de programmation des entrées tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="e7f84-140">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

