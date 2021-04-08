---
title: Message BM_SETSTYLE (winuser. h)
description: Définit le style d’un bouton. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro Button SetStyle.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941851"
---
# <a name="bm_setstyle-message"></a><span data-ttu-id="a46b5-105">\_Message BM SETSTYLE</span><span class="sxs-lookup"><span data-stu-id="a46b5-105">BM\_SETSTYLE message</span></span>

<span data-ttu-id="a46b5-106">Définit le style d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="a46b5-106">Sets the style of a button.</span></span> <span data-ttu-id="a46b5-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**Button \_ SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) .</span><span class="sxs-lookup"><span data-stu-id="a46b5-107">You can send this message explicitly or use the [**Button\_SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a46b5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a46b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a46b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a46b5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a46b5-110">Style du bouton.</span><span class="sxs-lookup"><span data-stu-id="a46b5-110">The button style.</span></span> <span data-ttu-id="a46b5-111">Ce paramètre peut être une combinaison de styles de bouton.</span><span class="sxs-lookup"><span data-stu-id="a46b5-111">This parameter can be a combination of button styles.</span></span> <span data-ttu-id="a46b5-112">Pour obtenir un tableau de styles de bouton, consultez [styles de bouton](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="a46b5-112">For a table of button styles, see [Button Styles](button-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a46b5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a46b5-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a46b5-114">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* est un **booléen** qui spécifie si le bouton doit être redessiné.</span><span class="sxs-lookup"><span data-stu-id="a46b5-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* is a **BOOL** that specifies whether the button is to be redrawn.</span></span> <span data-ttu-id="a46b5-115">La valeur **true** redessine le bouton. la valeur **false** ne redessine pas le bouton.</span><span class="sxs-lookup"><span data-stu-id="a46b5-115">A value of **TRUE** redraws the button; a value of **FALSE** does not redraw the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a46b5-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a46b5-116">Return value</span></span>

<span data-ttu-id="a46b5-117">Ce message retourne toujours la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="a46b5-117">This message always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a46b5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a46b5-118">Requirements</span></span>



| <span data-ttu-id="a46b5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a46b5-119">Requirement</span></span> | <span data-ttu-id="a46b5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a46b5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a46b5-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a46b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a46b5-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a46b5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a46b5-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a46b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a46b5-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a46b5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a46b5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a46b5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a46b5-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a46b5-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

