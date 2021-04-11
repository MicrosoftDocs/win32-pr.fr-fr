---
title: NM_SETFOCUS le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle a reçu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 4810afd3-c8a8-4813-b44a-eba3d409d4f1
keywords:
- Contrôles Windows de code de notification NM_SETFOCUS
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd3d50596f39359fe2aeeeb4fe61b8bc73603efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942479"
---
# <a name="nm_setfocus-notification-code"></a><span data-ttu-id="ea43e-105">NM \_ Code de notification SetFocus</span><span class="sxs-lookup"><span data-stu-id="ea43e-105">NM\_SETFOCUS notification code</span></span>

<span data-ttu-id="ea43e-106">Avertit la fenêtre parente d’un contrôle que le contrôle a reçu le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ea43e-106">Notifies a control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="ea43e-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ea43e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ea43e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea43e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea43e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea43e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea43e-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="ea43e-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea43e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea43e-111">Return value</span></span>

<span data-ttu-id="ea43e-112">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ea43e-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea43e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea43e-113">Requirements</span></span>



| <span data-ttu-id="ea43e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea43e-114">Requirement</span></span> | <span data-ttu-id="ea43e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea43e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea43e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea43e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ea43e-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea43e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea43e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea43e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ea43e-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea43e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea43e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea43e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea43e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea43e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





