---
title: Message LVN_ENDSCROLL (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View quand une opération de défilement se termine. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- LVN_ENDSCROLL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9dcdcff2d0bcfc28e1818d5add6d37838e5f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844478"
---
# <a name="lvn_endscroll-message"></a><span data-ttu-id="8c81f-105">\_Message LVN ENDSCROLL</span><span class="sxs-lookup"><span data-stu-id="8c81f-105">LVN\_ENDSCROLL message</span></span>

<span data-ttu-id="8c81f-106">Avertit la fenêtre parente d’un contrôle List-View quand une opération de défilement se termine.</span><span class="sxs-lookup"><span data-stu-id="8c81f-106">Notifies a list-view control's parent window when a scrolling operation ends.</span></span> <span data-ttu-id="8c81f-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8c81f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8c81f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c81f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c81f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c81f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c81f-110">Pointeur vers une structure [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) qui contient la position horizontale ou verticale de l’emplacement où l’opération de défilement se termine.</span><span class="sxs-lookup"><span data-stu-id="8c81f-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation ends.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c81f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c81f-111">Return value</span></span>

<span data-ttu-id="8c81f-112">Valeur de retour non utilisée.</span><span class="sxs-lookup"><span data-stu-id="8c81f-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c81f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8c81f-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8c81f-114">Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="8c81f-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="8c81f-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8c81f-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c81f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c81f-116">Requirements</span></span>



| <span data-ttu-id="8c81f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c81f-117">Requirement</span></span> | <span data-ttu-id="8c81f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c81f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c81f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c81f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8c81f-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c81f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c81f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c81f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8c81f-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c81f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c81f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c81f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c81f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c81f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





