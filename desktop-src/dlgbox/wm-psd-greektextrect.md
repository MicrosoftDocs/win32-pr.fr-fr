---
title: Message d’WM_PSD_GREEKTEXTRECT (COMMDLG. h)
description: Notifie la procédure de raccordement d’une boîte de dialogue de mise en page, PagePaintHook, que la boîte de dialogue est sur le de dessiner du texte grec à l’intérieur du rectangle de marge de la page d’exemple.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- Boîtes de dialogue de WM_PSD_GREEKTEXTRECT message
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0853720bea8cadc8df40d8fa649f644fd00694
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033063"
---
# <a name="wm_psd_greektextrect-message"></a><span data-ttu-id="4f03a-104">\_ \_ Message GREEKTEXTRECT WM</span><span class="sxs-lookup"><span data-stu-id="4f03a-104">WM\_PSD\_GREEKTEXTRECT message</span></span>

<span data-ttu-id="4f03a-105">Notifie la procédure de raccordement d’une boîte de dialogue de **mise en page** , PagePaintHook, que la boîte de dialogue est sur le [](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)de dessiner du texte grec à l’intérieur du rectangle de marge de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="4f03a-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw Greek text inside the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a><span data-ttu-id="4f03a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f03a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f03a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f03a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f03a-108">Handle vers le contexte de périphérique pour la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="4f03a-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="4f03a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f03a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f03a-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les coordonnées, en pixels, du rectangle de texte grec.</span><span class="sxs-lookup"><span data-stu-id="4f03a-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the Greek text rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f03a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f03a-111">Return value</span></span>

<span data-ttu-id="4f03a-112">Si la procédure de raccordement retourne la **valeur true**, la boîte de dialogue ne dessine pas la partie du texte grec de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="4f03a-112">If the hook procedure returns **TRUE**, the dialog box does not draw the Greek text portion of the sample page.</span></span>

<span data-ttu-id="4f03a-113">Si la procédure de raccordement retourne la **valeur false**, la boîte de dialogue dessine la partie du texte grec de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="4f03a-113">If the hook procedure returns **FALSE**, the dialog box draws the Greek text portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f03a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4f03a-114">Remarks</span></span>

<span data-ttu-id="4f03a-115">La boîte de dialogue **mise en page** comprend une image d’un exemple de page qui montre comment les sélections de l’utilisateur affectent l’apparence de la sortie imprimée.</span><span class="sxs-lookup"><span data-stu-id="4f03a-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="4f03a-116">Quand vous appelez la fonction [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , vous pouvez fournir une procédure de hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser l’apparence de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="4f03a-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="4f03a-117">Chaque fois que la boîte de dialogue est sur le paragraphe pour dessiner le contenu de la page d’exemple, la boîte de dialogue envoie une séquence de messages à la procédure de raccordement.</span><span class="sxs-lookup"><span data-stu-id="4f03a-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f03a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f03a-118">Requirements</span></span>



| <span data-ttu-id="4f03a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f03a-119">Requirement</span></span> | <span data-ttu-id="4f03a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f03a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f03a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f03a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f03a-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f03a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4f03a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f03a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f03a-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f03a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4f03a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f03a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f03a-126"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f03a-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f03a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f03a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="4f03a-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4f03a-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4f03a-129">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="4f03a-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="4f03a-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f03a-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4f03a-131">**\_PAGESETUPDLG WM \_**</span><span class="sxs-lookup"><span data-stu-id="4f03a-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="4f03a-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="4f03a-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4f03a-133">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="4f03a-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

