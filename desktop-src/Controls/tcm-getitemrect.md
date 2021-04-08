---
title: Message TCM_GETITEMRECT (commctrl. h)
description: Récupère le rectangle englobant d’un onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetItemRect.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- TCM_GETITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844181"
---
# <a name="tcm_getitemrect-message"></a><span data-ttu-id="a0f45-105">\_Message GETITEMRECT TCM</span><span class="sxs-lookup"><span data-stu-id="a0f45-105">TCM\_GETITEMRECT message</span></span>

<span data-ttu-id="a0f45-106">Récupère le rectangle englobant d’un onglet dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="a0f45-106">Retrieves the bounding rectangle for a tab in a tab control.</span></span> <span data-ttu-id="a0f45-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="a0f45-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0f45-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0f45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f45-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0f45-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0f45-110">Index de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="a0f45-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="a0f45-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0f45-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0f45-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle englobant de l’onglet, dans les coordonnées de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a0f45-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the tab, in viewport coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f45-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0f45-113">Return value</span></span>

<span data-ttu-id="a0f45-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a0f45-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f45-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0f45-115">Requirements</span></span>



| <span data-ttu-id="a0f45-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0f45-116">Requirement</span></span> | <span data-ttu-id="a0f45-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0f45-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f45-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0f45-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f45-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0f45-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0f45-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0f45-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f45-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0f45-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0f45-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0f45-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0f45-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f45-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

