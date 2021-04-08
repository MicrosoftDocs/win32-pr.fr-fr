---
title: Message TVM_GETINDENT (commctrl. h)
description: Récupère la quantité, en pixels, que les éléments enfants sont mis en retrait par rapport à leurs éléments parents. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro GetIndent TreeView.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- TVM_GETINDENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844250"
---
# <a name="tvm_getindent-message"></a><span data-ttu-id="c4547-105">TVM \_ GETINDENT message</span><span class="sxs-lookup"><span data-stu-id="c4547-105">TVM\_GETINDENT message</span></span>

<span data-ttu-id="c4547-106">Récupère la quantité, en pixels, que les éléments enfants sont mis en retrait par rapport à leurs éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c4547-106">Retrieves the amount, in pixels, that child items are indented relative to their parent items.</span></span> <span data-ttu-id="c4547-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetIndent TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) .</span><span class="sxs-lookup"><span data-stu-id="c4547-107">You can send this message explicitly or by using the [**TreeView\_GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4547-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4547-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4547-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4547-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c4547-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c4547-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c4547-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4547-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c4547-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c4547-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4547-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4547-113">Return value</span></span>

<span data-ttu-id="c4547-114">Retourne la valeur de la mise en retrait.</span><span class="sxs-lookup"><span data-stu-id="c4547-114">Returns the amount of indentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4547-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4547-115">Requirements</span></span>



| <span data-ttu-id="c4547-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4547-116">Requirement</span></span> | <span data-ttu-id="c4547-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4547-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4547-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4547-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c4547-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4547-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4547-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4547-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c4547-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4547-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4547-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4547-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4547-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4547-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





