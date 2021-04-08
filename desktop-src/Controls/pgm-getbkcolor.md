---
title: Message PGM_GETBKCOLOR (commctrl. h)
description: Récupère la couleur d’arrière-plan actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetBkColor.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- PGM_GETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742525"
---
# <a name="pgm_getbkcolor-message"></a><span data-ttu-id="025cb-105">\_Message GETBKCOLOR PGM</span><span class="sxs-lookup"><span data-stu-id="025cb-105">PGM\_GETBKCOLOR message</span></span>

<span data-ttu-id="025cb-106">Récupère la couleur d’arrière-plan actuelle pour le contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="025cb-106">Retrieves the current background color for the pager control.</span></span> <span data-ttu-id="025cb-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="025cb-107">You can send this message explicitly or use the [**Pager\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="025cb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="025cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="025cb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="025cb-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="025cb-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="025cb-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="025cb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="025cb-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="025cb-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="025cb-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="025cb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="025cb-113">Return value</span></span>

<span data-ttu-id="025cb-114">Retourne une valeur **COLORREF** qui contient la couleur d’arrière-plan actuelle.</span><span class="sxs-lookup"><span data-stu-id="025cb-114">Returns a **COLORREF** value that contains the current background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="025cb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="025cb-115">Remarks</span></span>

<span data-ttu-id="025cb-116">Par défaut, le contrôle de pagineur utilise la couleur de la face du bouton système comme couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="025cb-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="025cb-117">Il s’agit de la même couleur que celle qui peut être récupérée en appelant [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) avec la couleur \_ BTNFACE.</span><span class="sxs-lookup"><span data-stu-id="025cb-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="025cb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="025cb-118">Requirements</span></span>



| <span data-ttu-id="025cb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="025cb-119">Requirement</span></span> | <span data-ttu-id="025cb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="025cb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="025cb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="025cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="025cb-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="025cb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="025cb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="025cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="025cb-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="025cb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="025cb-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="025cb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="025cb-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="025cb-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

