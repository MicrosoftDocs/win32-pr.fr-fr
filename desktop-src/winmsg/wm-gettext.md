---
description: Copie le texte qui correspond à une fenêtre dans une mémoire tampon fournie par l’appelant.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: Message WM_GETTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757822"
---
# <a name="wm_gettext-message"></a><span data-ttu-id="dd5be-103">\_Message WM GETTEXT</span><span class="sxs-lookup"><span data-stu-id="dd5be-103">WM\_GETTEXT message</span></span>

<span data-ttu-id="dd5be-104">Copie le texte qui correspond à une fenêtre dans une mémoire tampon fournie par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="dd5be-104">Copies the text that corresponds to a window into a buffer provided by the caller.</span></span>


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a><span data-ttu-id="dd5be-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd5be-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd5be-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd5be-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5be-107">Nombre maximal de caractères à copier, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="dd5be-107">The maximum number of characters to be copied, including the terminating null character.</span></span>

<span data-ttu-id="dd5be-108">La taille de la chaîne dans la mémoire tampon peut être réduite pour les applications ANSI (à un minimum de la moitié de la valeur *wParam* ) en raison de la conversion d’ANSI en Unicode.</span><span class="sxs-lookup"><span data-stu-id="dd5be-108">ANSI applications may have the string in the buffer reduced in size (to a minimum of half that of the *wParam* value) due to conversion from ANSI to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="dd5be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd5be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5be-110">Pointeur vers la mémoire tampon qui doit recevoir le texte.</span><span class="sxs-lookup"><span data-stu-id="dd5be-110">A pointer to the buffer that is to receive the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd5be-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd5be-111">Return value</span></span>

<span data-ttu-id="dd5be-112">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="dd5be-112">Type: **LRESULT**</span></span>

<span data-ttu-id="dd5be-113">La valeur de retour est le nombre de caractères copiés, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="dd5be-113">The return value is the number of characters copied, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd5be-114">Notes</span><span class="sxs-lookup"><span data-stu-id="dd5be-114">Remarks</span></span>

<span data-ttu-id="dd5be-115">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copie le texte associé à la fenêtre dans la mémoire tampon spécifiée et retourne le nombre de caractères copiés.</span><span class="sxs-lookup"><span data-stu-id="dd5be-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function copies the text associated with the window into the specified buffer and returns the number of characters copied.</span></span> <span data-ttu-id="dd5be-116">Notez que pour les contrôles statiques non textuels, vous obtenez le texte avec lequel le contrôle a été créé à l’origine, c’est-à-dire le numéro d’identification.</span><span class="sxs-lookup"><span data-stu-id="dd5be-116">Note, for non-text static controls this gives you the text with which the control was originally created, that is, the ID number.</span></span> <span data-ttu-id="dd5be-117">Toutefois, il vous donne l’ID du contrôle statique non textuel tel qu’il a été créé à l’origine.</span><span class="sxs-lookup"><span data-stu-id="dd5be-117">However, it gives you the ID of the non-text static control as originally created.</span></span> <span data-ttu-id="dd5be-118">Autrement dit, si vous utilisiez par la suite un **\_ SETIMAGE STM** pour le modifier, l’ID d’origine est toujours retourné.</span><span class="sxs-lookup"><span data-stu-id="dd5be-118">That is, if you subsequently used a **STM\_SETIMAGE** to change it the original ID would still be returned.</span></span>

<span data-ttu-id="dd5be-119">Pour un contrôle d’édition, le texte à copier correspond au contenu du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="dd5be-119">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="dd5be-120">Pour une zone de liste modifiable, le texte est le contenu de la partie contrôle d’édition (ou texte statique) de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="dd5be-120">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="dd5be-121">Pour un bouton, le texte est le nom du bouton.</span><span class="sxs-lookup"><span data-stu-id="dd5be-121">For a button, the text is the button name.</span></span> <span data-ttu-id="dd5be-122">Pour les autres fenêtres, le texte est le titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dd5be-122">For other windows, the text is the window title.</span></span> <span data-ttu-id="dd5be-123">Pour copier le texte d’un élément dans une zone de liste, une application peut utiliser le message d’attente [**\_ GETTEXT**](../controls/lb-gettext.md) .</span><span class="sxs-lookup"><span data-stu-id="dd5be-123">To copy the text of an item in a list box, an application can use the [**LB\_GETTEXT**](../controls/lb-gettext.md) message.</span></span>

<span data-ttu-id="dd5be-124">Lorsque le message **WM \_ GETTEXT** est envoyé à un contrôle statique avec le style d' **\_ icône SS** , un handle vers l’icône est retourné dans les quatre premiers octets de la mémoire tampon pointée par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="dd5be-124">When the **WM\_GETTEXT** message is sent to a static control with the **SS\_ICON** style, a handle to the icon will be returned in the first four bytes of the buffer pointed to by *lParam*.</span></span> <span data-ttu-id="dd5be-125">Cela est vrai uniquement si le message [**WM \_ SETTEXT**](wm-settext.md) a été utilisé pour définir l’icône.</span><span class="sxs-lookup"><span data-stu-id="dd5be-125">This is true only if the [**WM\_SETTEXT**](wm-settext.md) message has been used to set the icon.</span></span>

<span data-ttu-id="dd5be-126">**Modification riche :** Si le texte à copier dépasse 64 Ko, utilisez le message [**em \_ STREAMOUT**](../controls/em-streamout.md) ou [**em \_ GETSELTEXT**](../controls/em-getseltext.md) .</span><span class="sxs-lookup"><span data-stu-id="dd5be-126">**Rich Edit:** If the text to be copied exceeds 64K, use either the [**EM\_STREAMOUT**](../controls/em-streamout.md) or [**EM\_GETSELTEXT**](../controls/em-getseltext.md) message.</span></span>

<span data-ttu-id="dd5be-127">L’envoi d’un message **WM \_ GETTEXT** à un contrôle statique non textuel, tel qu’une image bitmap statique ou un contrôle d’icône statique, ne retourne pas de valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="dd5be-127">Sending a **WM\_GETTEXT** message to a non-text static control, such as a static bitmap or static icon control, does not return a string value.</span></span> <span data-ttu-id="dd5be-128">Au lieu de cela, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="dd5be-128">Instead, it returns zero.</span></span> <span data-ttu-id="dd5be-129">De plus, dans les versions antérieures de Windows, les applications pouvaient envoyer un message **WM \_ GETTEXT** à un contrôle statique non textuel pour récupérer l’ID du contrôle.</span><span class="sxs-lookup"><span data-stu-id="dd5be-129">In addition, in early versions of Windows, applications could send a **WM\_GETTEXT** message to a non-text static control to retrieve the control's ID.</span></span> <span data-ttu-id="dd5be-130">Pour récupérer l’ID d’un contrôle, les applications peuvent utiliser [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) en passant l' **\_ ID de GWL** en tant que valeur d’index ou [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) à l’aide de l' **\_ ID GWLP**.</span><span class="sxs-lookup"><span data-stu-id="dd5be-130">To retrieve a control's ID, applications can use [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passing **GWL\_ID** as the index value or [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) using **GWLP\_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd5be-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd5be-131">Requirements</span></span>



| <span data-ttu-id="dd5be-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd5be-132">Requirement</span></span> | <span data-ttu-id="dd5be-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd5be-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd5be-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd5be-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dd5be-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd5be-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dd5be-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd5be-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dd5be-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd5be-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dd5be-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd5be-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd5be-139"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd5be-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd5be-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd5be-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="dd5be-141">**Référence**</span><span class="sxs-lookup"><span data-stu-id="dd5be-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dd5be-142">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="dd5be-142">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="dd5be-143">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="dd5be-143">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[<span data-ttu-id="dd5be-144">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="dd5be-144">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[<span data-ttu-id="dd5be-145">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="dd5be-145">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="dd5be-146">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="dd5be-146">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="dd5be-147">**\_GETTEXTLENGTH WM**</span><span class="sxs-lookup"><span data-stu-id="dd5be-147">**WM\_GETTEXTLENGTH**</span></span>](wm-gettextlength.md)
</dt> <dt>

[<span data-ttu-id="dd5be-148">**WM, \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="dd5be-148">**WM\_SETTEXT**</span></span>](wm-settext.md)
</dt> <dt>

<span data-ttu-id="dd5be-149">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="dd5be-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dd5be-150">Windows</span><span class="sxs-lookup"><span data-stu-id="dd5be-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="dd5be-151">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="dd5be-151">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="dd5be-152">**\_GETSELTEXT em**</span><span class="sxs-lookup"><span data-stu-id="dd5be-152">**EM\_GETSELTEXT**</span></span>](../controls/em-getseltext.md)
</dt> <dt>

[<span data-ttu-id="dd5be-153">**\_STREAMOUT em**</span><span class="sxs-lookup"><span data-stu-id="dd5be-153">**EM\_STREAMOUT**</span></span>](../controls/em-streamout.md)
</dt> <dt>

[<span data-ttu-id="dd5be-154">**LB, \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="dd5be-154">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> </dl>

 

 
