---
title: CDN_INCLUDEITEM le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous pour déterminer si la boîte de dialogue doit afficher un élément dans la liste d’éléments d’un dossier de l’interpréteur de commandes.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- Boîtes de dialogue CDN_INCLUDEITEM code de notification
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f25ea90f8eb37c829cdc86e89f6d7e8cad2312
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549254"
---
# <a name="cdn_includeitem-notification-code"></a><span data-ttu-id="1e1f2-104">\_Code de notification CDN INCLUDEITEM</span><span class="sxs-lookup"><span data-stu-id="1e1f2-104">CDN\_INCLUDEITEM notification code</span></span>

<span data-ttu-id="1e1f2-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="1e1f2-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="1e1f2-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="1e1f2-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="1e1f2-107">Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** pour déterminer si la boîte de dialogue doit afficher un élément dans la liste d’éléments d’un dossier de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="1e1f2-107">Sent by an **Open** or **Save As** dialog box to determine whether the dialog box should display an item in a shell folder's item list.</span></span> <span data-ttu-id="1e1f2-108">Lorsque l’utilisateur ouvre un dossier, la boîte de dialogue envoie une notification **\_ INCLUDEITEM CDN** pour chaque élément du dossier.</span><span class="sxs-lookup"><span data-stu-id="1e1f2-108">When the user opens a folder, the dialog box sends a **CDN\_INCLUDEITEM** notification for each item in the folder.</span></span> <span data-ttu-id="1e1f2-109">La boîte de dialogue envoie cette notification uniquement si l’indicateur **OFN \_ ENABLEINCLUDENOTIFY** a été défini lors de la création de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1e1f2-109">The dialog box sends this notification only if the **OFN\_ENABLEINCLUDENOTIFY** flag was set when the dialog box was created.</span></span>

<span data-ttu-id="1e1f2-110">Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1e1f2-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a><span data-ttu-id="1e1f2-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e1f2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e1f2-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e1f2-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e1f2-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="1e1f2-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f2-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e1f2-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e1f2-115">Pointeur vers une structure [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) .</span><span class="sxs-lookup"><span data-stu-id="1e1f2-115">A pointer to an [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure.</span></span>

<span data-ttu-id="1e1f2-116">La structure [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ INCLUDEITEM** .</span><span class="sxs-lookup"><span data-stu-id="1e1f2-116">The [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INCLUDEITEM** notification message.</span></span>

<span data-ttu-id="1e1f2-117">Le membre des **fibres** discontinues de la structure [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) est un pointeur vers une interface pour le dossier dont les éléments sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="1e1f2-117">The **psf** member of the [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure is a pointer to an interface for the folder whose items are being enumerated.</span></span> <span data-ttu-id="1e1f2-118">Le membre **PIDL** est un pointeur vers une liste d’identificateurs d’éléments qui identifie l’élément par rapport au dossier.</span><span class="sxs-lookup"><span data-stu-id="1e1f2-118">The **pidl** member is a pointer to an item identifier list that identifies the item relative to the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e1f2-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1e1f2-119">Return value</span></span>

<span data-ttu-id="1e1f2-120">Si la procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) retourne la valeur zéro, la boîte de dialogue exclut l’élément de la liste d’éléments.</span><span class="sxs-lookup"><span data-stu-id="1e1f2-120">If the [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure returns zero, the dialog box excludes the item from the list of items.</span></span>

<span data-ttu-id="1e1f2-121">Pour inclure l’élément, retournez une valeur différente de zéro à partir de la procédure de raccordement.</span><span class="sxs-lookup"><span data-stu-id="1e1f2-121">To include the item, return a nonzero value from the hook procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e1f2-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="1e1f2-122">Remarks</span></span>

<span data-ttu-id="1e1f2-123">La boîte de dialogue comprend toujours les éléments qui ont à la fois les attributs **SFGAO \_ FileSystem** et **SFGAO \_ FILESYSANCESTOR** , quelle que soit la valeur retournée par **CDN \_ INCLUDEITEM**.</span><span class="sxs-lookup"><span data-stu-id="1e1f2-123">The dialog box always includes items that have both the **SFGAO\_FILESYSTEM** and **SFGAO\_FILESYSANCESTOR** attributes, regardless of the value returned by **CDN\_INCLUDEITEM**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e1f2-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1e1f2-124">Requirements</span></span>



| <span data-ttu-id="1e1f2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e1f2-125">Requirement</span></span> | <span data-ttu-id="1e1f2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e1f2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e1f2-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e1f2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1e1f2-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e1f2-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1e1f2-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e1f2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1e1f2-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e1f2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e1f2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e1f2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e1f2-132"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e1f2-132"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e1f2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e1f2-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e1f2-134">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="1e1f2-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1e1f2-135">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="1e1f2-135">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="1e1f2-136">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="1e1f2-136">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="1e1f2-137">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="1e1f2-137">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="1e1f2-138">**OFNOTIFYEX**</span><span class="sxs-lookup"><span data-stu-id="1e1f2-138">**OFNOTIFYEX**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

<span data-ttu-id="1e1f2-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1e1f2-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e1f2-140">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="1e1f2-140">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

