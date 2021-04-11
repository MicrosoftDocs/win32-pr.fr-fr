---
title: CBEN_DRAGBEGIN le code de notification (commctrl. h)
description: Envoyé lorsque l’utilisateur commence à faire glisser l’image de l’élément affiché dans la partie modifiable du contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- Contrôles Windows de code de notification CBEN_DRAGBEGIN
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105757"
---
# <a name="cben_dragbegin-notification-code"></a><span data-ttu-id="038db-105">\_Code de notification CBEN DRAGBEGIN</span><span class="sxs-lookup"><span data-stu-id="038db-105">CBEN\_DRAGBEGIN notification code</span></span>

<span data-ttu-id="038db-106">Envoyé lorsque l’utilisateur commence à faire glisser l’image de l’élément affiché dans la partie modifiable du contrôle.</span><span class="sxs-lookup"><span data-stu-id="038db-106">Sent when the user begins dragging the image of the item displayed in the edit portion of the control.</span></span> <span data-ttu-id="038db-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="038db-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="038db-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="038db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="038db-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="038db-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="038db-110">Pointeur vers une structure [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="038db-110">A pointer to a [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="038db-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="038db-111">Return value</span></span>

<span data-ttu-id="038db-112">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="038db-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="038db-113">Notes</span><span class="sxs-lookup"><span data-stu-id="038db-113">Remarks</span></span>

<span data-ttu-id="038db-114">Si l’application réceptrice implémente la fonctionnalité de glisser-déplacer à partir du contrôle, l’application commence l’opération de glisser-déplacer en réponse à ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="038db-114">If the receiving application implements drag-and-drop functionality from the control, the application will begin the drag-and-drop operation in response to this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="038db-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="038db-115">Requirements</span></span>



| <span data-ttu-id="038db-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="038db-116">Requirement</span></span> | <span data-ttu-id="038db-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="038db-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="038db-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="038db-118">Minimum supported client</span></span><br/> | <span data-ttu-id="038db-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="038db-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="038db-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="038db-120">Minimum supported server</span></span><br/> | <span data-ttu-id="038db-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="038db-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="038db-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="038db-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="038db-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="038db-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="038db-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="038db-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="038db-125">**CBEN \_ DRAGBEGINW** (Unicode) et **CBEN \_ DRAGBEGINA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="038db-125">**CBEN\_DRAGBEGINW** (Unicode) and **CBEN\_DRAGBEGINA** (ANSI)</span></span><br/>             |



 

 





