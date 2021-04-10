---
description: Envoyé à une application lorsque la fenêtre IME ne trouve aucun espace pour étendre la zone de la fenêtre de composition. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: Message WM_IME_COMPOSITIONFULL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210931"
---
# <a name="wm_ime_compositionfull-message"></a><span data-ttu-id="9c375-104">\_ \_ Message COMPOSITIONFULL de l’IME WM</span><span class="sxs-lookup"><span data-stu-id="9c375-104">WM\_IME\_COMPOSITIONFULL message</span></span>

<span data-ttu-id="9c375-105">Envoyé à une application lorsque la fenêtre IME ne trouve aucun espace pour étendre la zone de la fenêtre de composition.</span><span class="sxs-lookup"><span data-stu-id="9c375-105">Sent to an application when the IME window finds no space to extend the area for the composition window.</span></span> <span data-ttu-id="9c375-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9c375-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="9c375-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c375-107">Parameters</span></span>

<span data-ttu-id="9c375-108">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="9c375-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="9c375-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c375-109">Return value</span></span>

<span data-ttu-id="9c375-110">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9c375-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c375-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9c375-111">Remarks</span></span>

<span data-ttu-id="9c375-112">L’application doit utiliser la commande [IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) pour spécifier la façon dont la fenêtre doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="9c375-112">The application should use the [IMC\_SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) command to specify how the window should be displayed.</span></span>

<span data-ttu-id="9c375-113">La fenêtre IME, au lieu de l’IME, envoie ce message de notification par la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="9c375-113">The IME window, instead of the IME, sends this notification message by the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c375-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c375-114">Requirements</span></span>



| <span data-ttu-id="9c375-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c375-115">Requirement</span></span> | <span data-ttu-id="9c375-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c375-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c375-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c375-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c375-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c375-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9c375-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c375-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c375-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c375-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c375-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c375-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c375-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c375-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c375-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c375-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c375-124">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="9c375-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="9c375-125">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="9c375-125">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="9c375-126">\_SETCOMPOSITIONWINDOW IMC</span><span class="sxs-lookup"><span data-stu-id="9c375-126">IMC\_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> </dl>

 

 
