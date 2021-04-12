---
title: Code de notification EN_ALIGNLTR (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que la direction du paragraphe est passée de gauche à droite. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message de commande WM.
ms.assetid: 754ac2b5-bcec-487b-a1ab-b653f673830a
keywords:
- Contrôles Windows de code de notification EN_ALIGNLTR
topic_type:
- apiref
api_name:
- EN_ALIGNLTR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55c20a9ae4efb3ba5758ed0740b20b8b57f3877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032698"
---
# <a name="en_alignltr-notification-code"></a><span data-ttu-id="09ca8-105">\_Code de notification en ALIGNLTR</span><span class="sxs-lookup"><span data-stu-id="09ca8-105">EN\_ALIGNLTR notification code</span></span>

<span data-ttu-id="09ca8-106">Avertit une fenêtre parente d’un contrôle RichEdit que la direction du paragraphe est passée de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="09ca8-106">Notifies a rich edit control's parent window that the paragraph direction has changed to left-to-right.</span></span> <span data-ttu-id="09ca8-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="09ca8-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNLTR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="09ca8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09ca8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09ca8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09ca8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09ca8-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="09ca8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="09ca8-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="09ca8-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="09ca8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09ca8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09ca8-113">Handle du contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="09ca8-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09ca8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09ca8-114">Return value</span></span>

<span data-ttu-id="09ca8-115">Ce code de notification ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="09ca8-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="09ca8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09ca8-116">Requirements</span></span>



| <span data-ttu-id="09ca8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09ca8-117">Requirement</span></span> | <span data-ttu-id="09ca8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="09ca8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09ca8-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ca8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09ca8-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09ca8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09ca8-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ca8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09ca8-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09ca8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09ca8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="09ca8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="09ca8-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="09ca8-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09ca8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09ca8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="09ca8-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="09ca8-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="09ca8-127">**en \_ ALIGNRTL**</span><span class="sxs-lookup"><span data-stu-id="09ca8-127">**EN\_ALIGNRTL**</span></span>](en-alignrtl.md)
</dt> <dt>

<span data-ttu-id="09ca8-128">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="09ca8-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="09ca8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09ca8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="09ca8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09ca8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="09ca8-131">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="09ca8-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

