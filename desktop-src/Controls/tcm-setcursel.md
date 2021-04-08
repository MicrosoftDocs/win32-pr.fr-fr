---
title: Message TCM_SETCURSEL (commctrl. h)
description: Sélectionne un onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetCurSel.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- TCM_SETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942156"
---
# <a name="tcm_setcursel-message"></a><span data-ttu-id="7a3f2-105">\_Message SETCURSEL TCM</span><span class="sxs-lookup"><span data-stu-id="7a3f2-105">TCM\_SETCURSEL message</span></span>

<span data-ttu-id="7a3f2-106">Sélectionne un onglet dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="7a3f2-106">Selects a tab in a tab control.</span></span> <span data-ttu-id="7a3f2-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="7a3f2-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a3f2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a3f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a3f2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a3f2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a3f2-110">Index de l’onglet à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="7a3f2-110">Index of the tab to select.</span></span>

</dd> <dt>

<span data-ttu-id="7a3f2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a3f2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7a3f2-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7a3f2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a3f2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a3f2-113">Return value</span></span>

<span data-ttu-id="7a3f2-114">Retourne l’index de l’onglet précédemment sélectionné en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7a3f2-114">Returns the index of the previously selected tab if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a3f2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7a3f2-115">Remarks</span></span>

<span data-ttu-id="7a3f2-116">Un contrôle onglet n’envoie pas de code de notification [TCN \_ SELCHANGING](tcn-selchanging.md) ou [TCN \_ selChange](tcn-selchange.md) lorsqu’un onglet est sélectionné à l’aide de ce message.</span><span class="sxs-lookup"><span data-stu-id="7a3f2-116">A tab control does not send a [TCN\_SELCHANGING](tcn-selchanging.md) or [TCN\_SELCHANGE](tcn-selchange.md) notification code when a tab is selected using this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a3f2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a3f2-117">Requirements</span></span>



| <span data-ttu-id="7a3f2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a3f2-118">Requirement</span></span> | <span data-ttu-id="7a3f2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a3f2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3f2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a3f2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a3f2-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a3f2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a3f2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a3f2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a3f2-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a3f2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a3f2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a3f2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a3f2-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a3f2-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





