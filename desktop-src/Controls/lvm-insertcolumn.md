---
title: Message LVM_INSERTCOLUMN (commctrl. h)
description: Insère une nouvelle colonne dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de ListView \_ InsertColumn.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- LVM_INSERTCOLUMN les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509154"
---
# <a name="lvm_insertcolumn-message"></a><span data-ttu-id="4110c-105">\_Message LVM INSERTCOLUMN</span><span class="sxs-lookup"><span data-stu-id="4110c-105">LVM\_INSERTCOLUMN message</span></span>

<span data-ttu-id="4110c-106">Insère une nouvelle colonne dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="4110c-106">Inserts a new column in a list-view control.</span></span> <span data-ttu-id="4110c-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .</span><span class="sxs-lookup"><span data-stu-id="4110c-107">You can send this message explicitly or by using the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4110c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4110c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4110c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4110c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4110c-110">Index de la nouvelle colonne.</span><span class="sxs-lookup"><span data-stu-id="4110c-110">Index of the new column.</span></span>

</dd> <dt>

<span data-ttu-id="4110c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4110c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4110c-112">Pointeur vers une structure [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) qui contient les attributs de la nouvelle colonne.</span><span class="sxs-lookup"><span data-stu-id="4110c-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the attributes of the new column.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4110c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4110c-113">Return value</span></span>

<span data-ttu-id="4110c-114">Retourne l’index de la nouvelle colonne en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4110c-114">Returns the index of the new column if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4110c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4110c-115">Remarks</span></span>

<span data-ttu-id="4110c-116">Les colonnes sont visibles uniquement dans la vue rapport (détails).</span><span class="sxs-lookup"><span data-stu-id="4110c-116">Columns are visible only in report (details) view.</span></span>

## <a name="requirements"></a><span data-ttu-id="4110c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4110c-117">Requirements</span></span>



| <span data-ttu-id="4110c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4110c-118">Requirement</span></span> | <span data-ttu-id="4110c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4110c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4110c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4110c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4110c-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4110c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4110c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4110c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4110c-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4110c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4110c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4110c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4110c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4110c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





