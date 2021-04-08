---
title: NM_FONTCHANGED le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View lorsque le contrôle a modifié une police. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- Contrôles Windows de code de notification NM_FONTCHANGED
topic_type:
- apiref
api_name:
- NM_FONTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75003021f83276c953b5aa2cf0b812d20d60857b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843078"
---
# <a name="nm_fontchanged-notification-code"></a><span data-ttu-id="52541-105">\_Code de notification FONTCHANGED nm</span><span class="sxs-lookup"><span data-stu-id="52541-105">NM\_FONTCHANGED notification code</span></span>

<span data-ttu-id="52541-106">Envoyé par un contrôle List-View lorsque le contrôle a modifié une police.</span><span class="sxs-lookup"><span data-stu-id="52541-106">Sent by a list-view control when the control has changed a font.</span></span> <span data-ttu-id="52541-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="52541-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_FONTCHANGED
        
    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="52541-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52541-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52541-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52541-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52541-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="52541-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52541-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52541-111">Return value</span></span>

<span data-ttu-id="52541-112">La valeur de retour est ignorée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="52541-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="52541-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52541-113">Requirements</span></span>



| <span data-ttu-id="52541-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52541-114">Requirement</span></span> | <span data-ttu-id="52541-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="52541-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52541-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52541-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52541-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52541-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52541-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52541-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52541-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52541-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52541-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="52541-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="52541-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52541-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





