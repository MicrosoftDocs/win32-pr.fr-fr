---
title: Message FILEOKSTRING (COMMDLG. h)
description: Une boîte de dialogue Ouvrir ou enregistrer sous envoie le message FILEOKSTRING Registered à votre procédure de Hook, OFNHookProc, lorsque l’utilisateur spécifie un nom de fichier et clique sur le bouton OK.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Boîtes de dialogue de message FILEOKSTRING
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24dd07faecc66bc50c408eab36bcbd8c93c460ef
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549214"
---
# <a name="fileokstring-message"></a><span data-ttu-id="2f130-104">Message FILEOKSTRING</span><span class="sxs-lookup"><span data-stu-id="2f130-104">FILEOKSTRING message</span></span>

<span data-ttu-id="2f130-105">\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="2f130-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="2f130-106">Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]</span><span class="sxs-lookup"><span data-stu-id="2f130-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="2f130-107">Une boîte de dialogue **ouvrir** ou **Enregistrer sous** envoie le message **FILEOKSTRING** Registered à votre procédure de Hook, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), lorsque l’utilisateur spécifie un nom de fichier et clique sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="2f130-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="2f130-108">La procédure de raccordement peut accepter le nom de fichier et autoriser la fermeture de la boîte de dialogue, ou refuser le nom de fichier et forcer la boîte de dialogue à rester ouverte.</span><span class="sxs-lookup"><span data-stu-id="2f130-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="2f130-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f130-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f130-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f130-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f130-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="2f130-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f130-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f130-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f130-113">Pointeur vers une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="2f130-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="2f130-114">Le membre **lpstrFile** de cette structure contient le lecteur, le chemin d’accès et le nom de fichier spécifiés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2f130-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f130-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2f130-115">Return value</span></span>

<span data-ttu-id="2f130-116">Si la procédure de raccordement retourne la valeur zéro, la boîte de dialogue **ouvrir** ou **Enregistrer sous** accepte le nom de fichier spécifié et se ferme.</span><span class="sxs-lookup"><span data-stu-id="2f130-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="2f130-117">Si la procédure de raccordement retourne une valeur différente de zéro, la boîte de dialogue **ouvrir** ou **Enregistrer sous** rejette le nom de fichier spécifié et reste ouverte.</span><span class="sxs-lookup"><span data-stu-id="2f130-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f130-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="2f130-118">Remarks</span></span>

<span data-ttu-id="2f130-119">La procédure de hook doit spécifier la constante **FILEOKSTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2f130-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f130-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2f130-120">Requirements</span></span>



| <span data-ttu-id="2f130-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f130-121">Requirement</span></span> | <span data-ttu-id="2f130-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f130-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f130-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f130-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2f130-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f130-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2f130-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f130-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2f130-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f130-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2f130-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f130-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f130-128"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f130-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2f130-129">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="2f130-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2f130-130">**FILEOKSTRINGW** (Unicode) et **FILEOKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2f130-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="2f130-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f130-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f130-132">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="2f130-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f130-133">**\_FILEOK CDN**</span><span class="sxs-lookup"><span data-stu-id="2f130-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="2f130-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="2f130-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="2f130-135">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="2f130-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="2f130-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="2f130-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f130-137">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="2f130-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

