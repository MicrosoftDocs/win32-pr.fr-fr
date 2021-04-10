---
title: Message EM_GETBIDIOPTIONS (RichEdit. h)
description: Indique l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- EM_GETBIDIOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104047"
---
# <a name="em_getbidioptions-message"></a><span data-ttu-id="bf76a-104">\_Message GETBIDIOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="bf76a-104">EM\_GETBIDIOPTIONS message</span></span>

<span data-ttu-id="bf76a-105">Indique l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bf76a-105">Indicates the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf76a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf76a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf76a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf76a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf76a-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="bf76a-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bf76a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf76a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf76a-110">Structure [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) qui reçoit l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bf76a-110">A [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that receives the current state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf76a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf76a-111">Return value</span></span>

<span data-ttu-id="bf76a-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bf76a-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf76a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bf76a-113">Remarks</span></span>

<span data-ttu-id="bf76a-114">Ce message définit les valeurs des membres **wMask** et **wEffects** sur la valeur de l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bf76a-114">This message sets the values of the **wMask** and **wEffects** members to the value of the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf76a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf76a-115">Requirements</span></span>



| <span data-ttu-id="bf76a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf76a-116">Requirement</span></span> | <span data-ttu-id="bf76a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf76a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf76a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf76a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf76a-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf76a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf76a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf76a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf76a-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf76a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf76a-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="bf76a-122">Redistributable</span></span><br/>          | <span data-ttu-id="bf76a-123">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="bf76a-123">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="bf76a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf76a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf76a-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf76a-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf76a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf76a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="bf76a-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="bf76a-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bf76a-128">**BIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="bf76a-128">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="bf76a-129">**\_SETBIDIOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="bf76a-129">**EM\_SETBIDIOPTIONS**</span></span>](em-setbidioptions.md)
</dt> </dl>

 

 





