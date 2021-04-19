---
title: Message RB_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan par défaut d’un contrôle rebar.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- RB_SETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106531617"
---
# <a name="rb_setbkcolor-message"></a><span data-ttu-id="7199a-104">\_Message SETBKCOLOR RB</span><span class="sxs-lookup"><span data-stu-id="7199a-104">RB\_SETBKCOLOR message</span></span>

<span data-ttu-id="7199a-105">Définit la couleur d’arrière-plan par défaut d’un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="7199a-105">Sets a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="7199a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7199a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7199a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7199a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7199a-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7199a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7199a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7199a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7199a-110">Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la nouvelle couleur d’arrière-plan par défaut.</span><span class="sxs-lookup"><span data-stu-id="7199a-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7199a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7199a-111">Return value</span></span>

<span data-ttu-id="7199a-112">Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur d’arrière-plan par défaut précédente.</span><span class="sxs-lookup"><span data-stu-id="7199a-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="7199a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7199a-113">Remarks</span></span>

<span data-ttu-id="7199a-114">La couleur d’arrière-plan par défaut du contrôle rebar est utilisée pour dessiner l’arrière-plan dans un contrôle rebar et toutes les bandes ajoutées après l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="7199a-114">The rebar control's default background color is used to draw the background in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="7199a-115">La couleur d’arrière-plan par défaut pour une bande particulière peut être remplacée lorsqu’une bande est ajoutée ou modifiée en définissant l' \_ indicateur de couleurs RBBIM dans **fmask** et en définissant **ClrBack** dans la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .</span><span class="sxs-lookup"><span data-stu-id="7199a-115">The default background color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

<span data-ttu-id="7199a-116">Lorsque les styles visuels sont activés, ce message n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="7199a-116">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="7199a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7199a-117">Requirements</span></span>



| <span data-ttu-id="7199a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7199a-118">Requirement</span></span> | <span data-ttu-id="7199a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7199a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7199a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7199a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7199a-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7199a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7199a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7199a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7199a-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7199a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7199a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7199a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7199a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7199a-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7199a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7199a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7199a-127">**\_GETBKCOLOR RB**</span><span class="sxs-lookup"><span data-stu-id="7199a-127">**RB\_GETBKCOLOR**</span></span>](rb-getbkcolor.md)
</dt> </dl>

 

