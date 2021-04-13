---
title: Message RB_SETCOLORSCHEME (commctrl. h)
description: Définit les informations de jeu de couleurs pour le contrôle rebar.
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- RB_SETCOLORSCHEME les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c7725d3c0bc3f3a7a7a72db16e19626a3c4d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508698"
---
# <a name="rb_setcolorscheme-message"></a><span data-ttu-id="9cc00-104">\_Message SETCOLORSCHEME RB</span><span class="sxs-lookup"><span data-stu-id="9cc00-104">RB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="9cc00-105">Définit les informations de jeu de couleurs pour le contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="9cc00-105">Sets the color scheme information for the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9cc00-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9cc00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc00-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9cc00-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9cc00-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9cc00-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9cc00-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9cc00-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cc00-110">Pointeur vers une structure [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) qui contient les informations sur le modèle de couleurs.</span><span class="sxs-lookup"><span data-stu-id="9cc00-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc00-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9cc00-111">Return value</span></span>

<span data-ttu-id="9cc00-112">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9cc00-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc00-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9cc00-113">Remarks</span></span>

<span data-ttu-id="9cc00-114">Le contrôle rebar utilise les informations de modèle de couleurs lors du dessin des éléments 3D dans le contrôle et les bandes.</span><span class="sxs-lookup"><span data-stu-id="9cc00-114">The rebar control uses the color scheme information when drawing the 3-D elements in the control and bands.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc00-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9cc00-115">Requirements</span></span>



| <span data-ttu-id="9cc00-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9cc00-116">Requirement</span></span> | <span data-ttu-id="9cc00-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9cc00-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc00-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cc00-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc00-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9cc00-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9cc00-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cc00-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc00-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9cc00-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9cc00-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9cc00-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cc00-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cc00-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cc00-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cc00-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc00-125">**\_GETCOLORSCHEME RB**</span><span class="sxs-lookup"><span data-stu-id="9cc00-125">**RB\_GETCOLORSCHEME**</span></span>](rb-getcolorscheme.md)
</dt> </dl>

 

 





