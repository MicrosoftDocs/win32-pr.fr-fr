---
title: Code de notification EN_CLIPFORMAT (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit qu’un collage a été effectué avec un format de presse-papiers particulier. Un contrôle RichEdit sans fenêtre envoie cette notification à l’aide de la méthode ITextHost TxNotify.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- Contrôles Windows de code de notification EN_CLIPFORMAT
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941954"
---
# <a name="en_clipformat-notification-code"></a><span data-ttu-id="d80cc-105">\_Code de notification en CLIPFORMAT</span><span class="sxs-lookup"><span data-stu-id="d80cc-105">EN\_CLIPFORMAT notification code</span></span>

<span data-ttu-id="d80cc-106">Avertit une fenêtre parente d’un contrôle RichEdit qu’un collage a été effectué avec un format de presse-papiers particulier.</span><span class="sxs-lookup"><span data-stu-id="d80cc-106">Notifies a rich edit control's parent window that a paste occurred with a particular clipboard format.</span></span> <span data-ttu-id="d80cc-107">Un contrôle RichEdit sans fenêtre envoie cette notification à l’aide de la méthode [**ITextHost :: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .</span><span class="sxs-lookup"><span data-stu-id="d80cc-107">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span>


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d80cc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d80cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d80cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d80cc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d80cc-110">ID de fenêtre récupéré en appelant la fonction [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) avec la \_ valeur d’ID GWL.</span><span class="sxs-lookup"><span data-stu-id="d80cc-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="d80cc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d80cc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d80cc-112">Pointeur vers une structure [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) qui contient des informations sur le format du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="d80cc-112">A pointer to a [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) structure that contains information about the clipboard format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d80cc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d80cc-113">Return value</span></span>

<span data-ttu-id="d80cc-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="d80cc-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="d80cc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d80cc-115">Remarks</span></span>

<span data-ttu-id="d80cc-116">Pour recevoir les \_ codes de notification en CLIPFORMAT, spécifiez [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="d80cc-116">To receive EN\_CLIPFORMAT notification codes, specify [**ENM\_CLIPFORMAT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d80cc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d80cc-117">Requirements</span></span>



| <span data-ttu-id="d80cc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d80cc-118">Requirement</span></span> | <span data-ttu-id="d80cc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d80cc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d80cc-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d80cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d80cc-121">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d80cc-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d80cc-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d80cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d80cc-123">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d80cc-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d80cc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d80cc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d80cc-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d80cc-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d80cc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d80cc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d80cc-127">**CLIPBOARDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d80cc-127">**CLIPBOARDFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

