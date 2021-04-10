---
title: LVN_ITEMACTIVATE le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’utilisateur active un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- Contrôles Windows de code de notification LVN_ITEMACTIVATE
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106666"
---
# <a name="lvn_itemactivate-notification-code"></a><span data-ttu-id="4411d-105">\_Code de notification LVN ITEMACTIVATE</span><span class="sxs-lookup"><span data-stu-id="4411d-105">LVN\_ITEMACTIVATE notification code</span></span>

<span data-ttu-id="4411d-106">Envoyé par un contrôle List-View lorsque l’utilisateur active un élément.</span><span class="sxs-lookup"><span data-stu-id="4411d-106">Sent by a list-view control when the user activates an item.</span></span> <span data-ttu-id="4411d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4411d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a><span data-ttu-id="4411d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4411d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4411d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4411d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4411d-110">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="4411d-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="4411d-111">Pointeur vers une structure [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="4411d-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains information about this notification code.</span></span>

<span data-ttu-id="4411d-112">[Version 4,70](common-control-versions.md) et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="4411d-112">[Version 4.70](common-control-versions.md) and earlier.</span></span> <span data-ttu-id="4411d-113">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="4411d-113">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4411d-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4411d-114">Return value</span></span>

<span data-ttu-id="4411d-115">L’application recevant ce code de notification doit retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="4411d-115">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4411d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4411d-116">Remarks</span></span>

<span data-ttu-id="4411d-117">Pour obtenir les éléments en cours d’activation, l’application réceptrice doit utiliser le message [**\_ GETSELECTEDCOUNT LVM**](lvm-getselectedcount.md) pour récupérer le nombre d’éléments sélectionnés, puis envoyer le [**message \_ GETNEXTITEM LVM**](lvm-getnextitem.md) avec **LVNI \_ sélectionné** jusqu’à ce que tous les éléments aient été récupérés.</span><span class="sxs-lookup"><span data-stu-id="4411d-117">To obtain the items being activated, the receiving application should use the [**LVM\_GETSELECTEDCOUNT**](lvm-getselectedcount.md) message to retrieve the number of items that are selected and then send the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message with **LVNI\_SELECTED** until all of the items have been retrieved.</span></span>

## <a name="requirements"></a><span data-ttu-id="4411d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4411d-118">Requirements</span></span>



| <span data-ttu-id="4411d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4411d-119">Requirement</span></span> | <span data-ttu-id="4411d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4411d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4411d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4411d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4411d-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4411d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4411d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4411d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4411d-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4411d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4411d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4411d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4411d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4411d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





