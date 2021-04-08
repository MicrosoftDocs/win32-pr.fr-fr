---
title: Message HDM_SETBITMAPMARGIN (commctrl. h)
description: Définit la largeur de la marge, spécifiée en pixels, d’une image bitmap dans un contrôle d’en-tête existant. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetBitmapMargin.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- HDM_SETBITMAPMARGIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844041"
---
# <a name="hdm_setbitmapmargin-message"></a><span data-ttu-id="555ee-105">\_Message HDM SETBITMAPMARGIN</span><span class="sxs-lookup"><span data-stu-id="555ee-105">HDM\_SETBITMAPMARGIN message</span></span>

<span data-ttu-id="555ee-106">Définit la largeur de la marge, spécifiée en pixels, d’une image bitmap dans un contrôle d’en-tête existant.</span><span class="sxs-lookup"><span data-stu-id="555ee-106">Sets the width of the margin, specified in pixels, of a bitmap in an existing header control.</span></span> <span data-ttu-id="555ee-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) .</span><span class="sxs-lookup"><span data-stu-id="555ee-107">You can send this message explicitly or use the [**Header\_SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="555ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="555ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="555ee-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="555ee-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="555ee-110">Largeur, spécifiée en pixels, de la marge qui entoure une bitmap dans un contrôle d’en-tête existant.</span><span class="sxs-lookup"><span data-stu-id="555ee-110">The width, specified in pixels, of the margin that surrounds a bitmap within an existing header control.</span></span>

</dd> <dt>

<span data-ttu-id="555ee-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="555ee-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="555ee-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="555ee-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="555ee-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="555ee-113">Return value</span></span>

<span data-ttu-id="555ee-114">Retourne la largeur de la marge de la bitmap, en pixels.</span><span class="sxs-lookup"><span data-stu-id="555ee-114">Returns the width of the bitmap margin, in pixels.</span></span> <span data-ttu-id="555ee-115">Si la marge de bitmap n’a pas été précédemment spécifiée, la valeur par défaut de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*) est retournée.</span><span class="sxs-lookup"><span data-stu-id="555ee-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM\_CXEDGE*) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="555ee-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="555ee-116">Requirements</span></span>



| <span data-ttu-id="555ee-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="555ee-117">Requirement</span></span> | <span data-ttu-id="555ee-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="555ee-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="555ee-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="555ee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="555ee-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="555ee-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="555ee-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="555ee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="555ee-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="555ee-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="555ee-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="555ee-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="555ee-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="555ee-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="555ee-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="555ee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="555ee-126">**HDM \_ GETBITMAPMARGIN**</span><span class="sxs-lookup"><span data-stu-id="555ee-126">**HDM\_GETBITMAPMARGIN**</span></span>](hdm-getbitmapmargin.md)
</dt> </dl>

 

