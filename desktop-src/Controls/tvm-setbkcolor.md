---
title: Message TVM_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetBkColor TreeView.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- TVM_SETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843782"
---
# <a name="tvm_setbkcolor-message"></a><span data-ttu-id="4a7fb-105">TVM \_ SETBKCOLOR message</span><span class="sxs-lookup"><span data-stu-id="4a7fb-105">TVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="4a7fb-106">Définit la couleur d’arrière-plan du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-106">Sets the background color of the control.</span></span> <span data-ttu-id="4a7fb-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetBkColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="4a7fb-107">You can send this message explicitly or by using the [**TreeView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a7fb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a7fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a7fb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a7fb-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4a7fb-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4a7fb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a7fb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a7fb-112">Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui contient la nouvelle couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new background color.</span></span> <span data-ttu-id="4a7fb-113">Si cette valeur est-1, le contrôle revient à l’utilisation de la couleur système pour la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-113">If this value is -1, the control will revert to using the system color for the background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a7fb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a7fb-114">Return value</span></span>

<span data-ttu-id="4a7fb-115">Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur d’arrière-plan précédente.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-115">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous background color.</span></span> <span data-ttu-id="4a7fb-116">Si cette valeur est-1, le contrôle utilisait la couleur système pour la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="4a7fb-116">If this value is -1, the control was using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a7fb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a7fb-117">Requirements</span></span>



| <span data-ttu-id="4a7fb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a7fb-118">Requirement</span></span> | <span data-ttu-id="4a7fb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a7fb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a7fb-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a7fb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a7fb-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a7fb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a7fb-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a7fb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a7fb-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a7fb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a7fb-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a7fb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a7fb-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a7fb-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a7fb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a7fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a7fb-127">**TVM \_ GETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4a7fb-127">**TVM\_GETBKCOLOR**</span></span>](tvm-getbkcolor.md)
</dt> </dl>

 

