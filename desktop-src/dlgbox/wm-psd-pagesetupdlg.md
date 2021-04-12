---
title: Message d’WM_PSD_PAGESETUPDLG (COMMDLG. h)
description: Notifie une procédure de hook PagePaintHook que la boîte de dialogue mise en page est sur le le présent pour dessiner le contenu de la page d’exemple. La procédure de raccordement peut utiliser ce message pour effectuer des tâches d’initialisation liées au dessin du contenu de la page d’exemple.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- Boîtes de dialogue de WM_PSD_PAGESETUPDLG message
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385211"
---
# <a name="wm_psd_pagesetupdlg-message"></a><span data-ttu-id="9bf89-105">\_ \_ Message PAGESETUPDLG WM</span><span class="sxs-lookup"><span data-stu-id="9bf89-105">WM\_PSD\_PAGESETUPDLG message</span></span>

<span data-ttu-id="9bf89-106">Notifie une procédure de hook [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) que la boîte de dialogue **mise en page** est sur le le présent pour dessiner le contenu de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="9bf89-106">Notifies a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that the **Page Setup** dialog box is about to draw the contents of the sample page.</span></span> <span data-ttu-id="9bf89-107">La procédure de raccordement peut utiliser ce message pour effectuer des tâches d’initialisation liées au dessin du contenu de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="9bf89-107">The hook procedure can use this message to carry out initialization tasks related to drawing the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a><span data-ttu-id="9bf89-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9bf89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bf89-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9bf89-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bf89-110">Le mot de poids faible spécifie une valeur qui indique le format du papier.</span><span class="sxs-lookup"><span data-stu-id="9bf89-110">The low-order word specifies a value that indicates the paper size.</span></span> <span data-ttu-id="9bf89-111">Cette valeur peut être l’une des **valeurs \_ DMPAPER** indiquées dans la description de la structure.</span><span class="sxs-lookup"><span data-stu-id="9bf89-111">This value can be one of the **DMPAPER\_** values listed in the description of the structure.</span></span> <span data-ttu-id="9bf89-112">Le mot de poids fort spécifie l’orientation du papier ou de l’enveloppe, et indique si l’imprimante est un appareil matricielle ou en HPPCL (Hewlett Packard Printer Control Language).</span><span class="sxs-lookup"><span data-stu-id="9bf89-112">The high-order word specifies the orientation of the paper or envelope, and whether the printer is a dot matrix or HPPCL (Hewlett Packard Printer Control Language) device.</span></span> <span data-ttu-id="9bf89-113">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9bf89-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9bf89-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bf89-114">Value</span></span>                                                                             | <span data-ttu-id="9bf89-115">Signification</span><span class="sxs-lookup"><span data-stu-id="9bf89-115">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="9bf89-116"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="9bf89-116"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="9bf89-117">Papier en mode paysage (matricielle)</span><span class="sxs-lookup"><span data-stu-id="9bf89-117">Paper in landscape mode (dot matrix)</span></span><br/>    |
| <dl> <span data-ttu-id="9bf89-118"><dt>0x0003</dt></span><span class="sxs-lookup"><span data-stu-id="9bf89-118"><dt>0x0003</dt></span></span> </dl> | <span data-ttu-id="9bf89-119">Papier en mode paysage (en HPPCL)</span><span class="sxs-lookup"><span data-stu-id="9bf89-119">Paper in landscape mode (HPPCL)</span></span><br/>         |
| <dl> <span data-ttu-id="9bf89-120"><dt>0x0005</dt></span><span class="sxs-lookup"><span data-stu-id="9bf89-120"><dt>0x0005</dt></span></span> </dl> | <span data-ttu-id="9bf89-121">Papier en mode Portrait (matricielle)</span><span class="sxs-lookup"><span data-stu-id="9bf89-121">Paper in portrait mode (dot matrix)</span></span><br/>     |
| <dl> <span data-ttu-id="9bf89-122"><dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="9bf89-122"><dt>0x0007</dt></span></span> </dl> | <span data-ttu-id="9bf89-123">Papier en mode Portrait (en HPPCL)</span><span class="sxs-lookup"><span data-stu-id="9bf89-123">Paper in portrait mode (HPPCL)</span></span><br/>          |
| <dl> <span data-ttu-id="9bf89-124"><dt>0x000b</dt></span><span class="sxs-lookup"><span data-stu-id="9bf89-124"><dt>0x000b</dt></span></span> </dl> | <span data-ttu-id="9bf89-125">Enveloppe en mode paysage (en HPPCL)</span><span class="sxs-lookup"><span data-stu-id="9bf89-125">Envelope in landscape mode (HPPCL)</span></span><br/>      |
| <dl> <span data-ttu-id="9bf89-126"><dt>0x000d</dt></span><span class="sxs-lookup"><span data-stu-id="9bf89-126"><dt>0x000d</dt></span></span> </dl> | <span data-ttu-id="9bf89-127">Enveloppe en mode Portrait (matricielle)</span><span class="sxs-lookup"><span data-stu-id="9bf89-127">Envelope in portrait mode (dot matrix)</span></span><br/>  |
| <dl> <span data-ttu-id="9bf89-128"><dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="9bf89-128"><dt>0x0019</dt></span></span> </dl> | <span data-ttu-id="9bf89-129">Enveloppe en mode paysage (matricielle)</span><span class="sxs-lookup"><span data-stu-id="9bf89-129">Envelope in landscape mode (dot matrix)</span></span><br/> |
| <dl> <span data-ttu-id="9bf89-130"><dt>0x001f</dt></span><span class="sxs-lookup"><span data-stu-id="9bf89-130"><dt>0x001f</dt></span></span> </dl> | <span data-ttu-id="9bf89-131">Enveloppe en mode Portrait (en HPPCL)</span><span class="sxs-lookup"><span data-stu-id="9bf89-131">Envelope in portrait mode (HPPCL)</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="9bf89-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9bf89-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bf89-133">Pointeur vers une structure [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) qui contient des informations utilisées pour initialiser la boîte de dialogue **mise en page** .</span><span class="sxs-lookup"><span data-stu-id="9bf89-133">A pointer to a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure that contains information used to initialize the **Page Setup** dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bf89-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9bf89-134">Return value</span></span>

<span data-ttu-id="9bf89-135">Si la procédure de raccordement retourne la **valeur true**, la boîte de dialogue n’envoie plus de messages et ne dessine pas dans la page d’exemple tant que le système n’a pas besoin de redessiner la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="9bf89-135">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="9bf89-136">Si la procédure de hook retourne la **valeur false**, la boîte de dialogue envoie les messages restants de la séquence de dessin.</span><span class="sxs-lookup"><span data-stu-id="9bf89-136">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bf89-137">Notes</span><span class="sxs-lookup"><span data-stu-id="9bf89-137">Remarks</span></span>

<span data-ttu-id="9bf89-138">La boîte de dialogue **mise en page** comprend une image d’un exemple de page qui montre comment les sélections de l’utilisateur affectent l’apparence de la sortie imprimée.</span><span class="sxs-lookup"><span data-stu-id="9bf89-138">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="9bf89-139">Quand vous appelez la fonction [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , vous pouvez fournir une procédure de hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser l’apparence de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="9bf89-139">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="9bf89-140">Chaque fois que la boîte de dialogue est sur le paragraphe pour dessiner le contenu de la page d’exemple, la boîte de dialogue envoie une séquence de messages à la procédure de raccordement.</span><span class="sxs-lookup"><span data-stu-id="9bf89-140">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="9bf89-141">Les trois premiers messages d’une séquence de dessin (**WM \_ PSD \_ PAGESETUPDLG**, [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)ou [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) fournissent des informations que la procédure de raccordement peut utiliser pour dessiner le contenu de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="9bf89-141">The first three messages of a drawing sequence (**WM\_PSD\_PAGESETUPDLG**, [**WM\_PSD\_FULLPAGERECT**](wm-psd-fullpagerect.md), or [**WM\_PSD\_MINMARGINRECT**](wm-psd-minmarginrect.md)) provide information that the hook procedure can use to draw the contents of the sample page.</span></span> <span data-ttu-id="9bf89-142">Les messages restants ([**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md), [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notifient à la procédure de hook que la boîte de dialogue est sur le point de dessiner une partie spécifique de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="9bf89-142">The remaining messages ([**WM\_PSD\_MARGINRECT**](wm-psd-marginrect.md), [**WM\_PSD\_GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM\_PSD\_ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM\_PSD\_YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notify the hook procedure that the dialog box is about to draw a specific portion of the sample page.</span></span> <span data-ttu-id="9bf89-143">Cela permet à la procédure de raccordement de dessiner des parties de la page d’exemple de manière sélective.</span><span class="sxs-lookup"><span data-stu-id="9bf89-143">This allows the hook procedure to selectively draw portions of the sample page.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bf89-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bf89-144">Requirements</span></span>



| <span data-ttu-id="9bf89-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bf89-145">Requirement</span></span> | <span data-ttu-id="9bf89-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bf89-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf89-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bf89-147">Minimum supported client</span></span><br/> | <span data-ttu-id="9bf89-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9bf89-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9bf89-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bf89-149">Minimum supported server</span></span><br/> | <span data-ttu-id="9bf89-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9bf89-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9bf89-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="9bf89-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bf89-152"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bf89-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bf89-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bf89-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="9bf89-154">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9bf89-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9bf89-155">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="9bf89-155">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="9bf89-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9bf89-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9bf89-157">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="9bf89-157">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="9bf89-158">**\_ENVSTAMPRECT WM \_**</span><span class="sxs-lookup"><span data-stu-id="9bf89-158">**WM\_PSD\_ENVSTAMPRECT**</span></span>](wm-psd-envstamprect.md)
</dt> <dt>

[<span data-ttu-id="9bf89-159">**\_FULLPAGERECT WM \_**</span><span class="sxs-lookup"><span data-stu-id="9bf89-159">**WM\_PSD\_FULLPAGERECT**</span></span>](wm-psd-fullpagerect.md)
</dt> <dt>

[<span data-ttu-id="9bf89-160">**\_GREEKTEXTRECT WM \_**</span><span class="sxs-lookup"><span data-stu-id="9bf89-160">**WM\_PSD\_GREEKTEXTRECT**</span></span>](wm-psd-greektextrect.md)
</dt> <dt>

[<span data-ttu-id="9bf89-161">**\_MARGINRECT WM \_**</span><span class="sxs-lookup"><span data-stu-id="9bf89-161">**WM\_PSD\_MARGINRECT**</span></span>](wm-psd-marginrect.md)
</dt> <dt>

[<span data-ttu-id="9bf89-162">**\_MINMARGINRECT WM \_**</span><span class="sxs-lookup"><span data-stu-id="9bf89-162">**WM\_PSD\_MINMARGINRECT**</span></span>](wm-psd-minmarginrect.md)
</dt> <dt>

[<span data-ttu-id="9bf89-163">**\_YAFULLPAGERECT WM \_**</span><span class="sxs-lookup"><span data-stu-id="9bf89-163">**WM\_PSD\_YAFULLPAGERECT**</span></span>](wm-psd-yafullpagerect.md)
</dt> <dt>

<span data-ttu-id="9bf89-164">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9bf89-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9bf89-165">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="9bf89-165">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

