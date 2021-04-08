---
title: Message WM_CTLCOLORDLG (winuser. h)
description: Envoyé à une boîte de dialogue avant que le système ne dessine la boîte de dialogue. En répondant à ce message, la boîte de dialogue peut définir ses couleurs de texte et d’arrière-plan à l’aide du handle de contexte de périphérique d’affichage spécifié.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- Boîtes de dialogue de WM_CTLCOLORDLG message
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740156"
---
# <a name="wm_ctlcolordlg-message"></a><span data-ttu-id="f2a29-105">\_Message WM CTLCOLORDLG</span><span class="sxs-lookup"><span data-stu-id="f2a29-105">WM\_CTLCOLORDLG message</span></span>

<span data-ttu-id="f2a29-106">Envoyé à une boîte de dialogue avant que le système ne dessine la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f2a29-106">Sent to a dialog box before the system draws the dialog box.</span></span> <span data-ttu-id="f2a29-107">En répondant à ce message, la boîte de dialogue peut définir ses couleurs de texte et d’arrière-plan à l’aide du handle de contexte de périphérique d’affichage spécifié.</span><span class="sxs-lookup"><span data-stu-id="f2a29-107">By responding to this message, the dialog box can set its text and background colors using the specified display device context handle.</span></span>


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a><span data-ttu-id="f2a29-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2a29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2a29-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2a29-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2a29-110">Handle du contexte de périphérique pour la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f2a29-110">A handle to the device context for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="f2a29-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2a29-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2a29-112">Handle de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f2a29-112">A handle to the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2a29-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2a29-113">Return value</span></span>

<span data-ttu-id="f2a29-114">Si une application traite ce message, elle doit retourner un handle à un pinceau.</span><span class="sxs-lookup"><span data-stu-id="f2a29-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="f2a29-115">Le système utilise le pinceau pour peindre l’arrière-plan de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f2a29-115">The system uses the brush to paint the background of the dialog box.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2a29-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f2a29-116">Remarks</span></span>

<span data-ttu-id="f2a29-117">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f2a29-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the dialog box.</span></span>

<span data-ttu-id="f2a29-118">Le système ne détruit pas automatiquement le pinceau retourné.</span><span class="sxs-lookup"><span data-stu-id="f2a29-118">The system does not automatically destroy the returned brush.</span></span> <span data-ttu-id="f2a29-119">Il incombe à l’application de détruire le pinceau lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f2a29-119">It is the application's responsibility to destroy the brush when it is no longer needed.</span></span>

<span data-ttu-id="f2a29-120">Le message **WM \_ CTLCOLORDLG** n’est jamais envoyé entre les threads.</span><span class="sxs-lookup"><span data-stu-id="f2a29-120">The **WM\_CTLCOLORDLG** message is never sent between threads.</span></span> <span data-ttu-id="f2a29-121">Elle est envoyée uniquement au sein d’un thread.</span><span class="sxs-lookup"><span data-stu-id="f2a29-121">It is sent only within one thread.</span></span>

<span data-ttu-id="f2a29-122">Notez que le message **WM \_ CTLCOLORDLG** est envoyé à la boîte de dialogue elle-même ; tous les autres \**WM \_ CTLCOLOR \** _ sont envoyés au propriétaire du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f2a29-122">Note that the **WM\_CTLCOLORDLG** message is sent to the dialog box itself; all of the other \**WM\_CTLCOLOR\** _ messages are sent to the owner of the control.</span></span>

<span data-ttu-id="f2a29-123">Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en _ *int \_ ptr*\* et retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="f2a29-123">If a dialog box procedure handles this message, it should cast the desired return value to an _ *INT\_PTR*\* and return the value directly.</span></span> <span data-ttu-id="f2a29-124">Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="f2a29-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="f2a29-125">La valeur **DWL \_ MSGRESULT** définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f2a29-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2a29-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2a29-126">Requirements</span></span>



| <span data-ttu-id="f2a29-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2a29-127">Requirement</span></span> | <span data-ttu-id="f2a29-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2a29-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a29-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2a29-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f2a29-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2a29-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f2a29-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2a29-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f2a29-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2a29-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f2a29-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2a29-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2a29-134"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2a29-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2a29-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2a29-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2a29-136">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f2a29-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f2a29-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="f2a29-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="f2a29-138">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="f2a29-138">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="f2a29-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f2a29-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f2a29-140">Boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="f2a29-140">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="f2a29-141">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="f2a29-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f2a29-142">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="f2a29-142">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="f2a29-143">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="f2a29-143">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

