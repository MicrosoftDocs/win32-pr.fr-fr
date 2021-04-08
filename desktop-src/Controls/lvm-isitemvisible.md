---
title: Message LVM_ISITEMVISIBLE (commctrl. h)
description: Indique si un élément du contrôle List-View est visible. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView IsItemVisible.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- LVM_ISITEMVISIBLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844081"
---
# <a name="lvm_isitemvisible-message"></a><span data-ttu-id="94986-105">\_Message ISITEMVISIBLE LVM</span><span class="sxs-lookup"><span data-stu-id="94986-105">LVM\_ISITEMVISIBLE message</span></span>

<span data-ttu-id="94986-106">Indique si un élément du contrôle List-View est visible.</span><span class="sxs-lookup"><span data-stu-id="94986-106">Indicates if an item in the list-view control is visible.</span></span> <span data-ttu-id="94986-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .</span><span class="sxs-lookup"><span data-stu-id="94986-107">Send this message explicitly or by using the [**ListView\_IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="94986-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94986-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94986-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94986-110">Index de l’élément dans le contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="94986-110">An index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="94986-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94986-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="94986-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="94986-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94986-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94986-113">Return value</span></span>

<span data-ttu-id="94986-114">Retourne la **valeur true** si visible, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="94986-114">Returns **TRUE** if visible, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="94986-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94986-115">Requirements</span></span>



| <span data-ttu-id="94986-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94986-116">Requirement</span></span> | <span data-ttu-id="94986-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="94986-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94986-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94986-118">Minimum supported client</span></span><br/> | <span data-ttu-id="94986-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94986-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94986-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94986-120">Minimum supported server</span></span><br/> | <span data-ttu-id="94986-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94986-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94986-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="94986-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="94986-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="94986-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





