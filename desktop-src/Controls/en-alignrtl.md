---
title: Code de notification EN_ALIGNRTL (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que la direction du paragraphe est passée de droite à gauche. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message de commande WM.
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- Contrôles Windows de code de notification EN_ALIGNRTL
topic_type:
- apiref
api_name:
- EN_ALIGNRTL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac2adaa629d00ef940f02f1ed69eb778cdc7813
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464894"
---
# <a name="en_alignrtl-notification-code"></a><span data-ttu-id="33337-105">\_Code de notification en ALIGNRTL</span><span class="sxs-lookup"><span data-stu-id="33337-105">EN\_ALIGNRTL notification code</span></span>

<span data-ttu-id="33337-106">Avertit une fenêtre parente d’un contrôle RichEdit que la direction du paragraphe est passée de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="33337-106">Notifies a rich edit control's parent window that the paragraph direction changed to right-to-left.</span></span> <span data-ttu-id="33337-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="33337-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNRTL

    WPARAM wParam
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="33337-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33337-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33337-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33337-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33337-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="33337-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="33337-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="33337-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="33337-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33337-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33337-113">Handle du contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="33337-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33337-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33337-114">Return value</span></span>

<span data-ttu-id="33337-115">Ce code de notification ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="33337-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="33337-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33337-116">Requirements</span></span>



| <span data-ttu-id="33337-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33337-117">Requirement</span></span> | <span data-ttu-id="33337-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="33337-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33337-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33337-119">Minimum supported client</span></span><br/> | <span data-ttu-id="33337-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33337-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33337-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33337-121">Minimum supported server</span></span><br/> | <span data-ttu-id="33337-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33337-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33337-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="33337-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="33337-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="33337-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33337-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33337-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="33337-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="33337-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="33337-127">**en \_ ALIGNLTR**</span><span class="sxs-lookup"><span data-stu-id="33337-127">**EN\_ALIGNLTR**</span></span>](en-alignltr.md)
</dt> <dt>

<span data-ttu-id="33337-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="33337-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="33337-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33337-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="33337-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33337-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="33337-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="33337-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

