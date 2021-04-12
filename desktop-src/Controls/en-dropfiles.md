---
title: Code de notification EN_DROPFILES (RichEdit. h)
description: Avertit une fenêtre parente du contrôle RichEdit que l’utilisateur tente de déposer des fichiers dans le contrôle. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify lorsqu’il reçoit le \_ message WM DROPFILES.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- Contrôles Windows de code de notification EN_DROPFILES
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464426"
---
# <a name="en_dropfiles-notification-code"></a><span data-ttu-id="14c6a-105">\_Code de notification en DROPFILES</span><span class="sxs-lookup"><span data-stu-id="14c6a-105">EN\_DROPFILES notification code</span></span>

<span data-ttu-id="14c6a-106">Avertit une fenêtre parente du contrôle RichEdit que l’utilisateur tente de déposer des fichiers dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="14c6a-106">Notifies a rich edit control parent window that the user is attempting to drop files into the control.</span></span> <span data-ttu-id="14c6a-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) lorsqu’il reçoit le message [**WM \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles) .</span><span class="sxs-lookup"><span data-stu-id="14c6a-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message when it receives the [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) message.</span></span>


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="14c6a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14c6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c6a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14c6a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14c6a-110">Structure [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) qui reçoit les informations sur les fichiers supprimés.</span><span class="sxs-lookup"><span data-stu-id="14c6a-110">An [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure that receives dropped files information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c6a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14c6a-111">Return value</span></span>

<span data-ttu-id="14c6a-112">Retourne une valeur différente de zéro pour permettre l’opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="14c6a-112">Return a nonzero value to allow the drop operation.</span></span>

<span data-ttu-id="14c6a-113">Retournez zéro pour ignorer l’opération de suppression.</span><span class="sxs-lookup"><span data-stu-id="14c6a-113">Return zero to ignore the drop operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="14c6a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="14c6a-114">Remarks</span></span>

<span data-ttu-id="14c6a-115">Pour qu’un contrôle RichEdit reçoive les messages [**WM \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles) , la fenêtre parente doit inscrire le contrôle en tant que cible de déplacement à l’aide de la fonction [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) .</span><span class="sxs-lookup"><span data-stu-id="14c6a-115">For a rich edit control to receive [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) messages, the parent window must register the control as a drop target by using the [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) function.</span></span> <span data-ttu-id="14c6a-116">Le contrôle ne s’inscrit pas lui-même.</span><span class="sxs-lookup"><span data-stu-id="14c6a-116">The control does not register itself.</span></span>

<span data-ttu-id="14c6a-117">Pour recevoir les \_ codes de notification en DROPFILES, spécifiez [**ENM \_ DROPFILES**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="14c6a-117">To receive EN\_DROPFILES notification codes, specify [**ENM\_DROPFILES**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c6a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14c6a-118">Requirements</span></span>



| <span data-ttu-id="14c6a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14c6a-119">Requirement</span></span> | <span data-ttu-id="14c6a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="14c6a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14c6a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14c6a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14c6a-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14c6a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14c6a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14c6a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14c6a-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14c6a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14c6a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="14c6a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="14c6a-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="14c6a-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c6a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14c6a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="14c6a-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="14c6a-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="14c6a-129">**ENDROPFILES**</span><span class="sxs-lookup"><span data-stu-id="14c6a-129">**ENDROPFILES**</span></span>](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

