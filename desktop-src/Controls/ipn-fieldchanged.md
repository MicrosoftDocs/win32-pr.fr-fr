---
title: IPN_FIELDCHANGED le code de notification (commctrl. h)
description: Envoyé lorsque l’utilisateur modifie un champ dans le contrôle ou passe d’un champ à un autre. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- Contrôles Windows de code de notification IPN_FIELDCHANGED
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033107"
---
# <a name="ipn_fieldchanged-notification-code"></a><span data-ttu-id="5f1be-105">\_Code de notification IPN FIELDCHANGED</span><span class="sxs-lookup"><span data-stu-id="5f1be-105">IPN\_FIELDCHANGED notification code</span></span>

<span data-ttu-id="5f1be-106">Envoyé lorsque l’utilisateur modifie un champ dans le contrôle ou passe d’un champ à un autre.</span><span class="sxs-lookup"><span data-stu-id="5f1be-106">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="5f1be-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1be-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5f1be-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f1be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f1be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f1be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f1be-110">Pointeur vers une structure [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) qui contient des informations sur l’adresse modifiée.</span><span class="sxs-lookup"><span data-stu-id="5f1be-110">A pointer to an [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) structure that contains information about the changed address.</span></span> <span data-ttu-id="5f1be-111">Le membre **iValue** de cette structure contiendra la valeur entrée, même si elle est en dehors de la plage du champ.</span><span class="sxs-lookup"><span data-stu-id="5f1be-111">The **iValue** member of this structure will contain the entered value, even if it is out of the range of the field.</span></span> <span data-ttu-id="5f1be-112">Vous pouvez modifier ce membre en n’importe quelle valeur comprise dans la plage du champ en réponse à ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="5f1be-112">You can modify this member to any value that is within the range for the field in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f1be-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f1be-113">Return value</span></span>

<span data-ttu-id="5f1be-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5f1be-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f1be-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5f1be-115">Remarks</span></span>

<span data-ttu-id="5f1be-116">Ce code de notification n’est pas envoyé en réponse à un message [**\_ SETADDRESS IPM**](ipm-setaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="5f1be-116">This notification code is not sent in response to a [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f1be-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f1be-117">Requirements</span></span>



| <span data-ttu-id="5f1be-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f1be-118">Requirement</span></span> | <span data-ttu-id="5f1be-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f1be-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1be-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f1be-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5f1be-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f1be-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f1be-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f1be-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5f1be-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f1be-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f1be-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f1be-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f1be-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f1be-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





