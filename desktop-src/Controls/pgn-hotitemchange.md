---
title: Message PGN_HOTITEMCHANGE (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle de pagineur que l’élément réactif (en surbrillance) a changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- PGN_HOTITEMCHANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573f3dd93a6e4b0b3db6682d36804416d6f6f1e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032753"
---
# <a name="pgn_hotitemchange-message"></a><span data-ttu-id="2e538-105">\_Message PGN HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="2e538-105">PGN\_HOTITEMCHANGE message</span></span>

<span data-ttu-id="2e538-106">Avertit la fenêtre parente d’un contrôle de pagineur que l’élément réactif (en surbrillance) a changé.</span><span class="sxs-lookup"><span data-stu-id="2e538-106">Notifies a pager control's parent window that the hot (highlighted) item has change.</span></span> <span data-ttu-id="2e538-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2e538-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2e538-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e538-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e538-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e538-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e538-110">Pointeur vers une structure [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="2e538-110">Pointer to a [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e538-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e538-111">Return value</span></span>

<span data-ttu-id="2e538-112">Retournez zéro pour mettre en surbrillance l’élément ou une valeur différente de zéro pour empêcher la mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="2e538-112">Return zero to highlight the item or nonzero to prevent highlighting.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e538-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2e538-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2e538-114">Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="2e538-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2e538-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2e538-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e538-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e538-116">Requirements</span></span>



| <span data-ttu-id="2e538-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e538-117">Requirement</span></span> | <span data-ttu-id="2e538-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e538-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e538-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e538-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2e538-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e538-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e538-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e538-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2e538-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e538-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e538-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e538-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e538-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e538-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





