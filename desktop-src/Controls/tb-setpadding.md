---
title: Message TB_SETPADDING (commctrl. h)
description: Définit la marge intérieure d’un contrôle de barre d’outils.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- TB_SETPADDING les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105751"
---
# <a name="tb_setpadding-message"></a><span data-ttu-id="53276-104">TO \_ SETPADDING message</span><span class="sxs-lookup"><span data-stu-id="53276-104">TB\_SETPADDING message</span></span>

<span data-ttu-id="53276-105">Définit la marge intérieure d’un contrôle de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="53276-105">Sets the padding for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="53276-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53276-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53276-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53276-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53276-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="53276-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="53276-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53276-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53276-110">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la marge intérieure horizontale, en pixels.</span><span class="sxs-lookup"><span data-stu-id="53276-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the horizontal padding, in pixels.</span></span> <span data-ttu-id="53276-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le remplissage vertical, en pixels.</span><span class="sxs-lookup"><span data-stu-id="53276-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53276-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53276-112">Return value</span></span>

<span data-ttu-id="53276-113">Retourne une valeur **DWORD** qui contient le remplissage horizontal précédent dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et le remplissage vertical précédent dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), en pixels.</span><span class="sxs-lookup"><span data-stu-id="53276-113">Returns a **DWORD** value that contains the previous horizontal padding in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous vertical padding in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="53276-114">Notes</span><span class="sxs-lookup"><span data-stu-id="53276-114">Remarks</span></span>

<span data-ttu-id="53276-115">Les valeurs de remplissage sont utilisées pour créer une zone vide entre le bord du bouton et l’image et/ou le texte du bouton.</span><span class="sxs-lookup"><span data-stu-id="53276-115">The padding values are used to create a blank area between the edge of the button and the button's image and/or text.</span></span> <span data-ttu-id="53276-116">L’emplacement et la quantité de remplissage réellement appliqués dépendent du type du bouton et de la présence ou non d’une image.</span><span class="sxs-lookup"><span data-stu-id="53276-116">Where and how much padding is actually applied depends on the type of the button and whether it has an image.</span></span> <span data-ttu-id="53276-117">Le remplissage horizontal est appliqué à droite et à gauche du bouton, et le remplissage vertical est appliqué à la fois au haut et au bas du bouton.</span><span class="sxs-lookup"><span data-stu-id="53276-117">The horizontal padding is applied to both the right and left of the button, and the vertical padding is applied to both the top and bottom of the button.</span></span> <span data-ttu-id="53276-118">Le remplissage est appliqué uniquement aux boutons qui ont le style de [**\_ redimensionnement automatique TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="53276-118">Padding is only applied to buttons that have the [**TBSTYLE\_AUTOSIZE**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="53276-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53276-119">Requirements</span></span>



| <span data-ttu-id="53276-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53276-120">Requirement</span></span> | <span data-ttu-id="53276-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="53276-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53276-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53276-122">Minimum supported client</span></span><br/> | <span data-ttu-id="53276-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53276-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53276-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53276-124">Minimum supported server</span></span><br/> | <span data-ttu-id="53276-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53276-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53276-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="53276-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="53276-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53276-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53276-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53276-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53276-129">**TO \_ GETPADDING**</span><span class="sxs-lookup"><span data-stu-id="53276-129">**TB\_GETPADDING**</span></span>](tb-getpadding.md)
</dt> </dl>

 

