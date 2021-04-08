---
title: EN_ALIGN_RTL_EC le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur a modifié la direction du contrôle d’édition de droite à gauche. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un \_ message de commande WM.
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- Contrôles Windows de code de notification EN_ALIGN_RTL_EC
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca94073b86ea44b192360e593f4b76d4227cf82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843358"
---
# <a name="en_align_rtl_ec-notification-code"></a><span data-ttu-id="418a7-105">En \_ alignant le \_ \_ Code de notification EC RTL</span><span class="sxs-lookup"><span data-stu-id="418a7-105">EN\_ALIGN\_RTL\_EC notification code</span></span>

<span data-ttu-id="418a7-106">Envoyé lorsque l’utilisateur a modifié la direction du contrôle d’édition de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="418a7-106">Sent when the user has changed the edit control direction to right-to-left.</span></span> <span data-ttu-id="418a7-107">La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="418a7-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="418a7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="418a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="418a7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="418a7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="418a7-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="418a7-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="418a7-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="418a7-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="418a7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="418a7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="418a7-113">Handle du contrôle d’édition qui envoie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="418a7-113">A handle to the edit control sending the notification code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="418a7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="418a7-114">Remarks</span></span>

<span data-ttu-id="418a7-115">Si une langue bidirectionnelle est installée sur votre système, par exemple en arabe ou en Hébreu, vous pouvez modifier la direction du contrôle d’édition à l’aide de la combinaison de touches CTRL + LSHIFT (de gauche à droite) et CTRL + RSHIFT (de droite à gauche).</span><span class="sxs-lookup"><span data-stu-id="418a7-115">If there is a bidirectional language installed on your system, for example, Arabic or Hebrew, you can change the edit control direction using CTRL+LSHIFT (for left to right) and CTRL+RSHIFT (for right to left).</span></span>

<span data-ttu-id="418a7-116">**Modification riche :** Ce code de notification n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="418a7-116">**Rich Edit:** This notification code is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="418a7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="418a7-117">Requirements</span></span>



| <span data-ttu-id="418a7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="418a7-118">Requirement</span></span> | <span data-ttu-id="418a7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="418a7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="418a7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="418a7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="418a7-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="418a7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="418a7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="418a7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="418a7-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="418a7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="418a7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="418a7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="418a7-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="418a7-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="418a7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="418a7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="418a7-127">**WM, \_ commande**</span><span class="sxs-lookup"><span data-stu-id="418a7-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

