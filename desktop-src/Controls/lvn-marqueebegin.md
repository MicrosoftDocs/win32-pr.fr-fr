---
title: LVN_MARQUEEBEGIN le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle d’affichage de liste qu’une sélection de cadre englobant (texte défilant) a commencé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- Contrôles Windows de code de notification LVN_MARQUEEBEGIN
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516300"
---
# <a name="lvn_marqueebegin-notification-code"></a><span data-ttu-id="d0473-105">\_Code de notification LVN MARQUEEBEGIN</span><span class="sxs-lookup"><span data-stu-id="d0473-105">LVN\_MARQUEEBEGIN notification code</span></span>

<span data-ttu-id="d0473-106">Avertit une fenêtre parente d’un contrôle d’affichage de liste qu’une sélection de cadre englobant (texte défilant) a commencé.</span><span class="sxs-lookup"><span data-stu-id="d0473-106">Notifies a list-view control's parent window that a bounding box (marquee) selection has begun.</span></span> <span data-ttu-id="d0473-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d0473-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d0473-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0473-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0473-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0473-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0473-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="d0473-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0473-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0473-111">Return value</span></span>

<span data-ttu-id="d0473-112">Pour accepter le code de notification, retournez zéro.</span><span class="sxs-lookup"><span data-stu-id="d0473-112">To accept the notification code, return zero.</span></span> <span data-ttu-id="d0473-113">Pour quitter la sélection de rectangle englobant, retournez une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d0473-113">To quit the bounding box selection, return nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0473-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d0473-114">Remarks</span></span>

<span data-ttu-id="d0473-115">Une *sélection de cadre englobant* est le processus qui consiste à cliquer sur la zone cliente de la fenêtre d’affichage de liste et à faire glisser pour sélectionner plusieurs éléments simultanément.</span><span class="sxs-lookup"><span data-stu-id="d0473-115">A *bounding box selection* is the process of clicking the list-view window's client area and dragging to select multiple items simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0473-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0473-116">Requirements</span></span>



| <span data-ttu-id="d0473-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0473-117">Requirement</span></span> | <span data-ttu-id="d0473-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0473-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0473-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0473-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d0473-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0473-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0473-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0473-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d0473-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0473-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0473-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0473-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0473-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0473-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





