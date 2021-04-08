---
title: HDN_ITEMCLICK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur a cliqué sur le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- Contrôles Windows de code de notification HDN_ITEMCLICK
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844122"
---
# <a name="hdn_itemclick-notification-code"></a><span data-ttu-id="e7cca-105">\_Code de notification HDN ITEMCLICK</span><span class="sxs-lookup"><span data-stu-id="e7cca-105">HDN\_ITEMCLICK notification code</span></span>

<span data-ttu-id="e7cca-106">Avertit la fenêtre parente d’un contrôle header que l’utilisateur a cliqué sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="e7cca-106">Notifies a header control's parent window that the user clicked the control.</span></span> <span data-ttu-id="e7cca-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e7cca-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e7cca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7cca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7cca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7cca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7cca-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui identifie le contrôle d’en-tête et spécifie l’index de l’élément d’en-tête sur lequel l’utilisateur a cliqué et le bouton de la souris utilisé pour cliquer sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="e7cca-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that identifies the header control and specifies the index of the header item that was clicked and the mouse button used to click the item.</span></span> <span data-ttu-id="e7cca-111">Le membre **pItem** a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="e7cca-111">The **pItem** member is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7cca-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7cca-112">Return value</span></span>

<span data-ttu-id="e7cca-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e7cca-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7cca-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e7cca-114">Remarks</span></span>

<span data-ttu-id="e7cca-115">Un contrôle header envoie ce code de notification lorsque l’utilisateur relâche le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="e7cca-115">A header control sends this notification code after the user releases the left mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7cca-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7cca-116">Requirements</span></span>



| <span data-ttu-id="e7cca-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7cca-117">Requirement</span></span> | <span data-ttu-id="e7cca-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7cca-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7cca-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7cca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e7cca-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7cca-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7cca-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7cca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e7cca-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7cca-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7cca-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7cca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7cca-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7cca-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e7cca-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e7cca-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e7cca-126">**HDN \_ ITEMCLICKW** (Unicode) et **HDN \_ ITEMCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e7cca-126">**HDN\_ITEMCLICKW** (Unicode) and **HDN\_ITEMCLICKA** (ANSI)</span></span><br/>               |



 

 





