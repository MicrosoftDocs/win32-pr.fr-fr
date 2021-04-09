---
title: Message TVM_GETTEXTCOLOR (commctrl. h)
description: Récupère la couleur de texte actuelle du contrôle. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetTextColor TreeView.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- TVM_GETTEXTCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032603"
---
# <a name="tvm_gettextcolor-message"></a><span data-ttu-id="dcb66-105">TVM \_ GETTEXTCOLOR message</span><span class="sxs-lookup"><span data-stu-id="dcb66-105">TVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="dcb66-106">Récupère la couleur de texte actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="dcb66-106">Retrieves the current text color of the control.</span></span> <span data-ttu-id="dcb66-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetTextColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) .</span><span class="sxs-lookup"><span data-stu-id="dcb66-107">You can send this message explicitly or by using the [**TreeView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dcb66-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcb66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcb66-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dcb66-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dcb66-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dcb66-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dcb66-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dcb66-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dcb66-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dcb66-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcb66-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcb66-113">Return value</span></span>

<span data-ttu-id="dcb66-114">Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur du texte actuel.</span><span class="sxs-lookup"><span data-stu-id="dcb66-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current text color.</span></span> <span data-ttu-id="dcb66-115">Si cette valeur est-1, le contrôle utilise la couleur système pour la couleur du texte.</span><span class="sxs-lookup"><span data-stu-id="dcb66-115">If this value is -1, the control is using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcb66-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcb66-116">Requirements</span></span>



| <span data-ttu-id="dcb66-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcb66-117">Requirement</span></span> | <span data-ttu-id="dcb66-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcb66-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb66-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcb66-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb66-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcb66-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dcb66-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcb66-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb66-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcb66-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dcb66-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcb66-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcb66-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcb66-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcb66-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcb66-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb66-126">**TVM \_ SETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="dcb66-126">**TVM\_SETTEXTCOLOR**</span></span>](tvm-settextcolor.md)
</dt> </dl>

 

