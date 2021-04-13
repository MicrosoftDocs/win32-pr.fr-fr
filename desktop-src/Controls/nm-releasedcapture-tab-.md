---
title: NM_RELEASEDCAPTURE (onglet) Code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 17f87666-692c-4c2f-9ef5-6d2593e0de97
keywords:
- Contrôles Windows de code de notification NM_RELEASEDCAPTURE (onglet)
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
ms.openlocfilehash: ad9c9049b63afb18413aea9fa77b7947e97e93b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465866"
---
# <a name="nm_releasedcapture-tab-notification-code"></a><span data-ttu-id="4f7f0-105">\_Code de notification RELEASEDCAPTURE nm (onglet)</span><span class="sxs-lookup"><span data-stu-id="4f7f0-105">NM\_RELEASEDCAPTURE (tab) notification code</span></span>

<span data-ttu-id="4f7f0-106">Avertit une fenêtre parente d’un contrôle onglet que le contrôle libère la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-106">Notifies a tab control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="4f7f0-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4f7f0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4f7f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f7f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f7f0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f7f0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f7f0-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f7f0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f7f0-111">Return value</span></span>

<span data-ttu-id="4f7f0-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f7f0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f7f0-113">Requirements</span></span>



| <span data-ttu-id="4f7f0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f7f0-114">Requirement</span></span> | <span data-ttu-id="4f7f0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f7f0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f7f0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f7f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4f7f0-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f7f0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f7f0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f7f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4f7f0-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f7f0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f7f0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f7f0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f7f0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f7f0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





