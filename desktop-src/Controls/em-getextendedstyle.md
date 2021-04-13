---
title: Message EM_GETEXTENDEDSTYLE (commctrl. h)
description: Récupère le style étendu d’un contrôle d’édition. Envoyez ce message explicitement ou à l’aide de la \_ macro Edit GetExtendedStyle.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466111"
---
# <a name="em_getextendedstyle-message-commctrlh"></a><span data-ttu-id="abae7-105">Message EM_GETEXTENDEDSTYLE (commctrl. h)</span><span class="sxs-lookup"><span data-stu-id="abae7-105">EM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="abae7-106">Récupère le style étendu pour un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="abae7-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="abae7-107">Envoyez ce message explicitement ou à l’aide de la macro [**Edit \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="abae7-107">Send this message explicitly or by using the [**Edit\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="abae7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abae7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abae7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abae7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="abae7-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="abae7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="abae7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="abae7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="abae7-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="abae7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abae7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="abae7-113">Return value</span></span>

<span data-ttu-id="abae7-114">Retourne la valeur du style étendu. Pour plus d’informations sur les styles, consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="abae7-114">Returns the value of extended style.For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abae7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="abae7-115">Remarks</span></span>

<span data-ttu-id="abae7-116">Les styles étendus pour un contrôle d’édition n’ont rien à faire avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="abae7-116">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="abae7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abae7-117">Requirements</span></span>



| <span data-ttu-id="abae7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abae7-118">Requirement</span></span> | <span data-ttu-id="abae7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="abae7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abae7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abae7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="abae7-121">Applications de bureau Windows 10, version 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abae7-121">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="abae7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abae7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="abae7-123">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abae7-123">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="abae7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="abae7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="abae7-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="abae7-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

