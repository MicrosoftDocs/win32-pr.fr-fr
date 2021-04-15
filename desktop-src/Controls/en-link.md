---
title: Code de notification EN_LINK (RichEdit. h)
description: Un contrôle RichEdit envoie \_ des codes de notification en lien lorsqu’il reçoit divers messages, par exemple lorsque l’utilisateur clique sur la souris ou lorsque le pointeur de la souris se trouve sur le texte qui a l' \_ effet de lien CFE.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- Contrôles Windows de code de notification EN_LINK
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466534"
---
# <a name="en_link-notification-code"></a><span data-ttu-id="cdac0-104">\_Code de notification en lien</span><span class="sxs-lookup"><span data-stu-id="cdac0-104">EN\_LINK notification code</span></span>

<span data-ttu-id="cdac0-105">Un contrôle RichEdit envoie \_ des codes de notification en lien lorsqu’il reçoit divers messages, par exemple lorsque l’utilisateur clique sur la souris ou lorsque le pointeur de la souris se trouve sur le texte qui a l’effet de **\_ lien CFE** .</span><span class="sxs-lookup"><span data-stu-id="cdac0-105">A rich edit control sends EN\_LINK notification codes when it receives various messages, for example, when the user clicks the mouse or when the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="cdac0-106">Un contrôle RichEdit sans fenêtre envoie cette notification à l’aide de la méthode [**ITextHost :: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .</span><span class="sxs-lookup"><span data-stu-id="cdac0-106">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span> <span data-ttu-id="cdac0-107">La fenêtre parente du contrôle reçoit ce code de notification via un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cdac0-107">The parent window of the control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cdac0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdac0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdac0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cdac0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdac0-110">ID de fenêtre récupéré en appelant la fonction [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) avec la \_ valeur d’ID GWL.</span><span class="sxs-lookup"><span data-stu-id="cdac0-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="cdac0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cdac0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdac0-112">Pointeur désignant une structure d' [**enlien**](/windows/desktop/api/Richedit/ns-richedit-enlink) .</span><span class="sxs-lookup"><span data-stu-id="cdac0-112">Pointer to an [**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink) structure.</span></span> <span data-ttu-id="cdac0-113">La structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , des informations sur le code de notification et une structure [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) qui indique la plage de caractères qui ont l’effet de **\_ lien CFE** .</span><span class="sxs-lookup"><span data-stu-id="cdac0-113">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, information about the notification code, and a [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that indicates the range of characters that have the **CFE\_LINK** effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdac0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cdac0-114">Return value</span></span>

<span data-ttu-id="cdac0-115">Retourne zéro pour permettre au contrôle de poursuivre sa gestion normale du message.</span><span class="sxs-lookup"><span data-stu-id="cdac0-115">Return zero to allow the control to proceed with its normal handling of the message.</span></span>

<span data-ttu-id="cdac0-116">Retourne une valeur différente de zéro pour empêcher le contrôle de gérer le message.</span><span class="sxs-lookup"><span data-stu-id="cdac0-116">Return a nonzero value to prevent the control from handling the message.</span></span>

<span data-ttu-id="cdac0-117">**Windows 8**: Return en lien permet d’indiquer **\_ \_ \_ par défaut** au contrôle RichEdit d’exécuter l’action par défaut.</span><span class="sxs-lookup"><span data-stu-id="cdac0-117">**Windows 8**: Return **EN\_LINK\_DO\_DEFAULT** to direct the rich edit control to perform the default action.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdac0-118">Notes</span><span class="sxs-lookup"><span data-stu-id="cdac0-118">Remarks</span></span>

<span data-ttu-id="cdac0-119">Pour recevoir des codes de notification en **\_ lien** lorsque le lien a le focus, spécifiez l’indicateur de [**\_ lien ENM**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="cdac0-119">To receive **EN\_LINK** notification codes when the link has focus, specify the [**ENM\_LINK**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="cdac0-120">Si le lien n’a pas le focus, pour recevoir les codes de notification en **\_ lien** , spécifiez l’indicateur **\_ NOFOCUSLINKNOTIFY ses** dans le masque envoyé avec le message [**em \_ SETEDITSTYLE**](em-seteditstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="cdac0-120">If the link has no focus, to receive **EN\_LINK** notification codes specify the **SES\_NOFOCUSLINKNOTIFY** flag in the mask sent with the [**EM\_SETEDITSTYLE**](em-seteditstyle.md) message.</span></span>

<span data-ttu-id="cdac0-121">Un contrôle RichEdit envoie des codes de notification en **\_ lien** lorsqu’il reçoit les messages suivants lorsque le pointeur de la souris se trouve sur le texte qui a l’effet de **\_ lien CFE** :</span><span class="sxs-lookup"><span data-stu-id="cdac0-121">A rich edit control sends **EN\_LINK** notification codes when it receives the following messages while the mouse pointer is over text that has the **CFE\_LINK** effect:</span></span>

-   [<span data-ttu-id="cdac0-122">**\_LBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="cdac0-122">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [<span data-ttu-id="cdac0-123">**\_LBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="cdac0-123">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)
-   [<span data-ttu-id="cdac0-124">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="cdac0-124">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)
-   [<span data-ttu-id="cdac0-125">**WM \_ MOUSEMOVE**</span><span class="sxs-lookup"><span data-stu-id="cdac0-125">**WM\_MOUSEMOVE**</span></span>](/windows/desktop/inputdev/wm-mousemove)
-   [<span data-ttu-id="cdac0-126">**\_RBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="cdac0-126">**WM\_RBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [<span data-ttu-id="cdac0-127">**\_RBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="cdac0-127">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown)
-   [<span data-ttu-id="cdac0-128">**\_RBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="cdac0-128">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
-   [<span data-ttu-id="cdac0-129">**\_SETCURSOR WM**</span><span class="sxs-lookup"><span data-stu-id="cdac0-129">**WM\_SETCURSOR**</span></span>](/windows/desktop/menurc/wm-setcursor)

<span data-ttu-id="cdac0-130">L’effet de **\_ lien CFE** identifie généralement une plage de texte qui contient une URL.</span><span class="sxs-lookup"><span data-stu-id="cdac0-130">The **CFE\_LINK** effect typically identifies a range of text that contains an URL.</span></span> <span data-ttu-id="cdac0-131">Les applications peuvent gérer le \_ Code de notification en lien en modifiant le pointeur de la souris lorsqu’il se trouve sur l’URL, ou en démarrant un navigateur pour afficher l’emplacement identifié par l’URL.</span><span class="sxs-lookup"><span data-stu-id="cdac0-131">Applications can handle the EN\_LINK notification code by changing the mouse pointer when it is over the URL, or by starting a browser to view the location identified by the URL.</span></span>

<span data-ttu-id="cdac0-132">Si vous envoyez le message [**em \_ AUTOURLDETECT**](em-autourldetect.md) pour activer la détection automatique des URL, le contrôle Rich Edit définit automatiquement l’effet de **\_ lien CFE** pour le texte modifié qu’il identifie en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="cdac0-132">If you send the [**EM\_AUTOURLDETECT**](em-autourldetect.md) message to enable automatic URL detection, the rich edit control automatically sets the **CFE\_LINK** effect for modified text that it identifies as a URL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdac0-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdac0-133">Requirements</span></span>



| <span data-ttu-id="cdac0-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdac0-134">Requirement</span></span> | <span data-ttu-id="cdac0-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdac0-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cdac0-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdac0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cdac0-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdac0-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cdac0-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdac0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cdac0-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdac0-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cdac0-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdac0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdac0-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdac0-141"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdac0-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdac0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdac0-143">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="cdac0-143">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[<span data-ttu-id="cdac0-144">**\_AUTOURLDETECT em**</span><span class="sxs-lookup"><span data-stu-id="cdac0-144">**EM\_AUTOURLDETECT**</span></span>](em-autourldetect.md)
</dt> <dt>

[<span data-ttu-id="cdac0-145">**Créer un lien**</span><span class="sxs-lookup"><span data-stu-id="cdac0-145">**ENLINK**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[<span data-ttu-id="cdac0-146">**ITextRange2 :: SetURL**</span><span class="sxs-lookup"><span data-stu-id="cdac0-146">**ITextRange2::SetURL**</span></span>](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[<span data-ttu-id="cdac0-147">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="cdac0-147">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

