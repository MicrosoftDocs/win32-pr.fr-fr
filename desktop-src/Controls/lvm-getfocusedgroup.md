---
title: Message LVM_GETFOCUSEDGROUP (commctrl. h)
description: Obtient le groupe qui a le focus. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetFocusedGroup.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- LVM_GETFOCUSEDGROUP les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464274"
---
# <a name="lvm_getfocusedgroup-message"></a><span data-ttu-id="ce19c-105">\_Message GETFOCUSEDGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="ce19c-105">LVM\_GETFOCUSEDGROUP message</span></span>

<span data-ttu-id="ce19c-106">Obtient le groupe qui a le focus.</span><span class="sxs-lookup"><span data-stu-id="ce19c-106">Gets the group that has the focus.</span></span> <span data-ttu-id="ce19c-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) .</span><span class="sxs-lookup"><span data-stu-id="ce19c-107">Send this message explicitly or by using the [**ListView\_GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce19c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce19c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce19c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce19c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ce19c-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ce19c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ce19c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce19c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ce19c-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ce19c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce19c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce19c-113">Return value</span></span>

<span data-ttu-id="ce19c-114">Retourne l’index du groupe avec l’État LVGS \_ Focused, ou-1 s’il n’existe aucun groupe avec l’État LVGS \_ focus.</span><span class="sxs-lookup"><span data-stu-id="ce19c-114">Returns the index of the group with state of LVGS\_FOCUSED, or -1 if there is no group with state of LVGS\_FOCUSED.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce19c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce19c-115">Requirements</span></span>



| <span data-ttu-id="ce19c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce19c-116">Requirement</span></span> | <span data-ttu-id="ce19c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce19c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce19c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce19c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ce19c-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce19c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce19c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce19c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ce19c-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce19c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce19c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce19c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce19c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce19c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





