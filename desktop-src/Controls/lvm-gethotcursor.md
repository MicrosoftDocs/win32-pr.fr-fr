---
title: Message LVM_GETHOTCURSOR (commctrl. h)
description: Récupère la valeur HCURSOR utilisée lorsque le pointeur se trouve sur un élément alors que la sélection active est activée. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetHotCursor.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743005"
---
# <a name="lvm_gethotcursor-message"></a><span data-ttu-id="561ba-105">\_Message GETHOTCURSOR LVM</span><span class="sxs-lookup"><span data-stu-id="561ba-105">LVM\_GETHOTCURSOR message</span></span>

<span data-ttu-id="561ba-106">Récupère la valeur HCURSOR utilisée lorsque le pointeur se trouve sur un élément alors que la sélection active est activée.</span><span class="sxs-lookup"><span data-stu-id="561ba-106">Retrieves the HCURSOR value used when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="561ba-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .</span><span class="sxs-lookup"><span data-stu-id="561ba-107">You can send this message explicitly or use the [**ListView\_GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="561ba-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="561ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="561ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="561ba-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="561ba-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="561ba-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="561ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="561ba-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="561ba-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="561ba-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="561ba-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="561ba-113">Return value</span></span>

<span data-ttu-id="561ba-114">Retourne une valeur HCURSOR qui est le handle du curseur que le contrôle d’affichage de liste utilise lorsque la sélection active est activée.</span><span class="sxs-lookup"><span data-stu-id="561ba-114">Returns an HCURSOR value that is the handle to the cursor that the list-view control uses when hot tracking is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="561ba-115">Notes</span><span class="sxs-lookup"><span data-stu-id="561ba-115">Remarks</span></span>

<span data-ttu-id="561ba-116">Un contrôle List-View utilise le suivi réactif et la sélection au pointage lorsque le style [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) est défini.</span><span class="sxs-lookup"><span data-stu-id="561ba-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="561ba-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="561ba-117">Requirements</span></span>



| <span data-ttu-id="561ba-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="561ba-118">Requirement</span></span> | <span data-ttu-id="561ba-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="561ba-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="561ba-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="561ba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="561ba-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="561ba-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="561ba-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="561ba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="561ba-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="561ba-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="561ba-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="561ba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="561ba-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="561ba-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





