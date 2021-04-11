---
title: CDN_HELP le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous d’un navigateur quand l’utilisateur clique sur le bouton aide.
ms.assetid: 18ee86b2-3446-4de4-a47a-2e44e677f4f7
keywords:
- Boîtes de dialogue CDN_HELP code de notification
topic_type:
- apiref
api_name:
- CDN_HELP
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c73b690b1ac522a985ae121413804c4385e0f2cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105316"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="3d012-104">\_Code de notification d’aide CDN</span><span class="sxs-lookup"><span data-stu-id="3d012-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="3d012-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3d012-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="3d012-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="3d012-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="3d012-107">Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** d’un navigateur quand l’utilisateur clique sur le bouton **aide** .</span><span class="sxs-lookup"><span data-stu-id="3d012-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="3d012-108">Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3d012-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="3d012-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d012-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d012-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d012-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d012-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="3d012-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3d012-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d012-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d012-113">Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="3d012-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="3d012-114">La structure **OFNOTIFY** contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **\_ d’aide CDN** .</span><span class="sxs-lookup"><span data-stu-id="3d012-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d012-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d012-115">Return value</span></span>

<span data-ttu-id="3d012-116">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3d012-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d012-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3d012-117">Remarks</span></span>

<span data-ttu-id="3d012-118">Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="3d012-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d012-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d012-119">Requirements</span></span>



| <span data-ttu-id="3d012-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d012-120">Requirement</span></span> | <span data-ttu-id="3d012-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d012-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d012-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d012-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3d012-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d012-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3d012-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d012-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3d012-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d012-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d012-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d012-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d012-127"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d012-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d012-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d012-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d012-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3d012-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3d012-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="3d012-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="3d012-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="3d012-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="3d012-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="3d012-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="3d012-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="3d012-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="3d012-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="3d012-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="3d012-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3d012-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3d012-136">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="3d012-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

