---
title: Message TB_SETCOLORSCHEME (commctrl. h)
description: Définit les informations de jeu de couleurs pour le contrôle ToolBar.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- TB_SETCOLORSCHEME les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844265"
---
# <a name="tb_setcolorscheme-message"></a><span data-ttu-id="93902-104">TO \_ SETCOLORSCHEME message</span><span class="sxs-lookup"><span data-stu-id="93902-104">TB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="93902-105">Définit les informations de jeu de couleurs pour le contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="93902-105">Sets the color scheme information for the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="93902-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93902-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93902-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93902-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="93902-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="93902-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="93902-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93902-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93902-110">Pointeur vers une structure [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) qui contient les informations sur le modèle de couleurs.</span><span class="sxs-lookup"><span data-stu-id="93902-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93902-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93902-111">Return value</span></span>

<span data-ttu-id="93902-112">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="93902-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="93902-113">Notes</span><span class="sxs-lookup"><span data-stu-id="93902-113">Remarks</span></span>

<span data-ttu-id="93902-114">Le contrôle ToolBar utilise les informations de jeu de couleurs lors du dessin des éléments 3D dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="93902-114">The toolbar control uses the color scheme information when drawing the 3-D elements in the control.</span></span>

<span data-ttu-id="93902-115">Lorsque les styles visuels sont activés, ce message n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="93902-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="93902-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93902-116">Requirements</span></span>



| <span data-ttu-id="93902-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93902-117">Requirement</span></span> | <span data-ttu-id="93902-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="93902-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93902-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93902-119">Minimum supported client</span></span><br/> | <span data-ttu-id="93902-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93902-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93902-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93902-121">Minimum supported server</span></span><br/> | <span data-ttu-id="93902-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93902-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93902-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="93902-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="93902-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="93902-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93902-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93902-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93902-126">**TO \_ GETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="93902-126">**TB\_GETCOLORSCHEME**</span></span>](tb-getcolorscheme.md)
</dt> </dl>

 

 





