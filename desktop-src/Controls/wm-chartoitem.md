---
title: Message WM_CHARTOITEM (winuser. h)
description: Envoyé par une zone de liste avec le \_ style WANTKEYBOARDINPUT lbs à son propriétaire en réponse à un \_ message WM char.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- WM_CHARTOITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104322542"
---
# <a name="wm_chartoitem-message"></a><span data-ttu-id="dcea1-104">\_Message WM CHARTOITEM</span><span class="sxs-lookup"><span data-stu-id="dcea1-104">WM\_CHARTOITEM message</span></span>

<span data-ttu-id="dcea1-105">Envoyé par une zone de liste avec le style [**\_ WANTKEYBOARDINPUT lbs**](list-box-styles.md) à son propriétaire en réponse à un message [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="dcea1-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="dcea1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcea1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcea1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dcea1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcea1-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie le code de caractère de la touche sur laquelle l’utilisateur a appuyé.</span><span class="sxs-lookup"><span data-stu-id="dcea1-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the character code of the key the user pressed.</span></span> <span data-ttu-id="dcea1-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position actuelle du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="dcea1-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="dcea1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dcea1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcea1-111">Handle vers la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="dcea1-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcea1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcea1-112">Return value</span></span>

<span data-ttu-id="dcea1-113">La valeur de retour spécifie l’action exécutée par l’application en réponse au message.</span><span class="sxs-lookup"><span data-stu-id="dcea1-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="dcea1-114">Une valeur de retour de-1 ou-2 indique que l’application a géré tous les aspects de la sélection de l’élément et ne nécessite aucune action supplémentaire de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="dcea1-114">A return value of -1 or -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="dcea1-115">Une valeur de retour supérieure ou égale à 0 spécifie l’index de base zéro d’un élément dans la zone de liste et indique que la zone de liste doit exécuter l’action par défaut pour la frappe sur l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="dcea1-115">A return value of 0 or greater specifies the zero-based index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcea1-116">Notes</span><span class="sxs-lookup"><span data-stu-id="dcea1-116">Remarks</span></span>

<span data-ttu-id="dcea1-117">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne-1.</span><span class="sxs-lookup"><span data-stu-id="dcea1-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="dcea1-118">Seules les zones de liste owner-drawn ne disposant pas du style de [**\_ HASSTRINGS lbs**](list-box-styles.md) peuvent recevoir ce message.</span><span class="sxs-lookup"><span data-stu-id="dcea1-118">Only owner-drawn list boxes that do not have the [**LBS\_HASSTRINGS**](list-box-styles.md) style can receive this message.</span></span>

<span data-ttu-id="dcea1-119">Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en valeur **booléenne** et retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="dcea1-119">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="dcea1-120">La valeur *DWL \_ MSGRESULT* définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="dcea1-120">The *DWL\_MSGRESULT* value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcea1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcea1-121">Requirements</span></span>



| <span data-ttu-id="dcea1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcea1-122">Requirement</span></span> | <span data-ttu-id="dcea1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcea1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcea1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcea1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dcea1-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcea1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dcea1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcea1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dcea1-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcea1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dcea1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcea1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcea1-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcea1-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcea1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcea1-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="dcea1-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="dcea1-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dcea1-132">**\_VKEYTOITEM WM**</span><span class="sxs-lookup"><span data-stu-id="dcea1-132">**WM\_VKEYTOITEM**</span></span>](wm-vkeytoitem.md)
</dt> <dt>

<span data-ttu-id="dcea1-133">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="dcea1-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="dcea1-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="dcea1-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="dcea1-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dcea1-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="dcea1-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dcea1-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dcea1-137">**\_caractère WM**</span><span class="sxs-lookup"><span data-stu-id="dcea1-137">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

