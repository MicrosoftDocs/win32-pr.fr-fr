---
title: CDN_FILEOK le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur lorsque l’utilisateur spécifie un nom de fichier et clique sur le bouton OK.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- Boîtes de dialogue CDN_FILEOK code de notification
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511390"
---
# <a name="cdn_fileok-notification-code"></a><span data-ttu-id="9b894-104">\_Code de notification CDN FILEOK</span><span class="sxs-lookup"><span data-stu-id="9b894-104">CDN\_FILEOK notification code</span></span>

<span data-ttu-id="9b894-105">Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur lorsque l’utilisateur spécifie un nom de fichier et clique sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="9b894-105">Sent by an Explorer-style **Open** or **Save As** dialog box when the user specifies a file name and clicks the **OK** button.</span></span>

<span data-ttu-id="9b894-106">Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9b894-106">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="9b894-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b894-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b894-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b894-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b894-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9b894-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9b894-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b894-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b894-111">Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="9b894-111">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="9b894-112">La structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ FILEOK** .</span><span class="sxs-lookup"><span data-stu-id="9b894-112">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FILEOK** notification message.</span></span>

<span data-ttu-id="9b894-113">La structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contient également un pointeur vers une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) dont le membre **lpstrFile** spécifie l’adresse du nom de fichier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="9b894-113">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **lpstrFile** member specifies the address of the selected file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b894-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b894-114">Return value</span></span>

<span data-ttu-id="9b894-115">Si la procédure de raccordement retourne la valeur zéro, la boîte de dialogue accepte le nom de fichier spécifié et se ferme.</span><span class="sxs-lookup"><span data-stu-id="9b894-115">If the hook procedure returns zero, the dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="9b894-116">Pour rejeter le nom de fichier spécifié et forcer la boîte de dialogue à rester ouverte, retournez une valeur différente de zéro à partir de la procédure de raccordement et appelez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour définir une valeur **\_ MSGRESULT DWL** différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="9b894-116">To reject the specified file name and force the dialog box to remain open, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set a nonzero **DWL\_MSGRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b894-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9b894-117">Remarks</span></span>

<span data-ttu-id="9b894-118">Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="9b894-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b894-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b894-119">Requirements</span></span>



| <span data-ttu-id="9b894-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b894-120">Requirement</span></span> | <span data-ttu-id="9b894-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b894-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b894-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b894-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9b894-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b894-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9b894-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b894-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9b894-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b894-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9b894-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b894-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b894-127"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b894-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b894-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b894-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9b894-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9b894-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9b894-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="9b894-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="9b894-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="9b894-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="9b894-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="9b894-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="9b894-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="9b894-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="9b894-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="9b894-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="9b894-135">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="9b894-135">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="9b894-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9b894-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9b894-137">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="9b894-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="9b894-138">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="9b894-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9b894-139">**\_notification WM**</span><span class="sxs-lookup"><span data-stu-id="9b894-139">**WM\_NOTIFY**</span></span>](../controls/wm-notify.md)
</dt> </dl>

 

