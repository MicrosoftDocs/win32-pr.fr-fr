---
title: Message HELPMSGSTRING (COMMDLG. h)
description: Une boîte de dialogue commune envoie le message HELPMSGSTRING Registered à la procédure de fenêtre de sa fenêtre propriétaire quand l’utilisateur clique sur le bouton aide.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Boîtes de dialogue de message HELPMSGSTRING
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3f7a883f50b06c8d142cb83bedf0bfa2920191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106012"
---
# <a name="helpmsgstring-message"></a><span data-ttu-id="dbee4-104">Message HELPMSGSTRING</span><span class="sxs-lookup"><span data-stu-id="dbee4-104">HELPMSGSTRING message</span></span>

<span data-ttu-id="dbee4-105">Une boîte de dialogue commune envoie le message **HELPMSGSTRING** Registered à la procédure de fenêtre de sa fenêtre propriétaire quand l’utilisateur clique sur le bouton **aide** .</span><span class="sxs-lookup"><span data-stu-id="dbee4-105">A common dialog box sends the **HELPMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Help** button.</span></span>


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a><span data-ttu-id="dbee4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbee4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dbee4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbee4-108">Handle de la boîte de dialogue commune.</span><span class="sxs-lookup"><span data-stu-id="dbee4-108">A handle to the common dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="dbee4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbee4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbee4-110">Pointeur vers la structure d’initialisation de la boîte de dialogue commune.</span><span class="sxs-lookup"><span data-stu-id="dbee4-110">A pointer to the initialization structure for the common dialog box.</span></span> <span data-ttu-id="dbee4-111">Cette structure peut être une structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) ou [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .</span><span class="sxs-lookup"><span data-stu-id="dbee4-111">This structure can be a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) or [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbee4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbee4-112">Return value</span></span>

<span data-ttu-id="dbee4-113">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="dbee4-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbee4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="dbee4-114">Remarks</span></span>

<span data-ttu-id="dbee4-115">Vous devez spécifier la constante **HELPMSGSTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="dbee4-115">You must specify the **HELPMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="dbee4-116">Lorsque vous créez la boîte de dialogue, utilisez le membre **hwndOwner** de la structure d’initialisation pour identifier la fenêtre de réception des messages **HELPMSGSTRING** .</span><span class="sxs-lookup"><span data-stu-id="dbee4-116">When you create the dialog box, use the **hwndOwner** member of the initialization structure to identify the window to receive **HELPMSGSTRING** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbee4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbee4-117">Requirements</span></span>



| <span data-ttu-id="dbee4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbee4-118">Requirement</span></span> | <span data-ttu-id="dbee4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbee4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbee4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbee4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dbee4-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbee4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dbee4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbee4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dbee4-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbee4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dbee4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbee4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbee4-125"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbee4-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="dbee4-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="dbee4-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dbee4-127">**HELPMSGSTRINGW** (Unicode) et **HELPMSGSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dbee4-127">**HELPMSGSTRINGW** (Unicode) and **HELPMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="dbee4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbee4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="dbee4-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="dbee4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dbee4-130">**\_aide CDN**</span><span class="sxs-lookup"><span data-stu-id="dbee4-130">**CDN\_HELP**</span></span>](cdn-help.md)
</dt> <dt>

[<span data-ttu-id="dbee4-131">**LES ChooseColor.**</span><span class="sxs-lookup"><span data-stu-id="dbee4-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="dbee4-132">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="dbee4-132">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="dbee4-133">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="dbee4-133">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="dbee4-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="dbee4-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="dbee4-135">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="dbee4-135">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[<span data-ttu-id="dbee4-136">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="dbee4-136">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="dbee4-137">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="dbee4-137">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="dbee4-138">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="dbee4-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dbee4-139">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="dbee4-139">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

