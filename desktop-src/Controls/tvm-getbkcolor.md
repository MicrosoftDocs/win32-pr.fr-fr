---
title: Message TVM_GETBKCOLOR (commctrl. h)
description: Récupère la couleur d’arrière-plan actuelle du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetBkColor TreeView.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- TVM_GETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512599"
---
# <a name="tvm_getbkcolor-message"></a><span data-ttu-id="f1d93-105">TVM \_ GETBKCOLOR message</span><span class="sxs-lookup"><span data-stu-id="f1d93-105">TVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="f1d93-106">Récupère la couleur d’arrière-plan actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1d93-106">Retrieves the current background color of the control.</span></span> <span data-ttu-id="f1d93-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetBkColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="f1d93-107">You can send this message explicitly or by using the [**TreeView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1d93-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1d93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1d93-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1d93-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f1d93-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f1d93-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f1d93-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1d93-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f1d93-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f1d93-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1d93-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1d93-113">Return value</span></span>

<span data-ttu-id="f1d93-114">Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur d’arrière-plan actuelle.</span><span class="sxs-lookup"><span data-stu-id="f1d93-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current background color.</span></span> <span data-ttu-id="f1d93-115">Si cette valeur est-1, le contrôle utilise la couleur système pour la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f1d93-115">If this value is -1, the control is using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1d93-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1d93-116">Requirements</span></span>



| <span data-ttu-id="f1d93-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1d93-117">Requirement</span></span> | <span data-ttu-id="f1d93-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1d93-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d93-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1d93-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f1d93-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1d93-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1d93-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1d93-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f1d93-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1d93-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1d93-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1d93-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1d93-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1d93-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1d93-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1d93-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d93-126">**TVM \_ SETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="f1d93-126">**TVM\_SETBKCOLOR**</span></span>](tvm-setbkcolor.md)
</dt> </dl>

 

