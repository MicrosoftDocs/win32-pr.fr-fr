---
title: Message DM_REPOSITION (winuser. h)
description: Repositionne une boîte de dialogue de niveau supérieur de façon à ce qu’elle s’ajuste à la zone du bureau. Une application peut envoyer ce message à une boîte de dialogue après l’avoir redimensionnée pour s’assurer que la boîte de dialogue entière reste visible.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- Boîtes de dialogue de DM_REPOSITION message
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033215"
---
# <a name="dm_reposition-message"></a><span data-ttu-id="16654-105">\_Message de repositionnement DM</span><span class="sxs-lookup"><span data-stu-id="16654-105">DM\_REPOSITION message</span></span>

<span data-ttu-id="16654-106">Repositionne une boîte de dialogue de niveau supérieur de façon à ce qu’elle s’ajuste à la zone du bureau.</span><span class="sxs-lookup"><span data-stu-id="16654-106">Repositions a top-level dialog box so that it fits within the desktop area.</span></span> <span data-ttu-id="16654-107">Une application peut envoyer ce message à une boîte de dialogue après l’avoir redimensionnée pour s’assurer que la boîte de dialogue entière reste visible.</span><span class="sxs-lookup"><span data-stu-id="16654-107">An application can send this message to a dialog box after resizing it to ensure that the entire dialog box remains visible.</span></span>


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="16654-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16654-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16654-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16654-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16654-110">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="16654-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="16654-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16654-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16654-112">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="16654-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16654-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16654-113">Return value</span></span>

<span data-ttu-id="16654-114">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="16654-114">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16654-115">Notes</span><span class="sxs-lookup"><span data-stu-id="16654-115">Remarks</span></span>

<span data-ttu-id="16654-116">Ce message n’a aucun effet si la boîte de dialogue est une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="16654-116">This message has no effect if the dialog box is a child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="16654-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16654-117">Requirements</span></span>



| <span data-ttu-id="16654-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16654-118">Requirement</span></span> | <span data-ttu-id="16654-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="16654-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16654-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16654-120">Minimum supported client</span></span><br/> | <span data-ttu-id="16654-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16654-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="16654-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16654-122">Minimum supported server</span></span><br/> | <span data-ttu-id="16654-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16654-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="16654-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="16654-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="16654-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16654-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16654-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16654-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16654-127">Vue d'ensemble des boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="16654-127">Dialog Boxes Overview</span></span>](dialog-boxes.md)
</dt> </dl>

 

 





