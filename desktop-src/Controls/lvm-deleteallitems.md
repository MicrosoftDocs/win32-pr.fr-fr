---
title: Message LVM_DELETEALLITEMS (commctrl. h)
description: Supprime tous les éléments d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView DeleteAllItems.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- LVM_DELETEALLITEMS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464298"
---
# <a name="lvm_deleteallitems-message"></a><span data-ttu-id="fdee9-105">\_Message DELETEALLITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="fdee9-105">LVM\_DELETEALLITEMS message</span></span>

<span data-ttu-id="fdee9-106">Supprime tous les éléments d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="fdee9-106">Removes all items from a list-view control.</span></span> <span data-ttu-id="fdee9-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) .</span><span class="sxs-lookup"><span data-stu-id="fdee9-107">You can send this message explicitly or by using the [**ListView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdee9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fdee9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdee9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdee9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fdee9-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="fdee9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fdee9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdee9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fdee9-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="fdee9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdee9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fdee9-113">Return value</span></span>

<span data-ttu-id="fdee9-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fdee9-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdee9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fdee9-115">Remarks</span></span>

<span data-ttu-id="fdee9-116">Lorsqu’un contrôle List-View reçoit le **message \_ DELETEALLITEMS LVM** , il envoie le code de notification [**\_ DELETEALLITEMS LVN**](lvn-deleteallitems.md) à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="fdee9-116">When a list-view control receives the **LVM\_DELETEALLITEMS** message, it sends the [**LVN\_DELETEALLITEMS**](lvn-deleteallitems.md) notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdee9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdee9-117">Requirements</span></span>



| <span data-ttu-id="fdee9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdee9-118">Requirement</span></span> | <span data-ttu-id="fdee9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdee9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdee9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdee9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fdee9-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdee9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fdee9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdee9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fdee9-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fdee9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdee9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fdee9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdee9-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdee9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





