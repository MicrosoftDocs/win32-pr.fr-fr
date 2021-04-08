---
title: Code de notification NM_RELEASEDCAPTURE (téléavertisseur) (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle de pagineur que le contrôle a relâché la capture de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5ce9c38a-5d37-4ac7-8510-30bc59d85cca
keywords:
- Contrôles Windows de code de notification NM_RELEASEDCAPTURE (téléavertisseur)
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
ms.openlocfilehash: 0fb1d258d9baa0952e1707e36884a492ff65f99b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843702"
---
# <a name="nm_releasedcapture-pager-notification-code"></a><span data-ttu-id="80284-105">\_Code de notification RELEASEDCAPTURE nm (téléavertisseur)</span><span class="sxs-lookup"><span data-stu-id="80284-105">NM\_RELEASEDCAPTURE (pager) notification code</span></span>

<span data-ttu-id="80284-106">Notifie la fenêtre parente d’un contrôle de pagineur que le contrôle a relâché la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="80284-106">Notifies a pager control's parent window that the control has released the mouse capture.</span></span> <span data-ttu-id="80284-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="80284-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="80284-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80284-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80284-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80284-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80284-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="80284-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80284-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80284-111">Return value</span></span>

<span data-ttu-id="80284-112">La valeur de retour est ignorée par le contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="80284-112">The return value is ignored by the pager control.</span></span>

## <a name="requirements"></a><span data-ttu-id="80284-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80284-113">Requirements</span></span>



| <span data-ttu-id="80284-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80284-114">Requirement</span></span> | <span data-ttu-id="80284-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="80284-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80284-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80284-116">Minimum supported client</span></span><br/> | <span data-ttu-id="80284-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80284-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80284-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80284-118">Minimum supported server</span></span><br/> | <span data-ttu-id="80284-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80284-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80284-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="80284-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="80284-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="80284-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





