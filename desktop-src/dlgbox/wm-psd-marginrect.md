---
title: Message d’WM_PSD_MARGINRECT (COMMDLG. h)
description: Notifie la procédure de raccordement d’une boîte de dialogue de mise en page, PagePaintHook, que la boîte de dialogue est sur le sujet de dessiner le rectangle de marge de la page d’exemple.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- Boîtes de dialogue de WM_PSD_MARGINRECT message
topic_type:
- apiref
api_name:
- WM_PSD_MARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718cfbe16db53378544d9fca0ab44ade23ffb3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466142"
---
# <a name="wm_psd_marginrect-message"></a><span data-ttu-id="5a86d-104">\_ \_ Message MARGINRECT WM</span><span class="sxs-lookup"><span data-stu-id="5a86d-104">WM\_PSD\_MARGINRECT message</span></span>

<span data-ttu-id="5a86d-105">Notifie la procédure de raccordement d’une boîte de dialogue de **mise en page** , [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que la boîte de dialogue est sur le sujet de dessiner le rectangle de marge de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="5a86d-105">Notifies the hook procedure of a **Page Setup** dialog box, [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## <a name="parameters"></a><span data-ttu-id="5a86d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a86d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a86d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a86d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a86d-108">Handle vers le contexte de périphérique pour la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="5a86d-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="5a86d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a86d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a86d-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les coordonnées, en pixels, du rectangle de marge.</span><span class="sxs-lookup"><span data-stu-id="5a86d-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the margin rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a86d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a86d-111">Return value</span></span>

<span data-ttu-id="5a86d-112">Si la procédure de raccordement retourne la **valeur true**, la boîte de dialogue ne dessine pas le rectangle de marge dans la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="5a86d-112">If the hook procedure returns **TRUE**, the dialog box does not draw the margin rectangle in the sample page.</span></span>

<span data-ttu-id="5a86d-113">Si la procédure de raccordement retourne la **valeur false**, la boîte de dialogue dessine le rectangle de marge dans la page de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="5a86d-113">If the hook procedure returns **FALSE**, the dialog box draws the margin rectangle in the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a86d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5a86d-114">Remarks</span></span>

<span data-ttu-id="5a86d-115">La boîte de dialogue **mise en page** comprend une image d’un exemple de page qui montre comment les sélections de l’utilisateur affectent l’apparence de la sortie imprimée.</span><span class="sxs-lookup"><span data-stu-id="5a86d-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="5a86d-116">Quand vous appelez la fonction [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , vous pouvez fournir une procédure de hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser l’apparence de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="5a86d-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="5a86d-117">Chaque fois que la boîte de dialogue est sur le paragraphe pour dessiner le contenu de la page d’exemple, la boîte de dialogue envoie une séquence de messages à la procédure de raccordement.</span><span class="sxs-lookup"><span data-stu-id="5a86d-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a86d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a86d-118">Requirements</span></span>



| <span data-ttu-id="5a86d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a86d-119">Requirement</span></span> | <span data-ttu-id="5a86d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a86d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a86d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a86d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5a86d-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a86d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5a86d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a86d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5a86d-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a86d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5a86d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a86d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a86d-126"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a86d-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a86d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a86d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="5a86d-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5a86d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5a86d-129">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="5a86d-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="5a86d-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5a86d-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5a86d-131">**\_PAGESETUPDLG WM \_**</span><span class="sxs-lookup"><span data-stu-id="5a86d-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="5a86d-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5a86d-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5a86d-133">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="5a86d-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

