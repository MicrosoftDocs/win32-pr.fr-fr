---
title: CDN_TYPECHANGE le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur lorsque l’utilisateur sélectionne un nouveau type de fichier dans la zone de liste déroulante types de fichiers.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- Boîtes de dialogue CDN_TYPECHANGE code de notification
topic_type:
- apiref
api_name:
- CDN_TYPECHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 180a16c32fb6e83ea0b17e38b42ce8c729f7685a
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590806"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="be1f7-104">\_Code de notification CDN TYPECHANGE</span><span class="sxs-lookup"><span data-stu-id="be1f7-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="be1f7-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="be1f7-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="be1f7-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="be1f7-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="be1f7-107">Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur lorsque l’utilisateur sélectionne un nouveau type de fichier dans la zone de liste déroulante types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="be1f7-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="be1f7-108">Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="be1f7-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="be1f7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be1f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be1f7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be1f7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be1f7-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="be1f7-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be1f7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be1f7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be1f7-113">Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="be1f7-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="be1f7-114">La structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ TYPECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="be1f7-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="be1f7-115">La structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contient également un pointeur vers une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) dont le membre **nFilterIndex** indique l’index de base un du filtre de type de fichier nouvellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="be1f7-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be1f7-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="be1f7-116">Return value</span></span>

<span data-ttu-id="be1f7-117">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="be1f7-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be1f7-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="be1f7-118">Remarks</span></span>

<span data-ttu-id="be1f7-119">Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="be1f7-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be1f7-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="be1f7-120">Requirements</span></span>



| <span data-ttu-id="be1f7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be1f7-121">Requirement</span></span> | <span data-ttu-id="be1f7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="be1f7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be1f7-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be1f7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="be1f7-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be1f7-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="be1f7-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be1f7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="be1f7-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be1f7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be1f7-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="be1f7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="be1f7-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be1f7-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be1f7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be1f7-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="be1f7-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="be1f7-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="be1f7-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="be1f7-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="be1f7-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="be1f7-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="be1f7-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="be1f7-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="be1f7-134">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="be1f7-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="be1f7-135">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="be1f7-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="be1f7-136">**Conceptuel**</span><span class="sxs-lookup"><span data-stu-id="be1f7-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="be1f7-137">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="be1f7-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

