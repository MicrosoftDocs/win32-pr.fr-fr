---
title: Message d’WM_PSD_MINMARGINRECT (COMMDLG. h)
description: Notifie une procédure de hook PagePaintHook des coordonnées du rectangle de marge dans la page de l’exemple. Une boîte de dialogue mise en page envoie ce message lorsqu’il est sur le présent de dessiner le contenu de la page d’exemple.
ms.assetid: 14977b52-7a6f-4c55-956a-716398a71613
keywords:
- Boîtes de dialogue de WM_PSD_MINMARGINRECT message
topic_type:
- apiref
api_name:
- WM_PSD_MINMARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ec7271026ba7557fcbe3fe17cd890d62eadbca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508949"
---
# <a name="wm_psd_minmarginrect-message"></a><span data-ttu-id="780fa-105">\_ \_ Message MINMARGINRECT WM</span><span class="sxs-lookup"><span data-stu-id="780fa-105">WM\_PSD\_MINMARGINRECT message</span></span>

<span data-ttu-id="780fa-106">Notifie une procédure de hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) des coordonnées du rectangle de marge dans la page de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="780fa-106">Notifies a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure of the coordinates of the margin rectangle in the sample page.</span></span> <span data-ttu-id="780fa-107">Une boîte de dialogue **mise en page** envoie ce message lorsqu’il est sur le présent de dessiner le contenu de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="780fa-107">A **Page Setup** dialog box sends this message when it is about to draw the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_MINMARGINRECT    (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="780fa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="780fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="780fa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="780fa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="780fa-110">Handle vers le contexte de périphérique pour la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="780fa-110">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="780fa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="780fa-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="780fa-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les coordonnées, en pixels, du rectangle de marge minimal.</span><span class="sxs-lookup"><span data-stu-id="780fa-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the minimum margin rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="780fa-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="780fa-113">Return value</span></span>

<span data-ttu-id="780fa-114">Si la procédure de raccordement retourne la **valeur true**, la boîte de dialogue n’envoie plus de messages et ne dessine pas dans la page d’exemple tant que le système n’a pas besoin de redessiner la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="780fa-114">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="780fa-115">Si la procédure de hook retourne la **valeur false**, la boîte de dialogue envoie les messages restants de la séquence de dessin.</span><span class="sxs-lookup"><span data-stu-id="780fa-115">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="780fa-116">Notes</span><span class="sxs-lookup"><span data-stu-id="780fa-116">Remarks</span></span>

<span data-ttu-id="780fa-117">La boîte de dialogue **mise en page** comprend une image d’un exemple de page qui montre comment les sélections de l’utilisateur affectent l’apparence de la sortie imprimée.</span><span class="sxs-lookup"><span data-stu-id="780fa-117">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="780fa-118">Quand vous appelez la fonction [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , vous pouvez fournir une procédure de hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser l’apparence de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="780fa-118">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="780fa-119">Chaque fois que la boîte de dialogue est sur le paragraphe pour dessiner le contenu de la page d’exemple, la boîte de dialogue envoie une séquence de messages à la procédure de raccordement.</span><span class="sxs-lookup"><span data-stu-id="780fa-119">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="780fa-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="780fa-120">Requirements</span></span>



| <span data-ttu-id="780fa-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="780fa-121">Requirement</span></span> | <span data-ttu-id="780fa-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="780fa-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="780fa-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="780fa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="780fa-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="780fa-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="780fa-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="780fa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="780fa-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="780fa-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="780fa-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="780fa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="780fa-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="780fa-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="780fa-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="780fa-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="780fa-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="780fa-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="780fa-131">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="780fa-131">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="780fa-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="780fa-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="780fa-133">**\_PAGESETUPDLG WM \_**</span><span class="sxs-lookup"><span data-stu-id="780fa-133">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="780fa-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="780fa-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="780fa-135">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="780fa-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

