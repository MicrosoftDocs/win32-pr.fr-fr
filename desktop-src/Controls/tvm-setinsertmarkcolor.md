---
title: Message TVM_SETINSERTMARKCOLOR (commctrl. h)
description: Définit la couleur utilisée pour dessiner la marque d’insertion pour l’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SetInsertMarkColor TreeView.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- TVM_SETINSERTMARKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104176"
---
# <a name="tvm_setinsertmarkcolor-message"></a><span data-ttu-id="0d5b6-105">TVM \_ SETINSERTMARKCOLOR message</span><span class="sxs-lookup"><span data-stu-id="0d5b6-105">TVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="0d5b6-106">Définit la couleur utilisée pour dessiner la marque d’insertion pour l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="0d5b6-106">Sets the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="0d5b6-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SetInsertMarkColor TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) .</span><span class="sxs-lookup"><span data-stu-id="0d5b6-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d5b6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d5b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d5b6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d5b6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0d5b6-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0d5b6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0d5b6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d5b6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d5b6-112">Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui contient la nouvelle couleur de la marque d’insertion.</span><span class="sxs-lookup"><span data-stu-id="0d5b6-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d5b6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d5b6-113">Return value</span></span>

<span data-ttu-id="0d5b6-114">Retourne une valeur **COLORREF** qui contient la couleur de la marque d’insertion précédente.</span><span class="sxs-lookup"><span data-stu-id="0d5b6-114">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d5b6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d5b6-115">Requirements</span></span>



| <span data-ttu-id="0d5b6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d5b6-116">Requirement</span></span> | <span data-ttu-id="0d5b6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d5b6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5b6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d5b6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0d5b6-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d5b6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d5b6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d5b6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0d5b6-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d5b6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d5b6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d5b6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d5b6-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d5b6-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d5b6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d5b6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5b6-125">**TVM \_ GETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="0d5b6-125">**TVM\_GETINSERTMARKCOLOR**</span></span>](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

