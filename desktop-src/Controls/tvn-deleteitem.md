---
title: TVN_DELETEITEM le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle Tree-View qu’un élément est en cours de suppression. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- Contrôles Windows de code de notification TVN_DELETEITEM
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465462"
---
# <a name="tvn_deleteitem-notification-code"></a><span data-ttu-id="a75b8-105">\_Code de notification TVN DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="a75b8-105">TVN\_DELETEITEM notification code</span></span>

<span data-ttu-id="a75b8-106">Avertit la fenêtre parente d’un contrôle Tree-View qu’un élément est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="a75b8-106">Notifies a tree-view control's parent window that an item is being deleted.</span></span> <span data-ttu-id="a75b8-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a75b8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="a75b8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a75b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a75b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a75b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a75b8-110">Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="a75b8-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="a75b8-111">Le membre **itemOld** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dont les membres **hitem** et **lParam** contiennent des informations valides sur l’élément en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="a75b8-111">The **itemOld** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **hItem** and **lParam** members contain valid information about the item being deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a75b8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a75b8-112">Return value</span></span>

<span data-ttu-id="a75b8-113">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="a75b8-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a75b8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a75b8-114">Remarks</span></span>

<span data-ttu-id="a75b8-115">Si le membre **lParam** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) pointe vers la mémoire allouée par votre application, vous pouvez le libérer lorsque vous recevez le code de \_ notification TVN DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="a75b8-115">If the **lParam** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure points to memory allocated by your application, you can free it when you receive the TVN\_DELETEITEM notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75b8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a75b8-116">Requirements</span></span>



| <span data-ttu-id="a75b8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a75b8-117">Requirement</span></span> | <span data-ttu-id="a75b8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a75b8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a75b8-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a75b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a75b8-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a75b8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a75b8-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a75b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a75b8-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a75b8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a75b8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a75b8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a75b8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a75b8-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a75b8-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a75b8-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a75b8-126">**TVN \_ DELETEITEMW** (Unicode) et **TVN \_ DELETEITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a75b8-126">**TVN\_DELETEITEMW** (Unicode) and **TVN\_DELETEITEMA** (ANSI)</span></span><br/>             |



 

 





