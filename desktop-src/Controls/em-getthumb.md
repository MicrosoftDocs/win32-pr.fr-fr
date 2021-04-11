---
title: Message EM_GETTHUMB (winuser. h)
description: Obtient la position de la case de défilement (Thumb) dans la barre de défilement verticale d’un contrôle d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- EM_GETTHUMB les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105112"
---
# <a name="em_getthumb-message"></a><span data-ttu-id="0f552-105">\_Message GETTHUMB em</span><span class="sxs-lookup"><span data-stu-id="0f552-105">EM\_GETTHUMB message</span></span>

<span data-ttu-id="0f552-106">Obtient la position de la case de défilement (Thumb) dans la barre de défilement verticale d’un contrôle d’édition multiligne.</span><span class="sxs-lookup"><span data-stu-id="0f552-106">Gets the position of the scroll box (thumb) in the vertical scroll bar of a multiline edit control.</span></span> <span data-ttu-id="0f552-107">Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.</span><span class="sxs-lookup"><span data-stu-id="0f552-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f552-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f552-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f552-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f552-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f552-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0f552-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0f552-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f552-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f552-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0f552-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f552-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f552-113">Return value</span></span>

<span data-ttu-id="0f552-114">La valeur de retour correspond à la position de la case de défilement.</span><span class="sxs-lookup"><span data-stu-id="0f552-114">The return value is the position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f552-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0f552-115">Remarks</span></span>

<span data-ttu-id="0f552-116">**Modification riche :** Pris en charge dans Microsoft Rich Edit 2,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0f552-116">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="0f552-117">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="0f552-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f552-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f552-118">Requirements</span></span>



| <span data-ttu-id="0f552-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f552-119">Requirement</span></span> | <span data-ttu-id="0f552-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f552-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f552-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f552-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f552-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f552-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0f552-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f552-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f552-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f552-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0f552-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f552-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f552-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f552-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





