---
title: Message TTM_DELTOOL (commctrl. h)
description: Supprime un outil d’un contrôle ToolTip.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- TTM_DELTOOL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510751"
---
# <a name="ttm_deltool-message"></a><span data-ttu-id="8bf92-104">\_Message atténuation DELTOOL</span><span class="sxs-lookup"><span data-stu-id="8bf92-104">TTM\_DELTOOL message</span></span>

<span data-ttu-id="8bf92-105">Supprime un outil d’un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="8bf92-105">Removes a tool from a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8bf92-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bf92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf92-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8bf92-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8bf92-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8bf92-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8bf92-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8bf92-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf92-110">Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="8bf92-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="8bf92-111">Les membres **HWND** et **UID** identifient l’outil à supprimer, tandis que le membre **cbSize** doit spécifier la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="8bf92-111">The **hwnd** and **uId** members identify the tool to remove, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="8bf92-112">Tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="8bf92-112">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf92-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8bf92-113">Return value</span></span>

<span data-ttu-id="8bf92-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8bf92-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf92-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bf92-115">Requirements</span></span>



| <span data-ttu-id="8bf92-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bf92-116">Requirement</span></span> | <span data-ttu-id="8bf92-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bf92-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf92-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bf92-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf92-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bf92-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8bf92-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bf92-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf92-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8bf92-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8bf92-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8bf92-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf92-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf92-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8bf92-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="8bf92-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8bf92-125">**Atténuation \_ DELTOOLW** (Unicode) et **atténuation \_ DELTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8bf92-125">**TTM\_DELTOOLW** (Unicode) and **TTM\_DELTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="8bf92-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bf92-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8bf92-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="8bf92-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8bf92-128">**ATTÉNUATION \_ ADDTOOL**</span><span class="sxs-lookup"><span data-stu-id="8bf92-128">**TTM\_ADDTOOL**</span></span>](ttm-addtool.md)
</dt> <dt>

<span data-ttu-id="8bf92-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="8bf92-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8bf92-130">À propos des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="8bf92-130">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





