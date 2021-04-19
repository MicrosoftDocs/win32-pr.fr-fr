---
description: Envoyé à une fenêtre lorsque sa zone non cliente doit être modifiée pour indiquer un état actif ou inactif.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: Message WM_NCACTIVATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518694"
---
# <a name="wm_ncactivate-message"></a><span data-ttu-id="553a6-103">\_Message WM NCACTIVATE</span><span class="sxs-lookup"><span data-stu-id="553a6-103">WM\_NCACTIVATE message</span></span>

<span data-ttu-id="553a6-104">Envoyé à une fenêtre lorsque sa zone non cliente doit être modifiée pour indiquer un état actif ou inactif.</span><span class="sxs-lookup"><span data-stu-id="553a6-104">Sent to a window when its nonclient area needs to be changed to indicate an active or inactive state.</span></span>

<span data-ttu-id="553a6-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="553a6-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a><span data-ttu-id="553a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="553a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="553a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="553a6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="553a6-108">Indique quand une barre de titre ou une icône doit être modifiée pour indiquer un état actif ou inactif.</span><span class="sxs-lookup"><span data-stu-id="553a6-108">Indicates when a title bar or icon needs to be changed to indicate an active or inactive state.</span></span> <span data-ttu-id="553a6-109">Si une barre de titre ou une icône active doit être dessinée, le paramètre *wParam* a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="553a6-109">If an active title bar or icon is to be drawn, the *wParam* parameter is **TRUE**.</span></span> <span data-ttu-id="553a6-110">Si une barre de titre ou une icône inactive doit être dessinée, *wParam* a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="553a6-110">If an inactive title bar or icon is to be drawn, *wParam* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="553a6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="553a6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="553a6-112">Quand un [style visuel](../controls/themes-overview.md) est actif pour cette fenêtre, ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="553a6-112">When a [visual style](../controls/themes-overview.md) is active for this window, this parameter is not used.</span></span>

<span data-ttu-id="553a6-113">Quand un style visuel n’est pas actif pour cette fenêtre, ce paramètre est un handle vers une région de mise à jour facultative pour la zone non cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="553a6-113">When a visual style is not active for this window, this parameter is a handle to an optional update region for the nonclient area of the window.</span></span> <span data-ttu-id="553a6-114">Si ce paramètre a la valeur-1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ne redessine pas la zone non cliente pour refléter le changement d’État.</span><span class="sxs-lookup"><span data-stu-id="553a6-114">If this parameter is set to -1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not repaint the nonclient area to reflect the state change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="553a6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="553a6-115">Return value</span></span>

<span data-ttu-id="553a6-116">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="553a6-116">Type: **LRESULT**</span></span>

<span data-ttu-id="553a6-117">Lorsque le paramètre *wParam* a la **valeur false**, une application doit retourner **true** pour indiquer que le système doit procéder au traitement par défaut, ou retourner la valeur **false** pour empêcher la modification.</span><span class="sxs-lookup"><span data-stu-id="553a6-117">When the *wParam* parameter is **FALSE**, an application should return **TRUE** to indicate that the system should proceed with the default processing, or it should return **FALSE** to prevent the change.</span></span> <span data-ttu-id="553a6-118">Lorsque *wParam* a la valeur **true**, la valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="553a6-118">When *wParam* is **TRUE**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="553a6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="553a6-119">Remarks</span></span>

<span data-ttu-id="553a6-120">Le traitement des messages liés à la zone non cliente d’une fenêtre standard n’est pas recommandé, car l’application doit être en mesure de dessiner toutes les parties requises de la zone non cliente pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="553a6-120">Processing messages related to the nonclient area of a standard window is not recommended, because the application must be able to draw all the required parts of the nonclient area for the window.</span></span> <span data-ttu-id="553a6-121">Si une application traite ce message, elle doit retourner la **valeur true** pour indiquer au système d’effectuer la modification de la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="553a6-121">If an application does process this message, it must return **TRUE** to direct the system to complete the change of active window.</span></span> <span data-ttu-id="553a6-122">Si la fenêtre est réduite lorsque ce message est reçu, l’application doit transmettre le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="553a6-122">If the window is minimized when this message is received, the application should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="553a6-123">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dessine la barre de titre ou le titre de l’icône dans ses couleurs actives lorsque le paramètre *wParam* a la **valeur true** et dans ses couleurs inactives lorsque *wParam* a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="553a6-123">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the title bar or icon title in its active colors when the *wParam* parameter is **TRUE** and in its inactive colors when *wParam* is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="553a6-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="553a6-124">Requirements</span></span>



| <span data-ttu-id="553a6-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="553a6-125">Requirement</span></span> | <span data-ttu-id="553a6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="553a6-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="553a6-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="553a6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="553a6-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="553a6-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="553a6-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="553a6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="553a6-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="553a6-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="553a6-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="553a6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="553a6-132"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="553a6-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="553a6-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="553a6-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="553a6-134">**Référence**</span><span class="sxs-lookup"><span data-stu-id="553a6-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="553a6-135">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="553a6-135">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="553a6-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="553a6-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="553a6-137">Windows</span><span class="sxs-lookup"><span data-stu-id="553a6-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
