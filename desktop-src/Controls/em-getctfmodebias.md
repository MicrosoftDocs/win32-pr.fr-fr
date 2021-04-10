---
title: Message EM_GETCTFMODEBIAS (RichEdit. h)
description: Obtient les valeurs de décalage du mode Text Services Framework pour un contrôle RichEdit Microsoft.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- EM_GETCTFMODEBIAS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104041"
---
# <a name="em_getctfmodebias-message"></a><span data-ttu-id="cb4ff-104">\_Message GETCTFMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="cb4ff-104">EM\_GETCTFMODEBIAS message</span></span>

<span data-ttu-id="cb4ff-105">Obtient les valeurs de décalage du mode Text Services Framework pour un contrôle RichEdit Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cb4ff-105">Gets the Text Services Framework mode bias values for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb4ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb4ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb4ff-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb4ff-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb4ff-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cb4ff-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cb4ff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb4ff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb4ff-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cb4ff-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb4ff-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb4ff-111">Return value</span></span>

<span data-ttu-id="cb4ff-112">Valeur de décalage en mode Text Services Framework actuelle.</span><span class="sxs-lookup"><span data-stu-id="cb4ff-112">The current Text Services Framework mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb4ff-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cb4ff-113">Remarks</span></span>

<span data-ttu-id="cb4ff-114">Pour connaître le décalage du mode IME, appelez [**em \_ GETIMEMODEBIAS**](em-getimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="cb4ff-114">To get the IME mode bias, call [**EM\_GETIMEMODEBIAS**](em-getimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4ff-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb4ff-115">Requirements</span></span>



| <span data-ttu-id="cb4ff-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb4ff-116">Requirement</span></span> | <span data-ttu-id="cb4ff-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb4ff-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4ff-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb4ff-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4ff-119">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb4ff-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb4ff-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb4ff-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4ff-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb4ff-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb4ff-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb4ff-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb4ff-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb4ff-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb4ff-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb4ff-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb4ff-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="cb4ff-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb4ff-126">**\_SETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="cb4ff-126">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="cb4ff-127">**\_GETIMEMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="cb4ff-127">**EM\_GETIMEMODEBIAS**</span></span>](em-getimemodebias.md)
</dt> </dl>

 

 





