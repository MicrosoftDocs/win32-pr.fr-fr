---
title: RBN_DELETINGBAND le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsqu’une bande va être supprimée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 92840cb1-375e-4c37-bde4-7ba02a1ff4f1
keywords:
- Contrôles Windows de code de notification RBN_DELETINGBAND
topic_type:
- apiref
api_name:
- RBN_DELETINGBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf810fd8800d7774a0dbf9a65cdf08c2d53d92ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942455"
---
# <a name="rbn_deletingband-notification-code"></a><span data-ttu-id="39075-105">\_Code de notification RBN DELETINGBAND</span><span class="sxs-lookup"><span data-stu-id="39075-105">RBN\_DELETINGBAND notification code</span></span>

<span data-ttu-id="39075-106">Envoyé par un contrôle rebar lorsqu’une bande va être supprimée.</span><span class="sxs-lookup"><span data-stu-id="39075-106">Sent by a rebar control when a band is about to be deleted.</span></span> <span data-ttu-id="39075-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="39075-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETINGBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="39075-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39075-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39075-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39075-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39075-110">Pointeur vers une structure [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="39075-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39075-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39075-111">Return value</span></span>

<span data-ttu-id="39075-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="39075-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="39075-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39075-113">Requirements</span></span>



| <span data-ttu-id="39075-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39075-114">Requirement</span></span> | <span data-ttu-id="39075-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="39075-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39075-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39075-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39075-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39075-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39075-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39075-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39075-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39075-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39075-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="39075-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39075-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="39075-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





