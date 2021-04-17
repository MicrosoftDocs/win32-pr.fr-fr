---
title: Message d’WM_PSD_ENVSTAMPRECT (COMMDLG. h)
description: Notifie la procédure de raccordement d’une boîte de dialogue de mise en page, PagePaintHook, à laquelle la boîte de dialogue va dessiner le rectangle d’enveloppes de la page d’exemple.
ms.assetid: f193baa0-a084-416e-90c9-9c838758a3d3
keywords:
- Boîtes de dialogue de WM_PSD_ENVSTAMPRECT message
topic_type:
- apiref
api_name:
- WM_PSD_ENVSTAMPRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf13485ab75f51298ef273c7e02ea0253e4244d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466143"
---
# <a name="wm_psd_envstamprect-message"></a><span data-ttu-id="08a3d-104">\_ \_ Message ENVSTAMPRECT WM</span><span class="sxs-lookup"><span data-stu-id="08a3d-104">WM\_PSD\_ENVSTAMPRECT message</span></span>

<span data-ttu-id="08a3d-105">Notifie la procédure de raccordement d’une boîte de dialogue de **mise en page** , [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), à laquelle la boîte de dialogue va dessiner le rectangle d’enveloppes de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="08a3d-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the envelope-stamp rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_ENVSTAMPRECT     (WM_USER+5)
```



## <a name="parameters"></a><span data-ttu-id="08a3d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08a3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a3d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08a3d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08a3d-108">Handle vers le contexte de périphérique pour la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="08a3d-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="08a3d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08a3d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08a3d-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les coordonnées, en pixels, du rectangle de l’horodatage de l’enveloppe.</span><span class="sxs-lookup"><span data-stu-id="08a3d-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the envelope-stamp rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a3d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08a3d-111">Return value</span></span>

<span data-ttu-id="08a3d-112">Si la procédure de raccordement retourne la **valeur true**, la boîte de dialogue ne dessine pas la partie de l’horodatage de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="08a3d-112">If the hook procedure returns **TRUE**, the dialog box does not draw the envelope-stamp portion of the sample page.</span></span>

<span data-ttu-id="08a3d-113">Si la procédure de raccordement retourne la **valeur false**, la boîte de dialogue dessine la partie de l’horodatage de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="08a3d-113">If the hook procedure returns **FALSE**, the dialog box draws the envelope-stamp portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a3d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="08a3d-114">Remarks</span></span>

<span data-ttu-id="08a3d-115">La boîte de dialogue **mise en page** comprend une image d’un exemple de page qui montre comment les sélections de l’utilisateur affectent l’apparence de la sortie imprimée.</span><span class="sxs-lookup"><span data-stu-id="08a3d-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="08a3d-116">Quand vous appelez la fonction [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , vous pouvez fournir une procédure de hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser l’apparence de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="08a3d-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="08a3d-117">Chaque fois que la boîte de dialogue est sur le paragraphe pour dessiner le contenu de la page d’exemple, la boîte de dialogue envoie une séquence de messages à la procédure de raccordement.</span><span class="sxs-lookup"><span data-stu-id="08a3d-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="08a3d-118">Une procédure de raccordement reçoit ce message uniquement si le type de papier sélectionné est une enveloppe.</span><span class="sxs-lookup"><span data-stu-id="08a3d-118">A hook procedure receives this message only if the selected paper type is an envelope.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a3d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08a3d-119">Requirements</span></span>



| <span data-ttu-id="08a3d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08a3d-120">Requirement</span></span> | <span data-ttu-id="08a3d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="08a3d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a3d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08a3d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="08a3d-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08a3d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="08a3d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08a3d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="08a3d-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08a3d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08a3d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="08a3d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="08a3d-127"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08a3d-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a3d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08a3d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="08a3d-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="08a3d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="08a3d-130">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="08a3d-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="08a3d-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08a3d-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="08a3d-132">**\_PAGESETUPDLG WM \_**</span><span class="sxs-lookup"><span data-stu-id="08a3d-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="08a3d-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="08a3d-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="08a3d-134">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="08a3d-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

