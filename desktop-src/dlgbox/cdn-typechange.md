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
ms.openlocfilehash: 3922dd71b70ace579fa4b5f2318776779afdfa4e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548864"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="d332f-104">\_Code de notification CDN TYPECHANGE</span><span class="sxs-lookup"><span data-stu-id="d332f-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="d332f-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="d332f-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="d332f-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="d332f-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="d332f-107">Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur lorsque l’utilisateur sélectionne un nouveau type de fichier dans la zone de liste déroulante types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d332f-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="d332f-108">Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d332f-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="d332f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d332f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d332f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d332f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d332f-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d332f-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d332f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d332f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d332f-113">Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="d332f-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="d332f-114">La structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ TYPECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="d332f-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="d332f-115">La structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contient également un pointeur vers une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) dont le membre **nFilterIndex** indique l’index de base un du filtre de type de fichier nouvellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d332f-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d332f-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d332f-116">Return value</span></span>

<span data-ttu-id="d332f-117">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="d332f-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d332f-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="d332f-118">Remarks</span></span>

<span data-ttu-id="d332f-119">Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="d332f-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d332f-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d332f-120">Requirements</span></span>



| <span data-ttu-id="d332f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d332f-121">Requirement</span></span> | <span data-ttu-id="d332f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d332f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d332f-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d332f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d332f-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d332f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d332f-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d332f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d332f-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d332f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d332f-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="d332f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d332f-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d332f-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d332f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d332f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d332f-130">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="d332f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d332f-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="d332f-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="d332f-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="d332f-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="d332f-133">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="d332f-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="d332f-134">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="d332f-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="d332f-135">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="d332f-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="d332f-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d332f-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d332f-137">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="d332f-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

