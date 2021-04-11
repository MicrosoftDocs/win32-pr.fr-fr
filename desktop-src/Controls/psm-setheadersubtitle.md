---
title: Message PSM_SETHEADERSUBTITLE (Prsht. h)
description: Définit le texte du sous-titre de l’en-tête de la page intérieure d’un Assistant. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet SetHeaderSubTitle.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- PSM_SETHEADERSUBTITLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942067"
---
# <a name="psm_setheadersubtitle-message"></a><span data-ttu-id="fb3cd-105">\_Message PSM SETHEADERSUBTITLE</span><span class="sxs-lookup"><span data-stu-id="fb3cd-105">PSM\_SETHEADERSUBTITLE message</span></span>

<span data-ttu-id="fb3cd-106">Définit le texte du sous-titre de l’en-tête de la page intérieure d’un Assistant.</span><span class="sxs-lookup"><span data-stu-id="fb3cd-106">Sets the subtitle text for the header of a wizard's interior page.</span></span> <span data-ttu-id="fb3cd-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .</span><span class="sxs-lookup"><span data-stu-id="fb3cd-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb3cd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb3cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb3cd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb3cd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb3cd-110">Index de base zéro de la page de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="fb3cd-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="fb3cd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb3cd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb3cd-112">Nouveau sous-titre d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="fb3cd-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb3cd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb3cd-113">Return value</span></span>

<span data-ttu-id="fb3cd-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="fb3cd-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb3cd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fb3cd-115">Remarks</span></span>

<span data-ttu-id="fb3cd-116">Si vous spécifiez la page actuelle, elle est immédiatement repeinte pour afficher le nouveau sous-titre.</span><span class="sxs-lookup"><span data-stu-id="fb3cd-116">If you specify the current page, it will immediately be repainted to display the new subtitle.</span></span>

> [!Note]  
> <span data-ttu-id="fb3cd-117">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="fb3cd-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb3cd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb3cd-118">Requirements</span></span>



| <span data-ttu-id="fb3cd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb3cd-119">Requirement</span></span> | <span data-ttu-id="fb3cd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb3cd-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3cd-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb3cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fb3cd-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb3cd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fb3cd-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb3cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fb3cd-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb3cd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb3cd-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb3cd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb3cd-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb3cd-126"><dt>Prsht.h</dt></span></span> </dl>      |
| <span data-ttu-id="fb3cd-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="fb3cd-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fb3cd-128">**PSM \_ SETHEADERSUBTITLEW** (Unicode) et **PSM \_ SETHEADERSUBTITLEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fb3cd-128">**PSM\_SETHEADERSUBTITLEW** (Unicode) and **PSM\_SETHEADERSUBTITLEA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb3cd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb3cd-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="fb3cd-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="fb3cd-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fb3cd-131">**\_HWNDTOINDEX PSM**</span><span class="sxs-lookup"><span data-stu-id="fb3cd-131">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="fb3cd-132">**\_IDTOINDEX PSM**</span><span class="sxs-lookup"><span data-stu-id="fb3cd-132">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="fb3cd-133">**\_PAGETOINDEX PSM**</span><span class="sxs-lookup"><span data-stu-id="fb3cd-133">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





