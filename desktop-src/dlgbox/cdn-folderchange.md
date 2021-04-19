---
title: CDN_FOLDERCHANGE le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous d’un navigateur lors de l’ouverture d’un nouveau dossier.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- Boîtes de dialogue CDN_FOLDERCHANGE code de notification
topic_type:
- apiref
api_name:
- CDN_FOLDERCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39075bddbd191f60a9f9bcbad745e213fe9a978
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590866"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="e5555-104">\_Code de notification CDN FOLDERCHANGE</span><span class="sxs-lookup"><span data-stu-id="e5555-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="e5555-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="e5555-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="e5555-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="e5555-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="e5555-107">Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** d’un navigateur lors de l’ouverture d’un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="e5555-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="e5555-108">Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e5555-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="e5555-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5555-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5555-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5555-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5555-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="e5555-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5555-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5555-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5555-113">Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="e5555-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="e5555-114">La structure **OFNOTIFY** contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ FOLDERCHANGE** .</span><span class="sxs-lookup"><span data-stu-id="e5555-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5555-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e5555-115">Return value</span></span>

<span data-ttu-id="e5555-116">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="e5555-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5555-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="e5555-117">Remarks</span></span>

<span data-ttu-id="e5555-118">Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="e5555-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="e5555-119">Pour récupérer le chemin d’accès du dossier qui vient d’être ouvert, la procédure de raccordement peut envoyer le message [**CDM \_ GETFOLDERPATH**](cdm-getfolderpath.md) à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e5555-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5555-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e5555-120">Requirements</span></span>



| <span data-ttu-id="e5555-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5555-121">Requirement</span></span> | <span data-ttu-id="e5555-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5555-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5555-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5555-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e5555-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5555-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e5555-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5555-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e5555-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5555-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e5555-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5555-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5555-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5555-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5555-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5555-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5555-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e5555-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e5555-131">**\_GETFOLDERPATH CDM**</span><span class="sxs-lookup"><span data-stu-id="e5555-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="e5555-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="e5555-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="e5555-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="e5555-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="e5555-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="e5555-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="e5555-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="e5555-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="e5555-136">**Conceptuel**</span><span class="sxs-lookup"><span data-stu-id="e5555-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e5555-137">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="e5555-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

