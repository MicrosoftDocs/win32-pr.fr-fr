---
title: Message d’WM_PSD_YAFULLPAGERECT (COMMDLG. h)
description: Notifie la procédure de raccordement d’une boîte de dialogue de mise en page, PagePaintHook, que la boîte de dialogue est sur le de dessiner la partie adresse de retour d’une page d’exemple d’enveloppe.
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- Boîtes de dialogue de WM_PSD_YAFULLPAGERECT message
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb325a8d408724cd865f5f9b70cfe7369fe6ffe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033213"
---
# <a name="wm_psd_yafullpagerect-message"></a><span data-ttu-id="72af6-104">\_ \_ Message YAFULLPAGERECT WM</span><span class="sxs-lookup"><span data-stu-id="72af6-104">WM\_PSD\_YAFULLPAGERECT message</span></span>

<span data-ttu-id="72af6-105">Notifie la procédure de raccordement d’une boîte de dialogue de **mise en page** , PagePaintHook, que la boîte de dialogue est sur le [](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)de dessiner la partie adresse de retour d’une page d’exemple d’enveloppe.</span><span class="sxs-lookup"><span data-stu-id="72af6-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the return address portion of an envelope sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a><span data-ttu-id="72af6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72af6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72af6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72af6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72af6-108">Handle vers le contexte de périphérique pour la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="72af6-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="72af6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72af6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72af6-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les coordonnées, en pixels, de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="72af6-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72af6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72af6-111">Return value</span></span>

<span data-ttu-id="72af6-112">Si la procédure de raccordement retourne la **valeur true**, la boîte de dialogue ne dessine pas la partie adresse de retour d’une page d’exemple d’enveloppe.</span><span class="sxs-lookup"><span data-stu-id="72af6-112">If the hook procedure returns **TRUE**, the dialog box does not draw the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="72af6-113">Si la procédure de raccordement retourne la **valeur false**, la boîte de dialogue dessine la partie adresse de retour d’une page d’exemple d’enveloppe.</span><span class="sxs-lookup"><span data-stu-id="72af6-113">If the hook procedure returns **FALSE**, the dialog box draws the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="72af6-114">Si le type de papier n’est pas une enveloppe, la valeur de retour n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="72af6-114">If the paper type is not an envelope, the return value has no effect.</span></span>

## <a name="remarks"></a><span data-ttu-id="72af6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="72af6-115">Remarks</span></span>

<span data-ttu-id="72af6-116">La boîte de dialogue **mise en page** comprend une image d’un exemple de page qui montre comment les sélections de l’utilisateur affectent l’apparence de la sortie imprimée.</span><span class="sxs-lookup"><span data-stu-id="72af6-116">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="72af6-117">Quand vous appelez la fonction [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , vous pouvez fournir une procédure de hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) pour personnaliser l’apparence de la page d’exemple.</span><span class="sxs-lookup"><span data-stu-id="72af6-117">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="72af6-118">Chaque fois que la boîte de dialogue est sur le paragraphe pour dessiner le contenu de la page d’exemple, la boîte de dialogue envoie une séquence de messages à la procédure de raccordement.</span><span class="sxs-lookup"><span data-stu-id="72af6-118">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="72af6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72af6-119">Requirements</span></span>



| <span data-ttu-id="72af6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72af6-120">Requirement</span></span> | <span data-ttu-id="72af6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="72af6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72af6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72af6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="72af6-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72af6-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="72af6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72af6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="72af6-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72af6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="72af6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="72af6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="72af6-127"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72af6-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72af6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72af6-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="72af6-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="72af6-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="72af6-130">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="72af6-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="72af6-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="72af6-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="72af6-132">**\_PAGESETUPDLG WM \_**</span><span class="sxs-lookup"><span data-stu-id="72af6-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="72af6-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="72af6-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="72af6-134">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="72af6-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

