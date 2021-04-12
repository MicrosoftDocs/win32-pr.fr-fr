---
title: CDN_SELCHANGE le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur lorsque la sélection change dans la zone de liste qui affiche le contenu du dossier ou du répertoire actuellement ouvert.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- Boîtes de dialogue CDN_SELCHANGE code de notification
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2f0f5a7860c7d729340a84bd80bc4e5713c733
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465282"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="9c9eb-104">\_Code de notification CDN selChange</span><span class="sxs-lookup"><span data-stu-id="9c9eb-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="9c9eb-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c9eb-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="9c9eb-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="9c9eb-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="9c9eb-107">Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur lorsque la sélection change dans la zone de liste qui affiche le contenu du dossier ou du répertoire actuellement ouvert.</span><span class="sxs-lookup"><span data-stu-id="9c9eb-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="9c9eb-108">Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9c9eb-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="9c9eb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c9eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c9eb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c9eb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c9eb-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9c9eb-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c9eb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c9eb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c9eb-113">Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="9c9eb-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="9c9eb-114">La structure **OFNOTIFY** contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ selChange** .</span><span class="sxs-lookup"><span data-stu-id="9c9eb-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c9eb-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c9eb-115">Return value</span></span>

<span data-ttu-id="9c9eb-116">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="9c9eb-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c9eb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9c9eb-117">Remarks</span></span>

<span data-ttu-id="9c9eb-118">Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="9c9eb-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="9c9eb-119">Pour récupérer le nom du fichier ou du dossier que vous venez de sélectionner, la procédure de hook peut envoyer le message [**CDM \_ GETFILEPATH**](cdm-getfilepath.md) ou [**CDM \_ GETSPEC**](cdm-getspec.md) à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9c9eb-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c9eb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c9eb-120">Requirements</span></span>



| <span data-ttu-id="9c9eb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c9eb-121">Requirement</span></span> | <span data-ttu-id="9c9eb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c9eb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9eb-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c9eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9c9eb-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c9eb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9c9eb-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c9eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9c9eb-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c9eb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c9eb-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c9eb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c9eb-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c9eb-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c9eb-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c9eb-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c9eb-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9c9eb-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c9eb-131">**\_GETFILEPATH CDM**</span><span class="sxs-lookup"><span data-stu-id="9c9eb-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="9c9eb-132">**\_GETSPEC CDM**</span><span class="sxs-lookup"><span data-stu-id="9c9eb-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="9c9eb-133">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="9c9eb-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="9c9eb-134">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="9c9eb-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="9c9eb-135">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="9c9eb-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="9c9eb-136">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="9c9eb-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="9c9eb-137">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9c9eb-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9c9eb-138">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="9c9eb-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

