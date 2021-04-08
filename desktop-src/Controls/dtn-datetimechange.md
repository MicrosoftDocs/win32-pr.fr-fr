---
title: DTN_DATETIMECHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) chaque fois qu’une modification se produit. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- Contrôles Windows de code de notification DTN_DATETIMECHANGE
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843938"
---
# <a name="dtn_datetimechange-notification-code"></a><span data-ttu-id="8f542-105">\_Code de notification DTN DATETIMECHANGE</span><span class="sxs-lookup"><span data-stu-id="8f542-105">DTN\_DATETIMECHANGE notification code</span></span>

<span data-ttu-id="8f542-106">Envoyé par un contrôle de sélecteur de date et heure (PAO) chaque fois qu’une modification se produit.</span><span class="sxs-lookup"><span data-stu-id="8f542-106">Sent by a date and time picker (DTP) control whenever a change occurs.</span></span> <span data-ttu-id="8f542-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8f542-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8f542-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f542-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f542-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f542-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f542-110">Pointeur vers une structure [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) contenant des informations sur la modification qui a eu lieu dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8f542-110">A pointer to an [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) structure containing information about the change that took place in the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f542-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f542-111">Return value</span></span>

<span data-ttu-id="8f542-112">Le propriétaire du contrôle doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="8f542-112">The owner of the control must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f542-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f542-113">Requirements</span></span>



| <span data-ttu-id="8f542-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f542-114">Requirement</span></span> | <span data-ttu-id="8f542-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f542-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f542-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f542-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8f542-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f542-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f542-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f542-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8f542-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f542-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f542-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f542-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f542-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f542-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





