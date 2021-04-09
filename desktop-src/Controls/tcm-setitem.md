---
title: Message TCM_SETITEM (commctrl. h)
description: Définit tout ou partie des attributs d’un onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetItem.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739885"
---
# <a name="tcm_setitem-message"></a><span data-ttu-id="fd605-105">\_Message SETITEM TCM</span><span class="sxs-lookup"><span data-stu-id="fd605-105">TCM\_SETITEM message</span></span>

<span data-ttu-id="fd605-106">Définit tout ou partie des attributs d’un onglet.</span><span class="sxs-lookup"><span data-stu-id="fd605-106">Sets some or all of a tab's attributes.</span></span> <span data-ttu-id="fd605-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) .</span><span class="sxs-lookup"><span data-stu-id="fd605-107">You can send this message explicitly or by using the [**TabCtrl\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd605-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd605-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd605-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd605-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd605-110">Index de l’élément.</span><span class="sxs-lookup"><span data-stu-id="fd605-110">Index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="fd605-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd605-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd605-112">Pointeur vers une structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) qui contient les nouveaux attributs d’élément.</span><span class="sxs-lookup"><span data-stu-id="fd605-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="fd605-113">Le membre **Mask** spécifie les attributs à définir.</span><span class="sxs-lookup"><span data-stu-id="fd605-113">The **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="fd605-114">Si le membre de **masque** spécifie la \_ valeur de texte TCIF, le membre **pszText** est l’adresse d’une chaîne terminée par le caractère null et le membre **cchTextMax** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="fd605-114">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd605-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd605-115">Return value</span></span>

<span data-ttu-id="fd605-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fd605-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd605-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd605-117">Requirements</span></span>



| <span data-ttu-id="fd605-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd605-118">Requirement</span></span> | <span data-ttu-id="fd605-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd605-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd605-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd605-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd605-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd605-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd605-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd605-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd605-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd605-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd605-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd605-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd605-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd605-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fd605-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="fd605-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fd605-127">**TCM \_ SETITEMW** (Unicode) et **TCM \_ SETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fd605-127">**TCM\_SETITEMW** (Unicode) and **TCM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





