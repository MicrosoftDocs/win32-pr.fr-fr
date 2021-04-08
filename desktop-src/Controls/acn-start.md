---
title: ACN_START le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle d’animation que le clip AVI associé a démarré. Ce code de notification est envoyé sous la forme d’un \_ message de commande WM.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- Contrôles Windows de code de notification ACN_START
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0354d8b2b41ea8690be47e70cbc577c064e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740517"
---
# <a name="acn_start-notification-code"></a><span data-ttu-id="aa533-105">ACN \_ Démarrer le code de notification</span><span class="sxs-lookup"><span data-stu-id="aa533-105">ACN\_START notification code</span></span>

<span data-ttu-id="aa533-106">Avertit la fenêtre parente d’un contrôle d’animation que le clip AVI associé a démarré.</span><span class="sxs-lookup"><span data-stu-id="aa533-106">Notifies an animation control's parent window that the associated AVI clip has started playing.</span></span> <span data-ttu-id="aa533-107">Ce code de notification est envoyé sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="aa533-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="aa533-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa533-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa533-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa533-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa533-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="aa533-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="aa533-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.</span><span class="sxs-lookup"><span data-stu-id="aa533-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="aa533-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa533-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa533-113">**HWND** qui spécifie le handle du contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="aa533-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa533-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa533-114">Requirements</span></span>



| <span data-ttu-id="aa533-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa533-115">Requirement</span></span> | <span data-ttu-id="aa533-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa533-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa533-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa533-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aa533-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa533-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa533-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa533-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aa533-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa533-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa533-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa533-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa533-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa533-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

