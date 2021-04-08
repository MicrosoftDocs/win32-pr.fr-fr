---
title: Message TVM_SETTEXTCOLOR (commctrl. h)
description: Définit la couleur du texte du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetTextColor TreeView.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- TVM_SETTEXTCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741997"
---
# <a name="tvm_settextcolor-message"></a><span data-ttu-id="e1402-105">TVM \_ SETTEXTCOLOR message</span><span class="sxs-lookup"><span data-stu-id="e1402-105">TVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="e1402-106">Définit la couleur du texte du contrôle.</span><span class="sxs-lookup"><span data-stu-id="e1402-106">Sets the text color of the control.</span></span> <span data-ttu-id="e1402-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetTextColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) .</span><span class="sxs-lookup"><span data-stu-id="e1402-107">You can send this message explicitly or by using the [**TreeView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1402-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1402-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1402-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1402-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e1402-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e1402-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e1402-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1402-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1402-112">Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui contient la nouvelle couleur de texte.</span><span class="sxs-lookup"><span data-stu-id="e1402-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new text color.</span></span> <span data-ttu-id="e1402-113">Si cet argument a la valeur-1, le contrôle revient à l’utilisation de la couleur système pour la couleur du texte.</span><span class="sxs-lookup"><span data-stu-id="e1402-113">If this argument is -1, the control will revert to using the system color for the text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1402-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1402-114">Return value</span></span>

<span data-ttu-id="e1402-115">Retourne une valeur **COLORREF** qui représente la couleur de texte précédente.</span><span class="sxs-lookup"><span data-stu-id="e1402-115">Returns a **COLORREF** value that represents the previous text color.</span></span> <span data-ttu-id="e1402-116">Si cette valeur est-1, le contrôle utilisait la couleur système pour la couleur du texte.</span><span class="sxs-lookup"><span data-stu-id="e1402-116">If this value is -1, the control was using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1402-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1402-117">Requirements</span></span>



| <span data-ttu-id="e1402-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1402-118">Requirement</span></span> | <span data-ttu-id="e1402-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1402-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1402-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1402-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e1402-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1402-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1402-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1402-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e1402-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1402-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1402-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1402-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1402-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1402-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1402-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1402-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1402-127">**TVM \_ GETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="e1402-127">**TVM\_GETTEXTCOLOR**</span></span>](tvm-gettextcolor.md)
</dt> </dl>

 

