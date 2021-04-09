---
description: Envoyé juste avant que l’IME génère la chaîne de composition à la suite d’une séquence de touches. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: Message WM_IME_STARTCOMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862646"
---
# <a name="wm_ime_startcomposition-message"></a><span data-ttu-id="4a154-104">\_ \_ Message STARTCOMPOSITION de l’IME WM</span><span class="sxs-lookup"><span data-stu-id="4a154-104">WM\_IME\_STARTCOMPOSITION message</span></span>

<span data-ttu-id="4a154-105">Envoyé juste avant que l’IME génère la chaîne de composition à la suite d’une séquence de touches.</span><span class="sxs-lookup"><span data-stu-id="4a154-105">Sent immediately before the IME generates the composition string as a result of a keystroke.</span></span> <span data-ttu-id="4a154-106">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4a154-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="4a154-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a154-107">Parameters</span></span>

<span data-ttu-id="4a154-108">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4a154-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="4a154-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a154-109">Return value</span></span>

<span data-ttu-id="4a154-110">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4a154-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a154-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4a154-111">Remarks</span></span>

<span data-ttu-id="4a154-112">Ce message est une notification à une fenêtre IME permettant d’ouvrir sa fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="4a154-112">This message is a notification to an IME window to open its composition window.</span></span> <span data-ttu-id="4a154-113">Une application doit traiter ce message si elle affiche lui-même des caractères de composition.</span><span class="sxs-lookup"><span data-stu-id="4a154-113">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="4a154-114">Si une application a créé une fenêtre IME, elle doit transmettre ce message à cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4a154-114">If an application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="4a154-115">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) traite le message en le passant à la fenêtre IME par défaut.</span><span class="sxs-lookup"><span data-stu-id="4a154-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes the message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a154-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a154-116">Requirements</span></span>



| <span data-ttu-id="4a154-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a154-117">Requirement</span></span> | <span data-ttu-id="4a154-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a154-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a154-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a154-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4a154-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a154-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4a154-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a154-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4a154-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a154-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4a154-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a154-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a154-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a154-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a154-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a154-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a154-126">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="4a154-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4a154-127">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="4a154-127">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
