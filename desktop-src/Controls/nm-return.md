---
title: NM_RETURN le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle a le focus d’entrée et que l’utilisateur a appuyé sur la touche entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2c4839bc-6b23-469b-978f-cdf5f7bc0549
keywords:
- Contrôles Windows de code de notification NM_RETURN
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c6cebd089873df5471c9b25710efafaab4d246f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509026"
---
# <a name="nm_return-notification-code"></a><span data-ttu-id="22258-105">\_Code de notification de retour nm</span><span class="sxs-lookup"><span data-stu-id="22258-105">NM\_RETURN notification code</span></span>

<span data-ttu-id="22258-106">Avertit la fenêtre parente d’un contrôle que le contrôle a le focus d’entrée et que l’utilisateur a appuyé sur la touche entrée.</span><span class="sxs-lookup"><span data-stu-id="22258-106">Notifies a control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="22258-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="22258-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="22258-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22258-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22258-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22258-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22258-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="22258-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22258-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22258-111">Return value</span></span>

<span data-ttu-id="22258-112">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="22258-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="22258-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22258-113">Requirements</span></span>



| <span data-ttu-id="22258-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22258-114">Requirement</span></span> | <span data-ttu-id="22258-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="22258-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22258-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22258-116">Minimum supported client</span></span><br/> | <span data-ttu-id="22258-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22258-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22258-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22258-118">Minimum supported server</span></span><br/> | <span data-ttu-id="22258-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22258-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22258-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="22258-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="22258-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22258-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





