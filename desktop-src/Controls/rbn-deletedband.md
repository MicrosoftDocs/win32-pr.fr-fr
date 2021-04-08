---
title: RBN_DELETEDBAND le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar après la suppression d’une bande. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- Contrôles Windows de code de notification RBN_DELETEDBAND
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af4e107ccb1a42b82335255f48d0328e03019a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843917"
---
# <a name="rbn_deletedband-notification-code"></a><span data-ttu-id="aefd7-105">\_Code de notification RBN DELETEDBAND</span><span class="sxs-lookup"><span data-stu-id="aefd7-105">RBN\_DELETEDBAND notification code</span></span>

<span data-ttu-id="aefd7-106">Envoyé par un contrôle rebar après la suppression d’une bande.</span><span class="sxs-lookup"><span data-stu-id="aefd7-106">Sent by a rebar control after a band has been deleted.</span></span> <span data-ttu-id="aefd7-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="aefd7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="aefd7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aefd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aefd7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aefd7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aefd7-110">Pointeur vers une structure [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="aefd7-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aefd7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aefd7-111">Return value</span></span>

<span data-ttu-id="aefd7-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="aefd7-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="aefd7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aefd7-113">Requirements</span></span>



| <span data-ttu-id="aefd7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aefd7-114">Requirement</span></span> | <span data-ttu-id="aefd7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="aefd7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aefd7-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aefd7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aefd7-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aefd7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aefd7-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aefd7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aefd7-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aefd7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aefd7-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="aefd7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aefd7-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aefd7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





