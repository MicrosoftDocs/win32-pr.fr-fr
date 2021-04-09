---
title: Message RB_SIZETORECT (commctrl. h)
description: Tente de trouver la meilleure disposition des bandes pour le rectangle donné.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106252"
---
# <a name="rb_sizetorect-message"></a><span data-ttu-id="c657d-104">\_Message SIZETORECT RB</span><span class="sxs-lookup"><span data-stu-id="c657d-104">RB\_SIZETORECT message</span></span>

<span data-ttu-id="c657d-105">Tente de trouver la meilleure disposition des bandes pour le rectangle donné.</span><span class="sxs-lookup"><span data-stu-id="c657d-105">Attempts to find the best layout of the bands for the given rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="c657d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c657d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c657d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c657d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c657d-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c657d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c657d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c657d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c657d-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie le rectangle vers lequel le contrôle rebar doit être dimensionné.</span><span class="sxs-lookup"><span data-stu-id="c657d-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the rectangle to which the rebar control should be sized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c657d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c657d-111">Return value</span></span>

<span data-ttu-id="c657d-112">Retourne une valeur différente de zéro si une modification de disposition s’est produite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c657d-112">Returns nonzero if a layout change occurred, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c657d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c657d-113">Remarks</span></span>

<span data-ttu-id="c657d-114">Les bandes rebar sont organisées et encapsulées si nécessaire pour s’ajuster au rectangle.</span><span class="sxs-lookup"><span data-stu-id="c657d-114">The rebar bands will be arranged and wrapped as necessary to fit the rectangle.</span></span> <span data-ttu-id="c657d-115">Les bandes qui ont le \_ style RBBS VARIABLEHEIGHT sont redimensionnées aussi uniformément que possible pour s’adapter au rectangle.</span><span class="sxs-lookup"><span data-stu-id="c657d-115">Bands that have the RBBS\_VARIABLEHEIGHT style will be resized as evenly as possible to fit the rectangle.</span></span> <span data-ttu-id="c657d-116">La hauteur d’un Rebar horizontal ou la largeur d’un Rebar vertical peut changer en fonction de la nouvelle disposition.</span><span class="sxs-lookup"><span data-stu-id="c657d-116">The height of a horizontal rebar or the width of a vertical rebar may change, depending on the new layout.</span></span>

## <a name="requirements"></a><span data-ttu-id="c657d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c657d-117">Requirements</span></span>



| <span data-ttu-id="c657d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c657d-118">Requirement</span></span> | <span data-ttu-id="c657d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c657d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c657d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c657d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c657d-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c657d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c657d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c657d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c657d-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c657d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c657d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c657d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c657d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c657d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

