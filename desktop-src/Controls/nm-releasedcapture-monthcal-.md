---
title: NM_RELEASEDCAPTURE (calendrier monthcal) Code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle calendrier monthcal que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: c05d3331-26f3-41f4-8032-36ed38d47917
keywords:
- Contrôles Windows de code de notification NM_RELEASEDCAPTURE (calendrier monthcal)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b9c743a076c8046aa57ba4306145248ed00f0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739917"
---
# <a name="nm_releasedcapture-monthcal-notification-code"></a><span data-ttu-id="b8b99-105">\_Code de notification RELEASEDCAPTURE nm (calendrier monthcal)</span><span class="sxs-lookup"><span data-stu-id="b8b99-105">NM\_RELEASEDCAPTURE (monthcal) notification code</span></span>

<span data-ttu-id="b8b99-106">Avertit la fenêtre parente d’un contrôle calendrier monthcal que le contrôle libère la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="b8b99-106">Notifies a monthcal control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="b8b99-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b8b99-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b8b99-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8b99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b99-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8b99-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8b99-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="b8b99-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8b99-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8b99-111">Return value</span></span>

<span data-ttu-id="b8b99-112">Le contrôle ignore la valeur de retour de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="b8b99-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b99-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8b99-113">Requirements</span></span>



| <span data-ttu-id="b8b99-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8b99-114">Requirement</span></span> | <span data-ttu-id="b8b99-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8b99-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b99-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8b99-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b99-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8b99-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8b99-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8b99-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b99-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8b99-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8b99-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8b99-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8b99-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8b99-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





