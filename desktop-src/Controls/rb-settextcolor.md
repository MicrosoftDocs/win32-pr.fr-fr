---
title: Message RB_SETTEXTCOLOR (commctrl. h)
description: Définit la couleur de texte par défaut d’un contrôle rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- RB_SETTEXTCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466070"
---
# <a name="rb_settextcolor-message"></a><span data-ttu-id="e7283-104">\_Message SETTEXTCOLOR RB</span><span class="sxs-lookup"><span data-stu-id="e7283-104">RB\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="e7283-105">Définit la couleur de texte par défaut d’un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="e7283-105">Sets a rebar control's default text color.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7283-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7283-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7283-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7283-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e7283-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e7283-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e7283-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7283-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7283-110">Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la nouvelle couleur de texte par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7283-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7283-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7283-111">Return value</span></span>

<span data-ttu-id="e7283-112">Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur de texte par défaut précédente.</span><span class="sxs-lookup"><span data-stu-id="e7283-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7283-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e7283-113">Remarks</span></span>

<span data-ttu-id="e7283-114">La couleur de texte par défaut du contrôle rebar est utilisée pour dessiner le texte dans un contrôle rebar et toutes les bandes ajoutées après l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="e7283-114">The rebar control's default text color is used to draw the text in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="e7283-115">La couleur de texte par défaut pour une bande particulière peut être remplacée lorsqu’une bande est ajoutée ou modifiée en définissant l' \_ indicateur de couleurs RBBIM dans **fmask** et en définissant **ClrBack** dans la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .</span><span class="sxs-lookup"><span data-stu-id="e7283-115">The default text color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7283-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7283-116">Requirements</span></span>



| <span data-ttu-id="e7283-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7283-117">Requirement</span></span> | <span data-ttu-id="e7283-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7283-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7283-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7283-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e7283-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7283-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7283-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7283-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e7283-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7283-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7283-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7283-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7283-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7283-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7283-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7283-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7283-126">**\_GETTEXTCOLOR RB**</span><span class="sxs-lookup"><span data-stu-id="e7283-126">**RB\_GETTEXTCOLOR**</span></span>](rb-gettextcolor.md)
</dt> </dl>

 

