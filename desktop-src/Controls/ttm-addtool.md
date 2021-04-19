---
title: Message TTM_ADDTOOL (commctrl. h)
description: Inscrit un outil avec un contrôle ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- TTM_ADDTOOL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509924"
---
# <a name="ttm_addtool-message"></a><span data-ttu-id="db6ea-104">\_Message atténuation ADDTOOL</span><span class="sxs-lookup"><span data-stu-id="db6ea-104">TTM\_ADDTOOL message</span></span>

<span data-ttu-id="db6ea-105">Inscrit un outil avec un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="db6ea-105">Registers a tool with a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="db6ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db6ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6ea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db6ea-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="db6ea-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="db6ea-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="db6ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db6ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db6ea-110">Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) contenant les informations dont le contrôle ToolTip a besoin pour afficher le texte de l’outil.</span><span class="sxs-lookup"><span data-stu-id="db6ea-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure containing information that the tooltip control needs to display text for the tool.</span></span> <span data-ttu-id="db6ea-111">Le membre **cbSize** de cette structure doit être rempli avant l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="db6ea-111">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db6ea-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db6ea-112">Return value</span></span>

<span data-ttu-id="db6ea-113">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="db6ea-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="db6ea-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db6ea-114">Requirements</span></span>



| <span data-ttu-id="db6ea-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db6ea-115">Requirement</span></span> | <span data-ttu-id="db6ea-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="db6ea-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db6ea-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db6ea-117">Minimum supported client</span></span><br/> | <span data-ttu-id="db6ea-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db6ea-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db6ea-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db6ea-119">Minimum supported server</span></span><br/> | <span data-ttu-id="db6ea-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db6ea-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db6ea-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="db6ea-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="db6ea-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db6ea-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="db6ea-123">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="db6ea-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="db6ea-124">**Atténuation \_ ADDTOOLW** (Unicode) et **atténuation \_ ADDTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="db6ea-124">**TTM\_ADDTOOLW** (Unicode) and **TTM\_ADDTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="db6ea-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db6ea-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="db6ea-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="db6ea-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="db6ea-127">**ATTÉNUATION \_ DELTOOL**</span><span class="sxs-lookup"><span data-stu-id="db6ea-127">**TTM\_DELTOOL**</span></span>](ttm-deltool.md)
</dt> <dt>

<span data-ttu-id="db6ea-128">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="db6ea-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="db6ea-129">À propos des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="db6ea-129">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





