---
title: Code de notification NM_HOVER (mode liste) (commctrl. h)
description: Envoyé par un contrôle List-View lorsque la souris pointe sur un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- Contrôles Windows de code de notification NM_HOVER (mode liste)
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60606dfac73e13b0439ce861f37cb4ec941fda3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843077"
---
# <a name="nm_hover-list-view-notification-code"></a><span data-ttu-id="3eb21-105">\_Code de notification de pointage nm (mode liste)</span><span class="sxs-lookup"><span data-stu-id="3eb21-105">NM\_HOVER (list view) notification code</span></span>

<span data-ttu-id="3eb21-106">Envoyé par un contrôle List-View lorsque la souris pointe sur un élément.</span><span class="sxs-lookup"><span data-stu-id="3eb21-106">Sent by a list-view control when the mouse hovers over an item.</span></span> <span data-ttu-id="3eb21-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb21-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3eb21-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3eb21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eb21-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3eb21-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3eb21-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="3eb21-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eb21-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3eb21-111">Return value</span></span>

<span data-ttu-id="3eb21-112">Retourne zéro pour permettre à la vue de liste de traiter le pointage normalement ou une valeur différente de zéro pour empêcher le pointage d’être traité.</span><span class="sxs-lookup"><span data-stu-id="3eb21-112">Return zero to allow the list view to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eb21-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3eb21-113">Requirements</span></span>



| <span data-ttu-id="3eb21-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3eb21-114">Requirement</span></span> | <span data-ttu-id="3eb21-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eb21-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb21-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3eb21-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3eb21-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3eb21-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3eb21-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3eb21-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3eb21-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3eb21-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3eb21-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3eb21-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3eb21-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eb21-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





