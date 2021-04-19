---
title: Message PSM_SETHEADERTITLE (Prsht. h)
description: Définit le texte du titre de l’en-tête de la page intérieure d’un Assistant. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet SetHeaderTitle.
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- PSM_SETHEADERTITLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527154"
---
# <a name="psm_setheadertitle-message"></a><span data-ttu-id="5dedc-105">\_Message PSM SETHEADERTITLE</span><span class="sxs-lookup"><span data-stu-id="5dedc-105">PSM\_SETHEADERTITLE message</span></span>

<span data-ttu-id="5dedc-106">Définit le texte du titre de l’en-tête de la page intérieure d’un Assistant.</span><span class="sxs-lookup"><span data-stu-id="5dedc-106">Sets the title text for the header of a wizard's interior page.</span></span> <span data-ttu-id="5dedc-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .</span><span class="sxs-lookup"><span data-stu-id="5dedc-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5dedc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5dedc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dedc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5dedc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dedc-110">Index de base zéro de la page de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="5dedc-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="5dedc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5dedc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dedc-112">Nouveau sous-titre d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="5dedc-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dedc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5dedc-113">Return value</span></span>

<span data-ttu-id="5dedc-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5dedc-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dedc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5dedc-115">Remarks</span></span>

<span data-ttu-id="5dedc-116">Si vous spécifiez la page actuelle, elle est immédiatement repeinte pour afficher le nouveau titre.</span><span class="sxs-lookup"><span data-stu-id="5dedc-116">If you specify the current page, it will immediately be repainted to display the new title.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dedc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dedc-117">Requirements</span></span>



| <span data-ttu-id="5dedc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dedc-118">Requirement</span></span> | <span data-ttu-id="5dedc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dedc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5dedc-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dedc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5dedc-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dedc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5dedc-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dedc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5dedc-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5dedc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5dedc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5dedc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dedc-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dedc-125"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="5dedc-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="5dedc-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5dedc-127">**PSM \_ SETHEADERTITLEW** (Unicode) et **PSM \_ SETHEADERTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5dedc-127">**PSM\_SETHEADERTITLEW** (Unicode) and **PSM\_SETHEADERTITLEA** (ANSI)</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5dedc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dedc-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="5dedc-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5dedc-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5dedc-130">**\_HWNDTOINDEX PSM**</span><span class="sxs-lookup"><span data-stu-id="5dedc-130">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="5dedc-131">**\_IDTOINDEX PSM**</span><span class="sxs-lookup"><span data-stu-id="5dedc-131">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="5dedc-132">**\_PAGETOINDEX PSM**</span><span class="sxs-lookup"><span data-stu-id="5dedc-132">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





