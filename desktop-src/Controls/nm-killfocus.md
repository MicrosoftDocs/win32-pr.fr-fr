---
title: NM_KILLFOCUS le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle a perdu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: d7538697-8b4c-4bbd-8b06-02cbc8069a22
keywords:
- Contrôles Windows de code de notification NM_KILLFOCUS
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 873af3315dd58a12a61249ca59a317ca5af4b105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102876"
---
# <a name="nm_killfocus-notification-code"></a><span data-ttu-id="ce51a-105">\_Code de notification KILLFOCUS nm</span><span class="sxs-lookup"><span data-stu-id="ce51a-105">NM\_KILLFOCUS notification code</span></span>

<span data-ttu-id="ce51a-106">Avertit la fenêtre parente d’un contrôle que le contrôle a perdu le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ce51a-106">Notifies a control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="ce51a-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ce51a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ce51a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce51a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce51a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce51a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce51a-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="ce51a-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce51a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce51a-111">Return value</span></span>

<span data-ttu-id="ce51a-112">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ce51a-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce51a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce51a-113">Requirements</span></span>



| <span data-ttu-id="ce51a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce51a-114">Requirement</span></span> | <span data-ttu-id="ce51a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce51a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce51a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce51a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce51a-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce51a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce51a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce51a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce51a-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce51a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce51a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce51a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce51a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce51a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





