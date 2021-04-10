---
title: Message TTM_GETBUBBLESIZE (commctrl. h)
description: Retourne la largeur et la hauteur d’un contrôle ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- TTM_GETBUBBLESIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103750"
---
# <a name="ttm_getbubblesize-message"></a><span data-ttu-id="6e2c2-104">\_Message atténuation GETBUBBLESIZE</span><span class="sxs-lookup"><span data-stu-id="6e2c2-104">TTM\_GETBUBBLESIZE message</span></span>

<span data-ttu-id="6e2c2-105">Retourne la largeur et la hauteur d’un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-105">Returns the width and height of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e2c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e2c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e2c2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e2c2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6e2c2-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6e2c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e2c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e2c2-110">Pointeur vers la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-110">Pointer to the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e2c2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e2c2-111">Return value</span></span>

<span data-ttu-id="6e2c2-112">Retourne la largeur de l’info-bulle dans le mot de poids faible et la hauteur du mot haut en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-112">Returns the width of the tooltip in the low word and the height in the high word if successful.</span></span> <span data-ttu-id="6e2c2-113">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-113">Otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e2c2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6e2c2-114">Remarks</span></span>

<span data-ttu-id="6e2c2-115">Si les \_ \_ indicateurs absolus Track et ttf sont définis dans le membre **uFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’info-bulle, ce message peut être utilisé pour aider à positionner l’info-bulle avec précision.</span><span class="sxs-lookup"><span data-stu-id="6e2c2-115">If the TTF\_TRACK and TTF\_ABSOLUTE flags are set in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, this message can be used to help position the tooltip accurately.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e2c2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e2c2-116">Requirements</span></span>



| <span data-ttu-id="6e2c2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e2c2-117">Requirement</span></span> | <span data-ttu-id="6e2c2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e2c2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2c2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e2c2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6e2c2-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e2c2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e2c2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e2c2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6e2c2-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e2c2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e2c2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e2c2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e2c2-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e2c2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





