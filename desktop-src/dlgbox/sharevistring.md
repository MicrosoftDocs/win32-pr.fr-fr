---
title: Message SHAREVISTRING (COMMDLG. h)
description: Une boîte de dialogue Ouvrir ou enregistrer sous envoie le message SHAREVISTRING Registered à votre procédure de Hook, OFNHookProc, si une violation de partage se produit pour le fichier sélectionné quand l’utilisateur clique sur le bouton OK.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Boîtes de dialogue de message SHAREVISTRING
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79535b66cff62ad0f9d3fd298fdd76bfc9123a3d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590666"
---
# <a name="sharevistring-message"></a><span data-ttu-id="42585-104">Message SHAREVISTRING</span><span class="sxs-lookup"><span data-stu-id="42585-104">SHAREVISTRING message</span></span>

<span data-ttu-id="42585-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="42585-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="42585-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="42585-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="42585-107">Une boîte de dialogue **ouvrir** ou **Enregistrer sous** envoie le message **SHAREVISTRING** Registered à votre procédure de Hook, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), si une violation de partage se produit pour le fichier sélectionné quand l’utilisateur clique sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="42585-107">An **Open** or **Save As** dialog box sends the **SHAREVISTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), if a sharing violation occurs for the selected file when the user clicks the **OK** button.</span></span>


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a><span data-ttu-id="42585-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42585-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42585-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42585-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42585-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="42585-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42585-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42585-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42585-112">Pointeur vers une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="42585-112">A pointer to a [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="42585-113">Le membre **lpstrFile** de cette structure contient le nom de fichier qui a provoqué la violation de partage.</span><span class="sxs-lookup"><span data-stu-id="42585-113">The **lpstrFile** member of this structure contains the file name that caused the sharing violation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42585-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="42585-114">Return value</span></span>

<span data-ttu-id="42585-115">La procédure de raccordement doit retourner l’une des valeurs suivantes pour indiquer comment la boîte de dialogue doit gérer la violation de partage.</span><span class="sxs-lookup"><span data-stu-id="42585-115">The hook procedure must return one of the following values to indicate how the dialog box should handle the sharing violation.</span></span>



| <span data-ttu-id="42585-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="42585-116">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="42585-117">Description</span><span class="sxs-lookup"><span data-stu-id="42585-117">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42585-118"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="42585-118"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="42585-119">Accepter le nom de fichier</span><span class="sxs-lookup"><span data-stu-id="42585-119">Accept the file name</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="42585-120"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="42585-120"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="42585-121">Refuser le nom de fichier, mais ne pas avertir l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="42585-121">Reject the file name but do not warn the user.</span></span> <span data-ttu-id="42585-122">L’application est responsable de l’affichage d’un message d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="42585-122">The application is responsible for displaying a warning message.</span></span><br/> |
| <dl> <span data-ttu-id="42585-123"><dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="42585-123"><dt>**OFN\_SHAREWARN**</dt> <dt>0</dt></span></span> </dl>        | <span data-ttu-id="42585-124">Rejetez le nom de fichier et affichez un message d’avertissement (le même résultat qu’en l’absence de procédure de raccordement).</span><span class="sxs-lookup"><span data-stu-id="42585-124">Reject the file name and displays a warning message (the same result as if there were no hook procedure).</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="42585-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="42585-125">Remarks</span></span>

<span data-ttu-id="42585-126">La procédure de hook doit spécifier la constante **SHAREVISTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="42585-126">The hook procedure must specify the **SHAREVISTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="42585-127">La boîte de dialogue envoie le message **SHAREVISTRING** Registered uniquement si vous n’avez pas spécifié l’indicateur **OFN \_ SHAREAWARE** dans le membre **Flags** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quand vous avez créé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="42585-127">The dialog box sends the **SHAREVISTRING** registered message only if you did not specify the **OFN\_SHAREAWARE** flag in the **Flags** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure when you created the dialog.</span></span>

<span data-ttu-id="42585-128">Si la procédure de raccordement retourne une valeur non définie, la boîte de dialogue répond comme si **OFN \_ SHAREWARN** était retourné.</span><span class="sxs-lookup"><span data-stu-id="42585-128">If the hook procedure returns an undefined value, the dialog box responds as if **OFN\_SHAREWARN** was returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="42585-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="42585-129">Requirements</span></span>



| <span data-ttu-id="42585-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42585-130">Requirement</span></span> | <span data-ttu-id="42585-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="42585-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42585-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42585-132">Minimum supported client</span></span><br/> | <span data-ttu-id="42585-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42585-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="42585-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42585-134">Minimum supported server</span></span><br/> | <span data-ttu-id="42585-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42585-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42585-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="42585-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="42585-137"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42585-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="42585-138">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="42585-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="42585-139">**SHAREVISTRINGW** (Unicode) et **SHAREVISTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="42585-139">**SHAREVISTRINGW** (Unicode) and **SHAREVISTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="42585-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42585-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="42585-141">**Référence**</span><span class="sxs-lookup"><span data-stu-id="42585-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="42585-142">**\_SHAREVIOLATION CDN**</span><span class="sxs-lookup"><span data-stu-id="42585-142">**CDN\_SHAREVIOLATION**</span></span>](cdn-shareviolation.md)
</dt> <dt>

[<span data-ttu-id="42585-143">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="42585-143">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="42585-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="42585-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="42585-145">**Conceptuel**</span><span class="sxs-lookup"><span data-stu-id="42585-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="42585-146">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="42585-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

