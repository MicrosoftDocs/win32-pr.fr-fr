---
title: LVN_DELETEALLITEMS le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View que tous les éléments du contrôle sont sur le côté d’être supprimés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- Contrôles Windows de code de notification LVN_DELETEALLITEMS
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942924"
---
# <a name="lvn_deleteallitems-notification-code"></a><span data-ttu-id="67220-105">\_Code de notification LVN DELETEALLITEMS</span><span class="sxs-lookup"><span data-stu-id="67220-105">LVN\_DELETEALLITEMS notification code</span></span>

<span data-ttu-id="67220-106">Avertit la fenêtre parente d’un contrôle List-View que tous les éléments du contrôle sont sur le côté d’être supprimés.</span><span class="sxs-lookup"><span data-stu-id="67220-106">Notifies a list-view control's parent window that all items in the control are about to be deleted.</span></span> <span data-ttu-id="67220-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="67220-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="67220-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67220-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67220-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67220-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67220-110">Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="67220-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="67220-111">Le membre **iItem** a la valeur-1, et les autres membres sont nuls.</span><span class="sxs-lookup"><span data-stu-id="67220-111">The **iItem** member is -1, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67220-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67220-112">Return value</span></span>

<span data-ttu-id="67220-113">Pour supprimer les codes de notification [LVN \_ DELETEITEM](lvn-deleteitem.md) suivants, retournez la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="67220-113">To suppress subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **TRUE**.</span></span>

<span data-ttu-id="67220-114">Pour recevoir les codes de notification [LVN \_ DELETEITEM](lvn-deleteitem.md) suivants, retournez la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="67220-114">To receive subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="67220-115">Notes</span><span class="sxs-lookup"><span data-stu-id="67220-115">Remarks</span></span>

<span data-ttu-id="67220-116">Un contrôle List-View envoie le code de notification [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) lorsqu’il est détruit ou lorsqu’il reçoit le message **\_ DELETEALLITEMS LVM** .</span><span class="sxs-lookup"><span data-stu-id="67220-116">A list-view control sends the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) notification code when it is destroyed or when it receives the **LVM\_DELETEALLITEMS** message.</span></span> <span data-ttu-id="67220-117">Si **LVM \_ DELETEALLITEMS** ne retourne pas la **valeur true**, le contrôle enverra également un code de notification [LVN \_ DELETEITEM](lvn-deleteitem.md) au fur et à mesure que chaque élément sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="67220-117">If **LVM\_DELETEALLITEMS** does not return **TRUE**, the control will also send an [LVN\_DELETEITEM](lvn-deleteitem.md) notification code as each item is deleted.</span></span>

<span data-ttu-id="67220-118">Si le gestionnaire de messages [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) se trouve dans une procédure de boîte de dialogue, retournez la valeur **true** à partir de la procédure de la boîte de dialogue et utilisez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec le \_ MSGRESULT DWL pour définir la valeur de retour du message.</span><span class="sxs-lookup"><span data-stu-id="67220-118">If the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) message handler is in a dialog box procedure, return **TRUE** from the dialog box procedure, and use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set the message return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="67220-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67220-119">Requirements</span></span>



| <span data-ttu-id="67220-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67220-120">Requirement</span></span> | <span data-ttu-id="67220-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="67220-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67220-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67220-122">Minimum supported client</span></span><br/> | <span data-ttu-id="67220-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67220-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67220-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67220-124">Minimum supported server</span></span><br/> | <span data-ttu-id="67220-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67220-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67220-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="67220-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="67220-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="67220-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

