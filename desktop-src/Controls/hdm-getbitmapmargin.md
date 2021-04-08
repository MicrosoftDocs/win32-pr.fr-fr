---
title: Message HDM_GETBITMAPMARGIN (commctrl. h)
description: Obtient la largeur de la marge de bitmap pour un contrôle d’en-tête. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetBitmapMargin.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- HDM_GETBITMAPMARGIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942168"
---
# <a name="hdm_getbitmapmargin-message"></a><span data-ttu-id="82af9-105">\_Message HDM GETBITMAPMARGIN</span><span class="sxs-lookup"><span data-stu-id="82af9-105">HDM\_GETBITMAPMARGIN message</span></span>

<span data-ttu-id="82af9-106">Obtient la largeur de la marge de bitmap pour un contrôle d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="82af9-106">Gets the width of the bitmap margin for a header control.</span></span> <span data-ttu-id="82af9-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) .</span><span class="sxs-lookup"><span data-stu-id="82af9-107">You can send this message explicitly or use the [**Header\_GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="82af9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82af9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82af9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82af9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="82af9-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="82af9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="82af9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82af9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="82af9-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="82af9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82af9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82af9-113">Return value</span></span>

<span data-ttu-id="82af9-114">Retourne la largeur, en pixels, de la marge de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="82af9-114">Returns the width of the bitmap margin in pixels.</span></span> <span data-ttu-id="82af9-115">Si la marge de bitmap n’a pas été précédemment spécifiée, la valeur par défaut de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ CXEDGE) est retournée.</span><span class="sxs-lookup"><span data-stu-id="82af9-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM\_CXEDGE) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="82af9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82af9-116">Requirements</span></span>



| <span data-ttu-id="82af9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82af9-117">Requirement</span></span> | <span data-ttu-id="82af9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="82af9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82af9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82af9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="82af9-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82af9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82af9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82af9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="82af9-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82af9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82af9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="82af9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="82af9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="82af9-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82af9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82af9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82af9-126">**HDM \_ SETBITMAPMARGIN**</span><span class="sxs-lookup"><span data-stu-id="82af9-126">**HDM\_SETBITMAPMARGIN**</span></span>](hdm-setbitmapmargin.md)
</dt> </dl>

 

