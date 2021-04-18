---
title: RBN_MINMAX le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar avant d’agrandir ou de réduire une bande. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- Contrôles Windows de code de notification RBN_MINMAX
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512399"
---
# <a name="rbn_minmax-notification-code"></a><span data-ttu-id="0ab73-105">\_Code de notification RBN MinMax</span><span class="sxs-lookup"><span data-stu-id="0ab73-105">RBN\_MINMAX notification code</span></span>

<span data-ttu-id="0ab73-106">Envoyé par un contrôle rebar avant d’agrandir ou de réduire une bande.</span><span class="sxs-lookup"><span data-stu-id="0ab73-106">Sent by a rebar control prior to maximizing or minimizing a band.</span></span> <span data-ttu-id="0ab73-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0ab73-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_MINMAX
```



## <a name="parameters"></a><span data-ttu-id="0ab73-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ab73-108">Parameters</span></span>

<span data-ttu-id="0ab73-109">Ce code de notification n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0ab73-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ab73-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ab73-110">Return value</span></span>

<span data-ttu-id="0ab73-111">Retourne une valeur différente de zéro pour empêcher l’opération de se produire, zéro pour l’autoriser à continuer.</span><span class="sxs-lookup"><span data-stu-id="0ab73-111">Return a nonzero value to prevent the operation from taking place, zero to allow it to continue.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ab73-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ab73-112">Requirements</span></span>



| <span data-ttu-id="0ab73-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ab73-113">Requirement</span></span> | <span data-ttu-id="0ab73-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ab73-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab73-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ab73-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0ab73-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ab73-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ab73-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ab73-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0ab73-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ab73-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ab73-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ab73-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ab73-120"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ab73-120"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





