---
title: Code de notification EN_SAVECLIPBOARD (RichEdit. h)
description: Avertit la fenêtre parente du contrôle RichEdit que le contrôle est en fermeture et que le presse-papiers contient des informations. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- Contrôles Windows de code de notification EN_SAVECLIPBOARD
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843437"
---
# <a name="en_saveclipboard-notification-code"></a><span data-ttu-id="bbf29-105">\_Code de notification en SAVECLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="bbf29-105">EN\_SAVECLIPBOARD notification code</span></span>

<span data-ttu-id="bbf29-106">Avertit la fenêtre parente du contrôle RichEdit que le contrôle est en fermeture et que le presse-papiers contient des informations.</span><span class="sxs-lookup"><span data-stu-id="bbf29-106">Notifies the rich edit control's parent window that the control is closing and the clipboard contains information.</span></span> <span data-ttu-id="bbf29-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf29-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bbf29-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbf29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbf29-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbf29-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf29-110">Structure [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) qui contient des informations sur les informations du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="bbf29-110">An [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) structure that contains information about clipboard information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbf29-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bbf29-111">Return value</span></span>

<span data-ttu-id="bbf29-112">Retourne zéro si le presse-papiers doit être mis à la disposition d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="bbf29-112">Return zero if the clipboard should be made available to other applications.</span></span>

<span data-ttu-id="bbf29-113">Retourne une valeur différente de zéro si le presse-papiers ne doit pas être enregistré.</span><span class="sxs-lookup"><span data-stu-id="bbf29-113">Return a nonzero value if the clipboard should not be saved.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf29-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bbf29-114">Remarks</span></span>

<span data-ttu-id="bbf29-115">La fenêtre parente reçoit toujours un [**message \_ de notification WM**](wm-notify.md) pour cet événement, elle ne nécessite pas de masque de notification envoyé avec [**em \_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="bbf29-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf29-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbf29-116">Requirements</span></span>



| <span data-ttu-id="bbf29-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbf29-117">Requirement</span></span> | <span data-ttu-id="bbf29-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbf29-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf29-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbf29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf29-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbf29-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbf29-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbf29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf29-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbf29-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbf29-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bbf29-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbf29-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbf29-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf29-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbf29-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="bbf29-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="bbf29-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bbf29-127">**ENSAVECLIPBOARD**</span><span class="sxs-lookup"><span data-stu-id="bbf29-127">**ENSAVECLIPBOARD**</span></span>](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





