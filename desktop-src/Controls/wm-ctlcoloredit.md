---
title: Message WM_CTLCOLOREDIT (winuser. h)
description: Un contrôle d’édition qui n’est pas en lecture seule ou qui est désactivé envoie le \_ message WM CTLCOLOREDIT à sa fenêtre parente lorsque le contrôle va être dessiné.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- WM_CTLCOLOREDIT les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464238"
---
# <a name="wm_ctlcoloredit-message"></a><span data-ttu-id="4dd96-104">\_Message WM CTLCOLOREDIT</span><span class="sxs-lookup"><span data-stu-id="4dd96-104">WM\_CTLCOLOREDIT message</span></span>

<span data-ttu-id="4dd96-105">Un contrôle d’édition qui n’est pas en lecture seule ou qui est désactivé envoie le message **WM \_ CTLCOLOREDIT** à sa fenêtre parente lorsque le contrôle va être dessiné.</span><span class="sxs-lookup"><span data-stu-id="4dd96-105">An edit control that is not read-only or disabled sends the **WM\_CTLCOLOREDIT** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="4dd96-106">En répondant à ce message, la fenêtre parente peut utiliser le handle de contexte de périphérique spécifié pour définir les couleurs de texte et d’arrière-plan du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4dd96-106">By responding to this message, the parent window can use the specified device context handle to set the text and background colors of the edit control.</span></span>


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4dd96-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4dd96-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dd96-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4dd96-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dd96-109">Handle du contexte de périphérique pour la fenêtre de contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4dd96-109">A handle to the device context for the edit control window.</span></span>

</dd> <dt>

<span data-ttu-id="4dd96-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4dd96-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dd96-111">Handle du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4dd96-111">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dd96-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4dd96-112">Return value</span></span>

<span data-ttu-id="4dd96-113">Si une application traite ce message, elle doit retourner le handle d’un pinceau.</span><span class="sxs-lookup"><span data-stu-id="4dd96-113">If an application processes this message, it must return the handle of a brush.</span></span> <span data-ttu-id="4dd96-114">Le système utilise le pinceau pour peindre l’arrière-plan du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4dd96-114">The system uses the brush to paint the background of the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dd96-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4dd96-115">Remarks</span></span>

<span data-ttu-id="4dd96-116">Si l’application retourne un pinceau qu’elle a créée (par exemple, à l’aide de la fonction [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), l’application doit libérer le pinceau.</span><span class="sxs-lookup"><span data-stu-id="4dd96-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="4dd96-117">Si l’application retourne un pinceau système (par exemple, un pinceau qui a été récupéré par la fonction [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), l’application n’a pas besoin de libérer le pinceau.</span><span class="sxs-lookup"><span data-stu-id="4dd96-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="4dd96-118">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut pour le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4dd96-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the edit control.</span></span>

<span data-ttu-id="4dd96-119">Les contrôles d’édition en lecture seule ou désactivés n’envoient pas le message **WM \_ CTLCOLOREDIT** ; à la place, ils envoient le message [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd96-119">Read-only or disabled edit controls do not send the **WM\_CTLCOLOREDIT** message; instead, they send the [**WM\_CTLCOLORSTATIC**](wm-ctlcolorstatic.md) message.</span></span>

<span data-ttu-id="4dd96-120">Le message **WM \_ CTLCOLOREDIT** n’est jamais envoyé entre les threads, il n’est envoyé que dans le même thread.</span><span class="sxs-lookup"><span data-stu-id="4dd96-120">The **WM\_CTLCOLOREDIT** message is never sent between threads, it is only sent within the same thread.</span></span>

<span data-ttu-id="4dd96-121">Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="4dd96-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="4dd96-122">Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="4dd96-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="4dd96-123">La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="4dd96-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="4dd96-124">**Modification riche :** Ce message n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4dd96-124">**Rich Edit:** This message is not supported.</span></span> <span data-ttu-id="4dd96-125">Pour définir la couleur d’arrière-plan d’un contrôle Rich Edit, utilisez le message [**em \_ SETBKGNDCOLOR**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd96-125">To set the background color for a rich edit control, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd96-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4dd96-126">Requirements</span></span>



| <span data-ttu-id="4dd96-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4dd96-127">Requirement</span></span> | <span data-ttu-id="4dd96-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4dd96-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd96-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4dd96-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4dd96-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4dd96-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4dd96-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4dd96-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4dd96-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4dd96-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4dd96-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="4dd96-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dd96-134"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4dd96-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dd96-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4dd96-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="4dd96-136">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4dd96-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4dd96-137">**\_SETBKGNDCOLOR em**</span><span class="sxs-lookup"><span data-stu-id="4dd96-137">**EM\_SETBKGNDCOLOR**</span></span>](em-setbkgndcolor.md)
</dt> <dt>

[<span data-ttu-id="4dd96-138">**\_CTLCOLORSTATIC WM**</span><span class="sxs-lookup"><span data-stu-id="4dd96-138">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="4dd96-139">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="4dd96-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4dd96-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="4dd96-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="4dd96-141">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="4dd96-141">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="4dd96-142">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="4dd96-142">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

