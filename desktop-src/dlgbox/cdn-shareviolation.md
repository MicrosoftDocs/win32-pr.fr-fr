---
title: CDN_SHAREVIOLATION le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous d’un navigateur quand l’utilisateur clique sur le bouton OK et qu’une violation de partage réseau se produit pour le fichier sélectionné.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- Boîtes de dialogue CDN_SHAREVIOLATION code de notification
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e79d9c48d3e80d14d83de07c03f7db119ea8e78
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590696"
---
# <a name="cdn_shareviolation-notification-code"></a><span data-ttu-id="14bad-104">\_Code de notification CDN SHAREVIOLATION</span><span class="sxs-lookup"><span data-stu-id="14bad-104">CDN\_SHAREVIOLATION notification code</span></span>

<span data-ttu-id="14bad-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="14bad-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="14bad-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="14bad-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="14bad-107">Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** d’un navigateur quand l’utilisateur clique sur le bouton **OK** et qu’une violation de partage réseau se produit pour le fichier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="14bad-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **OK** button and a network sharing violation occurs for the selected file.</span></span>

<span data-ttu-id="14bad-108">Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="14bad-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="14bad-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14bad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14bad-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14bad-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14bad-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="14bad-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="14bad-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14bad-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14bad-113">Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="14bad-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="14bad-114">Le membre **pszFile** de cette structure est un pointeur vers le nom du fichier qui avait la violation de partage.</span><span class="sxs-lookup"><span data-stu-id="14bad-114">The **pszFile** member of this structure is a pointer to the name of the file that had the sharing violation.</span></span> <span data-ttu-id="14bad-115">La structure **OFNOTIFY** contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ SHAREVIOLATION** .</span><span class="sxs-lookup"><span data-stu-id="14bad-115">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SHAREVIOLATION** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14bad-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="14bad-116">Return value</span></span>

<span data-ttu-id="14bad-117">La valeur de retour indique comment la boîte de dialogue doit gérer la violation de partage.</span><span class="sxs-lookup"><span data-stu-id="14bad-117">The return value indicates how the dialog box should handle the sharing violation.</span></span>

<span data-ttu-id="14bad-118">Si la procédure de raccordement retourne la valeur zéro, la boîte de dialogue affiche le message d’avertissement standard pour une violation de partage.</span><span class="sxs-lookup"><span data-stu-id="14bad-118">If the hook procedure returns zero, the dialog box displays the standard warning message for a sharing violation.</span></span>

<span data-ttu-id="14bad-119">Pour empêcher l’affichage du message d’avertissement standard, retournez une valeur différente de zéro à partir de la procédure de raccordement et appelez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour définir l’une des valeurs de **\_ MSGRESULT DWL** suivantes.</span><span class="sxs-lookup"><span data-stu-id="14bad-119">To prevent the display of the standard warning message, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set one of the following **DWL\_MSGRESULT** values.</span></span>



| <span data-ttu-id="14bad-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="14bad-120">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="14bad-121">Description</span><span class="sxs-lookup"><span data-stu-id="14bad-121">Description</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14bad-122"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="14bad-122"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="14bad-123">Fait en sorte que la boîte de dialogue retourne le nom du fichier sans avertir l’utilisateur de la violation de partage.</span><span class="sxs-lookup"><span data-stu-id="14bad-123">Causes the dialog box to return the file name without warning the user about the sharing violation.</span></span><br/>  |
| <dl> <span data-ttu-id="14bad-124"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="14bad-124"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="14bad-125">Fait en sorte que la boîte de dialogue rejette le nom de fichier sans avertir l’utilisateur de la violation de partage.</span><span class="sxs-lookup"><span data-stu-id="14bad-125">Causes the dialog box to reject the file name without warning the user about the sharing violation.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="14bad-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="14bad-126">Remarks</span></span>

<span data-ttu-id="14bad-127">Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="14bad-127">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="14bad-128">Le système envoie cette notification uniquement si la valeur **OFN \_ SHAREAWARE** n’a pas été spécifiée lors de la création de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="14bad-128">The system sends this notification only if the **OFN\_SHAREAWARE** value was not specified when the dialog box was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="14bad-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="14bad-129">Requirements</span></span>



| <span data-ttu-id="14bad-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14bad-130">Requirement</span></span> | <span data-ttu-id="14bad-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="14bad-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14bad-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14bad-132">Minimum supported client</span></span><br/> | <span data-ttu-id="14bad-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14bad-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="14bad-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14bad-134">Minimum supported server</span></span><br/> | <span data-ttu-id="14bad-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14bad-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="14bad-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="14bad-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="14bad-137"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14bad-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14bad-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14bad-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="14bad-139">**Référence**</span><span class="sxs-lookup"><span data-stu-id="14bad-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="14bad-140">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="14bad-140">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="14bad-141">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="14bad-141">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="14bad-142">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="14bad-142">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="14bad-143">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="14bad-143">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="14bad-144">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="14bad-144">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="14bad-145">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="14bad-145">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="14bad-146">**Conceptuel**</span><span class="sxs-lookup"><span data-stu-id="14bad-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="14bad-147">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="14bad-147">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

