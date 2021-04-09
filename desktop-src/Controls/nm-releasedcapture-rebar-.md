---
title: Code de notification NM_RELEASEDCAPTURE (Rebar) (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle rebar que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 1196260f-b9ba-4a9e-80a7-e126196c3beb
keywords:
- Contrôles Windows de code de notification NM_RELEASEDCAPTURE (Rebar)
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
ms.openlocfilehash: 3c2f5367a0a5d5fac0948493ef70e4be1140013c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942197"
---
# <a name="nm_releasedcapture-rebar-notification-code"></a><span data-ttu-id="e0c92-105">\_Code de notification RELEASEDCAPTURE nm (Rebar)</span><span class="sxs-lookup"><span data-stu-id="e0c92-105">NM\_RELEASEDCAPTURE (rebar) notification code</span></span>

<span data-ttu-id="e0c92-106">Notifie la fenêtre parente d’un contrôle rebar que le contrôle libère la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="e0c92-106">Notifies a rebar control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="e0c92-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e0c92-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e0c92-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0c92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0c92-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0c92-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c92-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="e0c92-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0c92-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0c92-111">Return value</span></span>

<span data-ttu-id="e0c92-112">Le contrôle ignore la valeur de retour de ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="e0c92-112">The control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c92-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0c92-113">Requirements</span></span>



| <span data-ttu-id="e0c92-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0c92-114">Requirement</span></span> | <span data-ttu-id="e0c92-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0c92-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c92-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0c92-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e0c92-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0c92-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0c92-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0c92-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e0c92-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0c92-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0c92-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0c92-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0c92-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0c92-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





