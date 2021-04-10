---
title: Code de notification NM_RELEASEDCAPTURE (TrackBar) (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle TrackBar que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 1e3e4f67-672d-4e3e-84f4-b3fa6221d118
keywords:
- Contrôles Windows du code de notification NM_RELEASEDCAPTURE (TrackBar)
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
ms.openlocfilehash: 684f58fb5328cfe0d25fc73ce7c1a2d9a189d86f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105094"
---
# <a name="nm_releasedcapture-trackbar-notification-code"></a><span data-ttu-id="5910d-105">\_Code de notification RELEASEDCAPTURE nm (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="5910d-105">NM\_RELEASEDCAPTURE (trackbar) notification code</span></span>

<span data-ttu-id="5910d-106">Avertit la fenêtre parente d’un contrôle TrackBar que le contrôle libère la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="5910d-106">Notifies a trackbar control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="5910d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5910d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5910d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5910d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5910d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5910d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5910d-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="5910d-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5910d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5910d-111">Return value</span></span>

<span data-ttu-id="5910d-112">Le contrôle ignore la valeur de retour de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="5910d-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5910d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5910d-113">Requirements</span></span>



| <span data-ttu-id="5910d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5910d-114">Requirement</span></span> | <span data-ttu-id="5910d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5910d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5910d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5910d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5910d-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5910d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5910d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5910d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5910d-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5910d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5910d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5910d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5910d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5910d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





