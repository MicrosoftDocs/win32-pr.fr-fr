---
title: Message PGM_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan actuelle pour le contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ SetBkColor.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- PGM_SETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103480"
---
# <a name="pgm_setbkcolor-message"></a><span data-ttu-id="47736-105">\_Message SETBKCOLOR PGM</span><span class="sxs-lookup"><span data-stu-id="47736-105">PGM\_SETBKCOLOR message</span></span>

<span data-ttu-id="47736-106">Définit la couleur d’arrière-plan actuelle pour le contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="47736-106">Sets the current background color for the pager control.</span></span> <span data-ttu-id="47736-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="47736-107">You can send this message explicitly or use the [**Pager\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="47736-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47736-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47736-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="47736-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="47736-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="47736-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="47736-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47736-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47736-112">Valeur **COLORREF** qui contient la nouvelle couleur d’arrière-plan du contrôle de pagineur.</span><span class="sxs-lookup"><span data-stu-id="47736-112">**COLORREF** value that contains the new background color of the pager control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47736-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47736-113">Return value</span></span>

<span data-ttu-id="47736-114">Retourne une valeur **COLORREF** qui contient la couleur d’arrière-plan précédente.</span><span class="sxs-lookup"><span data-stu-id="47736-114">Returns a **COLORREF** value that contains the previous background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="47736-115">Notes</span><span class="sxs-lookup"><span data-stu-id="47736-115">Remarks</span></span>

<span data-ttu-id="47736-116">Par défaut, le contrôle de pagineur utilise la couleur de la face du bouton système comme couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="47736-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="47736-117">Il s’agit de la même couleur que celle qui peut être récupérée en appelant [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) avec la couleur \_ BTNFACE.</span><span class="sxs-lookup"><span data-stu-id="47736-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="47736-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47736-118">Requirements</span></span>



| <span data-ttu-id="47736-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47736-119">Requirement</span></span> | <span data-ttu-id="47736-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="47736-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47736-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47736-121">Minimum supported client</span></span><br/> | <span data-ttu-id="47736-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47736-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47736-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47736-123">Minimum supported server</span></span><br/> | <span data-ttu-id="47736-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47736-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47736-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="47736-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="47736-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="47736-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

