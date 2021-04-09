---
description: Envoyé à toutes les fenêtres une fois que l’utilisateur s’est connecté ou désactivé. Lorsque l’utilisateur ouvre ou ferme une session, le système met à jour les paramètres spécifiques à l’utilisateur. Le système envoie ce message immédiatement après la mise à jour des paramètres.
title: Message WM_USERCHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952904"
---
# <a name="wm_userchanged-message"></a><span data-ttu-id="2de01-105">\_Message WM USERCHANGED</span><span class="sxs-lookup"><span data-stu-id="2de01-105">WM\_USERCHANGED message</span></span>

<span data-ttu-id="2de01-106">Envoyé à toutes les fenêtres une fois que l’utilisateur s’est connecté ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="2de01-106">Sent to all windows after the user has logged on or off.</span></span> <span data-ttu-id="2de01-107">Lorsque l’utilisateur ouvre ou ferme une session, le système met à jour les paramètres spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2de01-107">When the user logs on or off, the system updates the user-specific settings.</span></span> <span data-ttu-id="2de01-108">Le système envoie ce message immédiatement après la mise à jour des paramètres.</span><span class="sxs-lookup"><span data-stu-id="2de01-108">The system sends this message immediately after updating the settings.</span></span>

<span data-ttu-id="2de01-109">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2de01-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="2de01-110">Ce message n’est pas pris en charge par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2de01-110">This message is not supported as of Windows Vista.</span></span>

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a><span data-ttu-id="2de01-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2de01-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2de01-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2de01-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2de01-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="2de01-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2de01-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2de01-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2de01-115">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="2de01-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2de01-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2de01-116">Return value</span></span>

<span data-ttu-id="2de01-117">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2de01-117">Type: **LRESULT**</span></span>

<span data-ttu-id="2de01-118">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="2de01-118">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2de01-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2de01-119">Requirements</span></span>



| <span data-ttu-id="2de01-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2de01-120">Requirement</span></span> | <span data-ttu-id="2de01-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2de01-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de01-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2de01-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2de01-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2de01-123">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2de01-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2de01-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2de01-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2de01-125">None supported</span></span><br/>                                                                                |
| <span data-ttu-id="2de01-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2de01-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2de01-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2de01-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de01-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2de01-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de01-129">Vue d’ensemble de Windows</span><span class="sxs-lookup"><span data-stu-id="2de01-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
