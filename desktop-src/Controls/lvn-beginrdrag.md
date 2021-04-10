---
title: LVN_BEGINRDRAG le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View qu’une opération de glisser-déplacer impliquant le bouton droit de la souris est initialisée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 93feba3b-8e3e-4a04-bf2c-7ff67a85d4fb
keywords:
- Contrôles Windows de code de notification LVN_BEGINRDRAG
topic_type:
- apiref
api_name:
- LVN_BEGINRDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b4f55c01ca2b5e43419ea926401ac3393d9a9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941709"
---
# <a name="lvn_beginrdrag-notification-code"></a><span data-ttu-id="4804d-105">\_Code de notification LVN BEGINRDRAG</span><span class="sxs-lookup"><span data-stu-id="4804d-105">LVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="4804d-106">Avertit une fenêtre parente d’un contrôle List-View qu’une opération de glisser-déplacer impliquant le bouton droit de la souris est initialisée.</span><span class="sxs-lookup"><span data-stu-id="4804d-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the right mouse button is being initiated.</span></span> <span data-ttu-id="4804d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4804d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINRDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4804d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4804d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4804d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4804d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4804d-110">Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="4804d-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="4804d-111">Le membre **iItem** identifie l’élément déplacé et les autres membres sont nuls.</span><span class="sxs-lookup"><span data-stu-id="4804d-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4804d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4804d-112">Return value</span></span>

<span data-ttu-id="4804d-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4804d-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4804d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4804d-114">Requirements</span></span>



| <span data-ttu-id="4804d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4804d-115">Requirement</span></span> | <span data-ttu-id="4804d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4804d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4804d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4804d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4804d-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4804d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4804d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4804d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4804d-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4804d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4804d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="4804d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4804d-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4804d-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





