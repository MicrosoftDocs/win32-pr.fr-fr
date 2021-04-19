---
title: BCN_DROPDOWN le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur clique sur une flèche de déroulement sur un bouton. La fenêtre parente du contrôle reçoit ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- Contrôles Windows de code de notification BCN_DROPDOWN
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511554"
---
# <a name="bcn_dropdown-notification-code"></a><span data-ttu-id="559cf-105">\_Code de notification de liste déroulante BCN</span><span class="sxs-lookup"><span data-stu-id="559cf-105">BCN\_DROPDOWN notification code</span></span>

<span data-ttu-id="559cf-106">Envoyé lorsque l’utilisateur clique sur une flèche de déroulement sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="559cf-106">Sent when the user clicks a drop down arrow on a button.</span></span> <span data-ttu-id="559cf-107">La fenêtre parente du contrôle reçoit ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="559cf-107">The parent window of the control receives this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="559cf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="559cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="559cf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="559cf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="559cf-110">Pointeur vers une structure [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) .</span><span class="sxs-lookup"><span data-stu-id="559cf-110">A pointer to a [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="559cf-111">Le membre **rcButton** est défini pour décrire la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="559cf-111">The **rcButton** member is set to describe the drop-down area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="559cf-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="559cf-112">Return value</span></span>

<span data-ttu-id="559cf-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="559cf-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="559cf-114">Notes</span><span class="sxs-lookup"><span data-stu-id="559cf-114">Remarks</span></span>

<span data-ttu-id="559cf-115">Le récepteur de notification convertit **lParam** pour récupérer la structure [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) .</span><span class="sxs-lookup"><span data-stu-id="559cf-115">The notification receiver casts **LPARAM** to retrieve the [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="559cf-116">**WParam** contient l’ID du contrôle qui envoie ce message.</span><span class="sxs-lookup"><span data-stu-id="559cf-116">**WPARAM** contains the ID of the control that sends this message.</span></span> <span data-ttu-id="559cf-117">Le contrôle Button doit avoir un style de bouton déroulant.</span><span class="sxs-lookup"><span data-stu-id="559cf-117">The button control must have a drop-down button style.</span></span>

## <a name="requirements"></a><span data-ttu-id="559cf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="559cf-118">Requirements</span></span>



| <span data-ttu-id="559cf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="559cf-119">Requirement</span></span> | <span data-ttu-id="559cf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="559cf-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="559cf-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="559cf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="559cf-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="559cf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="559cf-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="559cf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="559cf-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="559cf-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="559cf-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="559cf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="559cf-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="559cf-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





