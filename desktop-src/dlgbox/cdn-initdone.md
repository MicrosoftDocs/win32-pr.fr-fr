---
title: CDN_INITDONE le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur lorsque le système a fini de réorganiser les contrôles dans la boîte de dialogue. Le système déplace les contrôles standard pour faire de la place pour les contrôles de la boîte de dialogue enfant.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- Boîtes de dialogue CDN_INITDONE code de notification
topic_type:
- apiref
api_name:
- CDN_INITDONE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b07c25183eced86c3a430621091bed74c53f90d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590796"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="5aea6-105">\_Code de notification CDN INITDONE</span><span class="sxs-lookup"><span data-stu-id="5aea6-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="5aea6-106">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="5aea6-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="5aea6-107">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="5aea6-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="5aea6-108">Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur lorsque le système a fini de réorganiser les contrôles dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="5aea6-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="5aea6-109">Le système déplace les contrôles standard pour faire de la place pour les contrôles de la boîte de dialogue enfant.</span><span class="sxs-lookup"><span data-stu-id="5aea6-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="5aea6-110">Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5aea6-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="5aea6-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5aea6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aea6-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5aea6-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5aea6-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="5aea6-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5aea6-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5aea6-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5aea6-115">Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="5aea6-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="5aea6-116">La structure **OFNOTIFY** contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ INITDONE** .</span><span class="sxs-lookup"><span data-stu-id="5aea6-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aea6-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5aea6-117">Return value</span></span>

<span data-ttu-id="5aea6-118">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5aea6-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aea6-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="5aea6-119">Remarks</span></span>

<span data-ttu-id="5aea6-120">Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="5aea6-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aea6-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5aea6-121">Requirements</span></span>



| <span data-ttu-id="5aea6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5aea6-122">Requirement</span></span> | <span data-ttu-id="5aea6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5aea6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aea6-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5aea6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5aea6-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5aea6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5aea6-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5aea6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5aea6-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5aea6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5aea6-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5aea6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5aea6-129"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5aea6-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aea6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aea6-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="5aea6-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5aea6-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5aea6-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="5aea6-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="5aea6-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="5aea6-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="5aea6-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="5aea6-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="5aea6-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="5aea6-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="5aea6-136">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="5aea6-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="5aea6-137">**Conceptuel**</span><span class="sxs-lookup"><span data-stu-id="5aea6-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5aea6-138">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="5aea6-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

