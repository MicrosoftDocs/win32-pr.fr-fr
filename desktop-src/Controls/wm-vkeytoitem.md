---
title: Message WM_VKEYTOITEM (winuser. h)
description: Envoyé par une zone de liste avec le \_ style WANTKEYBOARDINPUT lbs à son propriétaire en réponse à un message « WM KeyOut \_ ».
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- WM_VKEYTOITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "104321669"
---
# <a name="wm_vkeytoitem-message"></a><span data-ttu-id="6acc3-104">\_Message WM VKEYTOITEM</span><span class="sxs-lookup"><span data-stu-id="6acc3-104">WM\_VKEYTOITEM message</span></span>

<span data-ttu-id="6acc3-105">Envoyé par une zone de liste avec le style [**\_ WANTKEYBOARDINPUT lbs**](list-box-styles.md) à son propriétaire en réponse à un message « [**WM \_**](/windows/desktop/inputdev/wm-keydown) KeyOut ».</span><span class="sxs-lookup"><span data-stu-id="6acc3-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span>


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6acc3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6acc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6acc3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6acc3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6acc3-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie le code de la touche virtuelle de la touche sur laquelle l’utilisateur a appuyé.</span><span class="sxs-lookup"><span data-stu-id="6acc3-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the virtual-key code of the key the user pressed.</span></span> <span data-ttu-id="6acc3-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position actuelle du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="6acc3-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="6acc3-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6acc3-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6acc3-111">Handle vers la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="6acc3-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6acc3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6acc3-112">Return value</span></span>

<span data-ttu-id="6acc3-113">La valeur de retour spécifie l’action exécutée par l’application en réponse au message.</span><span class="sxs-lookup"><span data-stu-id="6acc3-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="6acc3-114">Une valeur de retour de-2 indique que l’application a géré tous les aspects de la sélection de l’élément et ne nécessite aucune action supplémentaire de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="6acc3-114">A return value of -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="6acc3-115">(Consultez la section Notes.) Une valeur de retour de-1 indique que la zone de liste doit exécuter l’action par défaut en réponse à la séquence de touches.</span><span class="sxs-lookup"><span data-stu-id="6acc3-115">(See Remarks.) A return value of -1 indicates that the list box should perform the default action in response to the keystroke.</span></span> <span data-ttu-id="6acc3-116">Une valeur de retour supérieure ou égale à 0 spécifie l’index d’un élément dans la zone de liste et indique que la zone de liste doit exécuter l’action par défaut pour la séquence d’entrée sur l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="6acc3-116">A return value of 0 or greater specifies the index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="6acc3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6acc3-117">Remarks</span></span>

<span data-ttu-id="6acc3-118">Une valeur de retour de-2 est valide uniquement pour les clés qui ne sont pas converties en caractères par le contrôle de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="6acc3-118">A return value of -2 is valid only for keys that are not translated into characters by the list box control.</span></span> <span data-ttu-id="6acc3-119">Si le message [**WM \_ keyverse**](/windows/desktop/inputdev/wm-keydown) se traduit par un message [**WM \_ char**](/windows/desktop/inputdev/wm-char) et que l’application traite le message **WM \_ VKEYTOITEM** généré à la suite de la pression sur la touche, la zone de liste ignore la valeur de retour et effectue le traitement par défaut pour ce caractère.</span><span class="sxs-lookup"><span data-stu-id="6acc3-119">If the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message translates to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message and the application processes the **WM\_VKEYTOITEM** message generated as a result of the key press, the list box ignores the return value and does the default processing for that character).</span></span> <span data-ttu-id="6acc3-120">**WM \_ Les messages** KeyOut générés par des clés telles que VK \_ up, VK \_ , VK \_ Next et VK \_ Previous ne sont pas traduits en messages **WM \_ char** .</span><span class="sxs-lookup"><span data-stu-id="6acc3-120">**WM\_KEYDOWN** messages generated by keys such as VK\_UP, VK\_DOWN, VK\_NEXT, and VK\_PREVIOUS are not translated to **WM\_CHAR** messages.</span></span> <span data-ttu-id="6acc3-121">Dans ce cas, le fait de piéger le message **WM \_ VKEYTOITEM** et de retourner-2 empêche la zone de liste d’exécuter le traitement par défaut pour cette clé.</span><span class="sxs-lookup"><span data-stu-id="6acc3-121">In such cases, trapping the **WM\_VKEYTOITEM** message and returning -2 prevents the list box from doing the default processing for that key.</span></span>

<span data-ttu-id="6acc3-122">Pour intercepter les clés qui génèrent un message de type char et effectuer un traitement spécial, l’application doit sous-classer la zone de liste, intercepter les messages [**WM \_ keyverse**](/windows/desktop/inputdev/wm-keydown) et [**WM \_ char**](/windows/desktop/inputdev/wm-char) et traiter les messages de manière appropriée dans la procédure de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="6acc3-122">To trap keys that generate a char message and do special processing, the application must subclass the list box, trap both the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) and [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages, and process the messages appropriately in the subclass procedure.</span></span>

<span data-ttu-id="6acc3-123">Les remarques précédentes s’appliquent aux zones de liste régulières créées avec le style [**\_ WANTKEYBOARDINPUT**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6acc3-123">The preceding remarks apply to regular list boxes that are created with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style.</span></span> <span data-ttu-id="6acc3-124">Si la zone de liste est owner-drawn, l’application doit traiter le message [**WM \_ CHARTOITEM**](wm-chartoitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6acc3-124">If the list box is owner-drawn, the application must process the [**WM\_CHARTOITEM**](wm-chartoitem.md) message.</span></span>

<span data-ttu-id="6acc3-125">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne-1.</span><span class="sxs-lookup"><span data-stu-id="6acc3-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="6acc3-126">Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en valeur **booléenne** et retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="6acc3-126">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="6acc3-127">La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="6acc3-127">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6acc3-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6acc3-128">Requirements</span></span>



| <span data-ttu-id="6acc3-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6acc3-129">Requirement</span></span> | <span data-ttu-id="6acc3-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6acc3-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6acc3-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6acc3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6acc3-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6acc3-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6acc3-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6acc3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6acc3-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6acc3-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6acc3-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="6acc3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6acc3-136"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6acc3-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6acc3-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6acc3-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="6acc3-138">**Référence**</span><span class="sxs-lookup"><span data-stu-id="6acc3-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6acc3-139">**\_CHARTOITEM WM**</span><span class="sxs-lookup"><span data-stu-id="6acc3-139">**WM\_CHARTOITEM**</span></span>](wm-chartoitem.md)
</dt> <dt>

<span data-ttu-id="6acc3-140">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="6acc3-140">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6acc3-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6acc3-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6acc3-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6acc3-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6acc3-143">**WM- \_ touche**</span><span class="sxs-lookup"><span data-stu-id="6acc3-143">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

