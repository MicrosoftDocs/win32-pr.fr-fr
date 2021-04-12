---
title: Message EM_GETHANDLE (winuser. h)
description: Obtient un handle de la mémoire actuellement allouée pour le texte d’un contrôle d’édition multiligne.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- EM_GETHANDLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508922"
---
# <a name="em_gethandle-message"></a><span data-ttu-id="3b187-104">\_Message em GETHANDLE</span><span class="sxs-lookup"><span data-stu-id="3b187-104">EM\_GETHANDLE message</span></span>

<span data-ttu-id="3b187-105">Obtient un handle de la mémoire actuellement allouée pour le texte d’un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="3b187-105">Gets a handle of the memory currently allocated for a multiline edit control's text.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b187-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b187-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b187-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b187-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b187-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3b187-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3b187-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b187-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b187-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3b187-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b187-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b187-111">Return value</span></span>

<span data-ttu-id="3b187-112">La valeur de retour est un handle de mémoire qui identifie la mémoire tampon qui contient le contenu du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="3b187-112">The return value is a memory handle identifying the buffer that holds the content of the edit control.</span></span> <span data-ttu-id="3b187-113">Si une erreur se produit, telle que l’envoi du message à un contrôle d’édition sur une seule ligne, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="3b187-113">If an error occurs, such as sending the message to a single-line edit control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b187-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3b187-114">Remarks</span></span>

<span data-ttu-id="3b187-115">Si la fonction réussit, l’application peut accéder au contenu du contrôle d’édition en effectuant un cast de la valeur de retour vers [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) et en la passant à [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span><span class="sxs-lookup"><span data-stu-id="3b187-115">If the function succeeds, the application can access the contents of the edit control by casting the return value to [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) and passing it to [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span></span> <span data-ttu-id="3b187-116">**LocalLock** retourne un pointeur vers une mémoire tampon qui est un tableau de char s ou **WCHAR** se terminant par un **caractère** null, selon qu’une fonction ANSI ou Unicode a créé le contrôle.</span><span class="sxs-lookup"><span data-stu-id="3b187-116">**LocalLock** returns a pointer to a buffer that is a null-terminated array of **CHAR** s or **WCHAR** s, depending on whether an ANSI or Unicode function created the control.</span></span> <span data-ttu-id="3b187-117">Par exemple, si [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) a été utilisé, la mémoire tampon est un tableau de **char** s, mais si **CreateWindowExW** a été utilisé, la mémoire tampon est un tableau de **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="3b187-117">For example, if [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) was used the buffer is an array of **CHAR** s, but if **CreateWindowExW** was used the buffer is an array of **WCHAR** s.</span></span> <span data-ttu-id="3b187-118">L’application ne peut pas modifier le contenu de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3b187-118">The application may not change the contents of the buffer.</span></span> <span data-ttu-id="3b187-119">Pour déverrouiller la mémoire tampon, l’application appelle [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) avant d’autoriser le contrôle d’édition à recevoir de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="3b187-119">To unlock the buffer, the application calls [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) before allowing the edit control to receive new messages.</span></span>

> [!Note]  
> <span data-ttu-id="3b187-120">Pour Comctl32.dll version 6, la mémoire tampon contient toujours un tableau de **WCHAR** s, qu’une fonction ANSI ou Unicode ait créé le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="3b187-120">For Comctl32.dll version 6, the buffer always contains an array of **WCHAR** s, regardless of whether an ANSI or Unicode function created the edit control.</span></span> <span data-ttu-id="3b187-121">Pour plus d’informations sur les versions de DLL, consultez [versions de contrôle courantes](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="3b187-121">For more information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

 

<span data-ttu-id="3b187-122">Si votre application ne peut pas respecter les restrictions imposées par **em \_ GETHANDLE**, utilisez les fonctions [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) et [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) pour copier le contenu du contrôle d’édition dans une mémoire tampon fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="3b187-122">If your application cannot abide by the restrictions imposed by **EM\_GETHANDLE**, use the [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) and [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) functions to copy the contents of the edit control into an application-provided buffer.</span></span>

<span data-ttu-id="3b187-123">**Modification riche :** Le message de **em \_ GETHANDLE** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3b187-123">**Rich Edit:** The **EM\_GETHANDLE** message is not supported.</span></span> <span data-ttu-id="3b187-124">Les contrôles RichEdit ne stockent pas de texte sous la forme d’un simple tableau de caractères.</span><span class="sxs-lookup"><span data-stu-id="3b187-124">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b187-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b187-125">Requirements</span></span>



| <span data-ttu-id="3b187-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b187-126">Requirement</span></span> | <span data-ttu-id="3b187-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b187-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b187-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b187-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3b187-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b187-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3b187-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b187-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3b187-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b187-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3b187-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b187-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b187-133"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b187-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b187-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b187-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b187-135">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3b187-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3b187-136">**\_SETHANDLE em**</span><span class="sxs-lookup"><span data-stu-id="3b187-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

<span data-ttu-id="3b187-137">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="3b187-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3b187-138">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="3b187-138">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="3b187-139">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="3b187-139">**GetWindowTextLength**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="3b187-140">**LocalLock**</span><span class="sxs-lookup"><span data-stu-id="3b187-140">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[<span data-ttu-id="3b187-141">**LocalUnlock**</span><span class="sxs-lookup"><span data-stu-id="3b187-141">**LocalUnlock**</span></span>](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

