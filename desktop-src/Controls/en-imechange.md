---
title: Code de notification EN_IMECHANGE (RichEdit. h)
description: Avertit le parent d’un contrôle RichEdit que l’état de conversion IME a changé.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- Contrôles Windows de code de notification EN_IMECHANGE
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032893"
---
# <a name="en_imechange-notification-code"></a><span data-ttu-id="24379-104">\_Code de notification en IMECHANGE</span><span class="sxs-lookup"><span data-stu-id="24379-104">EN\_IMECHANGE notification code</span></span>

<span data-ttu-id="24379-105">Avertit le parent d’un contrôle RichEdit que l’état de conversion IME a changé.</span><span class="sxs-lookup"><span data-stu-id="24379-105">Notifies a rich edit control's parent that the IME conversion status has changed.</span></span> <span data-ttu-id="24379-106">Ce code de notification est disponible *uniquement* pour les versions en langue asiatique du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="24379-106">This notification code is available *only* for Asian-language versions of the operating system.</span></span> <span data-ttu-id="24379-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="24379-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="24379-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24379-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24379-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24379-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24379-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="24379-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="24379-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="24379-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="24379-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24379-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24379-113">Handle du contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="24379-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24379-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24379-114">Return value</span></span>

<span data-ttu-id="24379-115">Ce code de notification retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="24379-115">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="24379-116">Notes</span><span class="sxs-lookup"><span data-stu-id="24379-116">Remarks</span></span>

<span data-ttu-id="24379-117">Pour recevoir les \_ codes de notification en IMECHANGE, spécifiez [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="24379-117">To receive EN\_IMECHANGE notification codes, specify [**ENM\_IMECHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="24379-118">Ce code de notification est pris en charge uniquement dans la version asiatique de Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="24379-118">This notification code is only supported in the Asian version of Rich Edit 1.0.</span></span> <span data-ttu-id="24379-119">Elle n’est pas prise en charge dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="24379-119">It is not supported in later versions.</span></span> <span data-ttu-id="24379-120">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="24379-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="24379-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24379-121">Requirements</span></span>



| <span data-ttu-id="24379-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24379-122">Requirement</span></span> | <span data-ttu-id="24379-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="24379-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24379-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24379-124">Minimum supported client</span></span><br/> | <span data-ttu-id="24379-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24379-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24379-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24379-126">Minimum supported server</span></span><br/> | <span data-ttu-id="24379-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24379-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24379-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="24379-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="24379-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="24379-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24379-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24379-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="24379-131">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="24379-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="24379-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24379-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="24379-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24379-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="24379-134">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="24379-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

