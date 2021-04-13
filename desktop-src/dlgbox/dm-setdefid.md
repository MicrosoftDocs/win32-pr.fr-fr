---
title: Message DM_SETDEFID (winuser. h)
description: Modifie l’identificateur du bouton de commande par défaut d’une boîte de dialogue.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- Boîtes de dialogue de DM_SETDEFID message
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509309"
---
# <a name="dm_setdefid-message"></a><span data-ttu-id="d78af-104">\_Message SETDEFID DM</span><span class="sxs-lookup"><span data-stu-id="d78af-104">DM\_SETDEFID message</span></span>

<span data-ttu-id="d78af-105">Modifie l’identificateur du bouton de commande par défaut d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d78af-105">Changes the identifier of the default push button for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="d78af-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d78af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d78af-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d78af-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d78af-108">Identificateur d’un contrôle de bouton de commande qui devient la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d78af-108">The identifier of a push button control that will become the default.</span></span>

</dd> <dt>

<span data-ttu-id="d78af-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d78af-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d78af-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d78af-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d78af-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d78af-111">Return value</span></span>

<span data-ttu-id="d78af-112">La valeur de retour est toujours **true**.</span><span class="sxs-lookup"><span data-stu-id="d78af-112">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d78af-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d78af-113">Remarks</span></span>

<span data-ttu-id="d78af-114">Ce message est traité par la fonction [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) .</span><span class="sxs-lookup"><span data-stu-id="d78af-114">This message is processed by the [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="d78af-115">Pour définir le bouton de commande par défaut, la fonction peut envoyer des messages [**WM \_ GETDLGCODE**](wm-getdlgcode.md) et [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) au contrôle spécifié et au bouton de commande par défaut actuel.</span><span class="sxs-lookup"><span data-stu-id="d78af-115">To set the default push button, the function can send [**WM\_GETDLGCODE**](wm-getdlgcode.md) and [**BM\_SETSTYLE**](../controls/bm-setstyle.md) messages to the specified control and the current default push button.</span></span>

<span data-ttu-id="d78af-116">L’utilisation du message **DM \_ SETDEFID** peut entraîner l’affichage de plusieurs boutons avec l’état de bouton de commande par défaut.</span><span class="sxs-lookup"><span data-stu-id="d78af-116">Using the **DM\_SETDEFID** message can result in more than one button appearing to have the default push button state.</span></span> <span data-ttu-id="d78af-117">Quand le système affiche une boîte de dialogue, il dessine le premier bouton de commande dans le modèle de boîte de dialogue avec la bordure d’État par défaut.</span><span class="sxs-lookup"><span data-stu-id="d78af-117">When the system brings up a dialog, it draws the first push button in the dialog template with the default state border.</span></span> <span data-ttu-id="d78af-118">L’envoi d’un message **DM \_ SETDEFID** pour modifier le bouton par défaut ne supprimera pas toujours la bordure d’État par défaut du premier bouton de commande.</span><span class="sxs-lookup"><span data-stu-id="d78af-118">Sending a **DM\_SETDEFID** message to change the default button will not always remove the default state border from the first push button.</span></span> <span data-ttu-id="d78af-119">Dans ce cas, l’application doit envoyer un message [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) pour modifier le premier style de bordure du bouton de commande.</span><span class="sxs-lookup"><span data-stu-id="d78af-119">In these cases, the application should send a [**BM\_SETSTYLE**](../controls/bm-setstyle.md) message to change the first push button border style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d78af-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d78af-120">Requirements</span></span>



| <span data-ttu-id="d78af-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d78af-121">Requirement</span></span> | <span data-ttu-id="d78af-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d78af-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d78af-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d78af-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d78af-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d78af-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d78af-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d78af-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d78af-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d78af-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d78af-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="d78af-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d78af-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d78af-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d78af-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d78af-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d78af-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d78af-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d78af-131">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="d78af-131">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="d78af-132">**DM \_ GETDEFID**</span><span class="sxs-lookup"><span data-stu-id="d78af-132">**DM\_GETDEFID**</span></span>](dm-getdefid.md)
</dt> <dt>

[<span data-ttu-id="d78af-133">**\_GETDLGCODE WM**</span><span class="sxs-lookup"><span data-stu-id="d78af-133">**WM\_GETDLGCODE**</span></span>](wm-getdlgcode.md)
</dt> <dt>

<span data-ttu-id="d78af-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d78af-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d78af-135">Boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="d78af-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="d78af-136">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="d78af-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d78af-137">**BM \_ SETSTYLE**</span><span class="sxs-lookup"><span data-stu-id="d78af-137">**BM\_SETSTYLE**</span></span>](../controls/bm-setstyle.md)
</dt> <dt>

[<span data-ttu-id="d78af-138">**\_SETLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="d78af-138">**EM\_SETLIMITTEXT**</span></span>](../controls/em-setlimittext.md)
</dt> </dl>

 

