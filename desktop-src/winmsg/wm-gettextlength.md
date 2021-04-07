---
description: Détermine la longueur, en caractères, du texte associé à une fenêtre.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: Message WM_GETTEXTLENGTH (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952419"
---
# <a name="wm_gettextlength-message"></a><span data-ttu-id="21fd5-103">\_Message WM GETTEXTLENGTH</span><span class="sxs-lookup"><span data-stu-id="21fd5-103">WM\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="21fd5-104">Détermine la longueur, en caractères, du texte associé à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="21fd5-104">Determines the length, in characters, of the text associated with a window.</span></span>


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a><span data-ttu-id="21fd5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21fd5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21fd5-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21fd5-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21fd5-107">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="21fd5-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="21fd5-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21fd5-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21fd5-109">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="21fd5-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21fd5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21fd5-110">Return value</span></span>

<span data-ttu-id="21fd5-111">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="21fd5-111">Type: **LRESULT**</span></span>

<span data-ttu-id="21fd5-112">La valeur de retour correspond à la longueur du texte en caractères, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="21fd5-112">The return value is the length of the text in characters, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="21fd5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="21fd5-113">Remarks</span></span>

<span data-ttu-id="21fd5-114">Pour un contrôle d’édition, le texte à copier correspond au contenu du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="21fd5-114">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="21fd5-115">Pour une zone de liste modifiable, le texte est le contenu de la partie contrôle d’édition (ou texte statique) de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="21fd5-115">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="21fd5-116">Pour un bouton, le texte est le nom du bouton.</span><span class="sxs-lookup"><span data-stu-id="21fd5-116">For a button, the text is the button name.</span></span> <span data-ttu-id="21fd5-117">Pour les autres fenêtres, le texte est le titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="21fd5-117">For other windows, the text is the window title.</span></span> <span data-ttu-id="21fd5-118">Pour déterminer la longueur d’un élément dans une zone de liste, une application peut utiliser le message [**lb \_ GETTEXTLEN**](../controls/lb-gettextlen.md) .</span><span class="sxs-lookup"><span data-stu-id="21fd5-118">To determine the length of an item in a list box, an application can use the [**LB\_GETTEXTLEN**](../controls/lb-gettextlen.md) message.</span></span>

<span data-ttu-id="21fd5-119">Lorsque le message **WM \_ GETTEXTLENGTH** est envoyé, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la longueur, en caractères, du texte.</span><span class="sxs-lookup"><span data-stu-id="21fd5-119">When the **WM\_GETTEXTLENGTH** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns the length, in characters, of the text.</span></span> <span data-ttu-id="21fd5-120">Dans certaines conditions, la fonction **DefWindowProc** retourne une valeur supérieure à la longueur réelle du texte.</span><span class="sxs-lookup"><span data-stu-id="21fd5-120">Under certain conditions, the **DefWindowProc** function returns a value that is larger than the actual length of the text.</span></span> <span data-ttu-id="21fd5-121">Cela se produit avec certains mélanges d’ANSI et Unicode, et est dû au système qui autorise l’existence possible de caractères DBCS (Double-Byte Character Set) dans le texte.</span><span class="sxs-lookup"><span data-stu-id="21fd5-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="21fd5-122">Toutefois, la valeur de retour sera toujours au moins égale à la longueur réelle du texte. vous pouvez donc toujours l’utiliser pour guider l’allocation de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="21fd5-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="21fd5-123">Ce comportement peut se produire lorsqu’une application utilise à la fois des fonctions ANSI et des boîtes de dialogue courantes, qui utilisent Unicode.</span><span class="sxs-lookup"><span data-stu-id="21fd5-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="21fd5-124">Pour obtenir la longueur exacte du texte, utilisez les messages [**WM \_ gettext**](wm-gettext.md), [**lb \_ gettext**](../controls/lb-gettext.md)ou [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) , ou la fonction [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="21fd5-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](wm-gettext.md), [**LB\_GETTEXT**](../controls/lb-gettext.md), or [**CB\_GETLBTEXT**](../controls/cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="21fd5-125">L’envoi d’un message **WM \_ GETTEXTLENGTH** à un contrôle statique non textuel, tel qu’une image bitmap statique ou une icône statique controlc, ne retourne pas de valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="21fd5-125">Sending a **WM\_GETTEXTLENGTH** message to a non-text static control, such as a static bitmap or static icon controlc, does not return a string value.</span></span> <span data-ttu-id="21fd5-126">Au lieu de cela, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="21fd5-126">Instead, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="21fd5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21fd5-127">Requirements</span></span>



| <span data-ttu-id="21fd5-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21fd5-128">Requirement</span></span> | <span data-ttu-id="21fd5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="21fd5-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21fd5-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21fd5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="21fd5-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21fd5-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="21fd5-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21fd5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="21fd5-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21fd5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="21fd5-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="21fd5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="21fd5-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21fd5-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21fd5-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21fd5-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="21fd5-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="21fd5-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="21fd5-138">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="21fd5-138">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="21fd5-139">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="21fd5-139">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="21fd5-140">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="21fd5-140">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="21fd5-141">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="21fd5-141">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="21fd5-142">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="21fd5-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="21fd5-143">Windows</span><span class="sxs-lookup"><span data-stu-id="21fd5-143">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="21fd5-144">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="21fd5-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="21fd5-145">**\_GETLBTEXT CB**</span><span class="sxs-lookup"><span data-stu-id="21fd5-145">**CB\_GETLBTEXT**</span></span>](../controls/cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="21fd5-146">**LB, \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="21fd5-146">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> <dt>

[<span data-ttu-id="21fd5-147">**\_GETTEXTLEN lb**</span><span class="sxs-lookup"><span data-stu-id="21fd5-147">**LB\_GETTEXTLEN**</span></span>](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
