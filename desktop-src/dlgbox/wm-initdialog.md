---
title: Message WM_INITDIALOG (winuser. h)
description: Envoyé à la procédure de boîte de dialogue immédiatement avant l’affichage d’une boîte de dialogue. Les procédures de boîte de dialogue utilisent généralement ce message pour initialiser des contrôles et effectuer d’autres tâches d’initialisation qui affectent l’apparence de la boîte de dialogue.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- Boîtes de dialogue de WM_INITDIALOG message
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513621"
---
# <a name="wm_initdialog-message"></a><span data-ttu-id="38e5c-105">\_Message WM INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="38e5c-105">WM\_INITDIALOG message</span></span>

<span data-ttu-id="38e5c-106">Envoyé à la procédure de boîte de dialogue immédiatement avant l’affichage d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="38e5c-106">Sent to the dialog box procedure immediately before a dialog box is displayed.</span></span> <span data-ttu-id="38e5c-107">Les procédures de boîte de dialogue utilisent généralement ce message pour initialiser des contrôles et effectuer d’autres tâches d’initialisation qui affectent l’apparence de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="38e5c-107">Dialog box procedures typically use this message to initialize controls and carry out any other initialization tasks that affect the appearance of the dialog box.</span></span>


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a><span data-ttu-id="38e5c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38e5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38e5c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38e5c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38e5c-110">Handle du contrôle qui doit recevoir le focus clavier par défaut.</span><span class="sxs-lookup"><span data-stu-id="38e5c-110">A handle to the control to receive the default keyboard focus.</span></span> <span data-ttu-id="38e5c-111">Le système affecte le focus clavier par défaut uniquement si la procédure de boîte de dialogue retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="38e5c-111">The system assigns the default keyboard focus only if the dialog box procedure returns **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="38e5c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38e5c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38e5c-113">Données d’initialisation supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="38e5c-113">Additional initialization data.</span></span> <span data-ttu-id="38e5c-114">Ces données sont passées au système en tant que paramètre *lParam* dans un appel à la [**fonction CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)ou [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) utilisée pour créer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="38e5c-114">This data is passed to the system as the *lParam* parameter in a call to the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), or [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) function used to create the dialog box.</span></span> <span data-ttu-id="38e5c-115">Pour les feuilles de propriétés, ce paramètre est un pointeur vers la structure [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) utilisée pour créer la page.</span><span class="sxs-lookup"><span data-stu-id="38e5c-115">For property sheets, this parameter is a pointer to the [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) structure used to create the page.</span></span> <span data-ttu-id="38e5c-116">Ce paramètre est égal à zéro si une autre fonction de création de boîte de dialogue est utilisée.</span><span class="sxs-lookup"><span data-stu-id="38e5c-116">This parameter is zero if any other dialog box creation function is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38e5c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38e5c-117">Return value</span></span>

<span data-ttu-id="38e5c-118">La procédure de la boîte de dialogue doit retourner **true** pour indiquer au système de définir le focus clavier sur le contrôle spécifié par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="38e5c-118">The dialog box procedure should return **TRUE** to direct the system to set the keyboard focus to the control specified by *wParam*.</span></span> <span data-ttu-id="38e5c-119">Dans le cas contraire, elle doit retourner la **valeur false** pour empêcher le système de définir le focus clavier par défaut.</span><span class="sxs-lookup"><span data-stu-id="38e5c-119">Otherwise, it should return **FALSE** to prevent the system from setting the default keyboard focus.</span></span>

<span data-ttu-id="38e5c-120">La procédure de boîte de dialogue doit retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="38e5c-120">The dialog box procedure should return the value directly.</span></span> <span data-ttu-id="38e5c-121">La valeur **DWL \_ MSGRESULT** définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="38e5c-121">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="38e5c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="38e5c-122">Remarks</span></span>

<span data-ttu-id="38e5c-123">Le contrôle qui doit recevoir le focus clavier par défaut est toujours le premier contrôle dans la boîte de dialogue qui est visible, et non désactivé, et qui a le style **WS \_ TABSTOP** .</span><span class="sxs-lookup"><span data-stu-id="38e5c-123">The control to receive the default keyboard focus is always the first control in the dialog box that is visible, not disabled, and that has the **WS\_TABSTOP** style.</span></span> <span data-ttu-id="38e5c-124">Lorsque la procédure de la boîte de dialogue retourne la **valeur true**, le système vérifie le contrôle pour s’assurer que la procédure ne l’a pas désactivée.</span><span class="sxs-lookup"><span data-stu-id="38e5c-124">When the dialog box procedure returns **TRUE**, the system checks the control to ensure that the procedure has not disabled it.</span></span> <span data-ttu-id="38e5c-125">Si elle a été désactivée, le système définit le focus clavier sur le contrôle suivant qui est visible, non désactivé, et possède le paramètre **WS \_ TABSTOP**.</span><span class="sxs-lookup"><span data-stu-id="38e5c-125">If it has been disabled, the system sets the keyboard focus to the next control that is visible, not disabled, and has the **WS\_TABSTOP**.</span></span>

<span data-ttu-id="38e5c-126">Une application ne peut retourner la **valeur false** que si elle a défini le focus clavier sur l’un des contrôles de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="38e5c-126">An application can return **FALSE** only if it has set the keyboard focus to one of the controls of the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="38e5c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38e5c-127">Requirements</span></span>



| <span data-ttu-id="38e5c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38e5c-128">Requirement</span></span> | <span data-ttu-id="38e5c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="38e5c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e5c-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38e5c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="38e5c-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38e5c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="38e5c-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38e5c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="38e5c-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38e5c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38e5c-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="38e5c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="38e5c-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38e5c-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38e5c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38e5c-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="38e5c-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="38e5c-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38e5c-138">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="38e5c-138">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="38e5c-139">**CreateDialogParam**</span><span class="sxs-lookup"><span data-stu-id="38e5c-139">**CreateDialogParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[<span data-ttu-id="38e5c-140">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="38e5c-140">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="38e5c-141">**DialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="38e5c-141">**DialogBoxParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[<span data-ttu-id="38e5c-142">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="38e5c-142">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="38e5c-143">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="38e5c-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38e5c-144">Boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="38e5c-144">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="38e5c-145">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="38e5c-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="38e5c-146">**PROPSHEETPAGE**</span><span class="sxs-lookup"><span data-stu-id="38e5c-146">**PROPSHEETPAGE**</span></span>](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

