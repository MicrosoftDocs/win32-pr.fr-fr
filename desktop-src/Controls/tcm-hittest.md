---
title: Message TCM_HITTEST (commctrl. h)
description: Détermine l’onglet, le cas échéant, à la position d’écran spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- TCM_HITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510353"
---
# <a name="tcm_hittest-message"></a><span data-ttu-id="a17f4-105">\_Message TCM HITTEST</span><span class="sxs-lookup"><span data-stu-id="a17f4-105">TCM\_HITTEST message</span></span>

<span data-ttu-id="a17f4-106">Détermine l’onglet, le cas échéant, à la position d’écran spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a17f4-106">Determines which tab, if any, is at a specified screen position.</span></span> <span data-ttu-id="a17f4-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) .</span><span class="sxs-lookup"><span data-stu-id="a17f4-107">You can send this message explicitly or by using the [**TabCtrl\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a17f4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a17f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a17f4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a17f4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a17f4-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a17f4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a17f4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a17f4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a17f4-112">Pointeur vers une structure [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) qui spécifie la position à l’écran à tester.</span><span class="sxs-lookup"><span data-stu-id="a17f4-112">Pointer to a [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) structure that specifies the screen position to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a17f4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a17f4-113">Return value</span></span>

<span data-ttu-id="a17f4-114">Retourne l’index de l’onglet ou-1 si aucun onglet n’est à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a17f4-114">Returns the index of the tab, or -1 if no tab is at the specified position.</span></span>

## <a name="requirements"></a><span data-ttu-id="a17f4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a17f4-115">Requirements</span></span>



| <span data-ttu-id="a17f4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a17f4-116">Requirement</span></span> | <span data-ttu-id="a17f4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a17f4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a17f4-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a17f4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a17f4-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a17f4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a17f4-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a17f4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a17f4-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a17f4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a17f4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="a17f4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a17f4-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a17f4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





