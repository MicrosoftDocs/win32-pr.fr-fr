---
title: Message WM_SETCURSOR (winuser. h)
description: Envoyé à une fenêtre si la souris provoque le déplacement du curseur dans une fenêtre et que l’entrée de la souris n’est pas capturée.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032948"
---
# <a name="wm_setcursor-message"></a><span data-ttu-id="652ca-104">\_Message WM SETCURSOR</span><span class="sxs-lookup"><span data-stu-id="652ca-104">WM\_SETCURSOR message</span></span>

<span data-ttu-id="652ca-105">Envoyé à une fenêtre si la souris provoque le déplacement du curseur dans une fenêtre et que l’entrée de la souris n’est pas capturée.</span><span class="sxs-lookup"><span data-stu-id="652ca-105">Sent to a window if the mouse causes the cursor to move within a window and mouse input is not captured.</span></span>


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a><span data-ttu-id="652ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="652ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="652ca-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="652ca-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="652ca-108">Handle de la fenêtre qui contient le curseur.</span><span class="sxs-lookup"><span data-stu-id="652ca-108">A handle to the window that contains the cursor.</span></span>

</dd> <dt>

<span data-ttu-id="652ca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="652ca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="652ca-110">Le mot de poids faible de *lParam* spécifie le résultat du test de positionnement pour la position du curseur.</span><span class="sxs-lookup"><span data-stu-id="652ca-110">The low-order word of *lParam* specifies the hit-test result for the cursor position.</span></span> <span data-ttu-id="652ca-111">Consultez les valeurs de retour de [WM_NCHITTEST](../inputdev/wm-nchittest.md) pour connaître les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="652ca-111">See the return values for [WM_NCHITTEST](../inputdev/wm-nchittest.md) for possible values.</span></span>

<span data-ttu-id="652ca-112">Le mot de poids fort de *lParam* spécifie le message de fenêtre de la souris qui a déclenché cet événement, par exemple [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span><span class="sxs-lookup"><span data-stu-id="652ca-112">The high-order word of *lParam* specifies the mouse window message which triggered this event, such as [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span></span> <span data-ttu-id="652ca-113">Quand la fenêtre passe en mode de menu, cette valeur est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="652ca-113">When the window enters menu mode, this value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="652ca-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="652ca-114">Return value</span></span>

<span data-ttu-id="652ca-115">Si une application traite ce message, elle doit retourner la **valeur true** pour arrêter le traitement ou **false** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="652ca-115">If an application processes this message, it should return **TRUE** to halt further processing or **FALSE** to continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="652ca-116">Notes</span><span class="sxs-lookup"><span data-stu-id="652ca-116">Remarks</span></span>

<span data-ttu-id="652ca-117">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) transmet le message **WM \_ SETCURSOR** à une fenêtre parente avant le traitement.</span><span class="sxs-lookup"><span data-stu-id="652ca-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) function passes the **WM\_SETCURSOR** message to a parent window before processing.</span></span> <span data-ttu-id="652ca-118">Si la fenêtre parente retourne la **valeur true**, le traitement supplémentaire est interrompu.</span><span class="sxs-lookup"><span data-stu-id="652ca-118">If the parent window returns **TRUE**, further processing is halted.</span></span> <span data-ttu-id="652ca-119">Le fait de passer le message à la fenêtre parente d’une fenêtre donne le contrôle de fenêtre parente sur le paramètre du curseur dans une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="652ca-119">Passing the message to a window's parent window gives the parent window control over the cursor's setting in a child window.</span></span> <span data-ttu-id="652ca-120">La fonction **DefWindowProc** utilise également ce message pour définir le curseur sur une flèche si elle ne se trouve pas dans la zone cliente ou sur le curseur de classe inscrit s’il se trouve dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="652ca-120">The **DefWindowProc** function also uses this message to set the cursor to an arrow if it is not in the client area, or to the registered class cursor if it is in the client area.</span></span> <span data-ttu-id="652ca-121">Si le mot de poids faible du paramètre *lParam* est **HTERROR** et que le mot de poids fort de *lParam* spécifie que l’un des boutons de la souris est enfoncé, **DefWindowProc** appelle la fonction [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) .</span><span class="sxs-lookup"><span data-stu-id="652ca-121">If the low-order word of the *lParam* parameter is **HTERROR** and the high-order word of *lParam* specifies that one of the mouse buttons is pressed, **DefWindowProc** calls the [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="652ca-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="652ca-122">Requirements</span></span>



| <span data-ttu-id="652ca-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="652ca-123">Requirement</span></span> | <span data-ttu-id="652ca-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="652ca-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="652ca-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="652ca-125">Minimum supported client</span></span><br/> | <span data-ttu-id="652ca-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="652ca-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="652ca-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="652ca-127">Minimum supported server</span></span><br/> | <span data-ttu-id="652ca-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="652ca-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="652ca-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="652ca-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="652ca-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="652ca-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="652ca-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="652ca-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="652ca-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="652ca-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="652ca-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="652ca-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

<span data-ttu-id="652ca-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="652ca-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="652ca-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="652ca-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="652ca-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="652ca-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="652ca-137">Curseurs</span><span class="sxs-lookup"><span data-stu-id="652ca-137">Cursors</span></span>](cursors.md)
</dt> </dl>

 

