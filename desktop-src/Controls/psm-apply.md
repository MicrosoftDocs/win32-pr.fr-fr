---
title: Message PSM_APPLY (Prsht. h)
description: Simule la sélection du bouton appliquer, indiquant qu’une ou plusieurs pages ont été modifiées et que les modifications doivent être validées et enregistrées.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- PSM_APPLY les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844029"
---
# <a name="psm_apply-message"></a><span data-ttu-id="c5c62-104">\_Message d’application PSM</span><span class="sxs-lookup"><span data-stu-id="c5c62-104">PSM\_APPLY message</span></span>

<span data-ttu-id="c5c62-105">Simule la sélection du bouton **appliquer** , indiquant qu’une ou plusieurs pages ont été modifiées et que les modifications doivent être validées et enregistrées.</span><span class="sxs-lookup"><span data-stu-id="c5c62-105">Simulates the selection of the **Apply** button, indicating that one or more pages have changed and the changes need to be validated and recorded.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5c62-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5c62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5c62-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5c62-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5c62-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c5c62-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c5c62-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5c62-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5c62-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c5c62-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5c62-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5c62-111">Return value</span></span>

<span data-ttu-id="c5c62-112">Retourne la **valeur true** si toutes les pages ont correctement appliqué les modifications, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c5c62-112">Returns **TRUE** if all pages successfully applied the changes, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5c62-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c5c62-113">Remarks</span></span>

<span data-ttu-id="c5c62-114">La feuille de propriétés envoie le code de notification [PSN \_ KILLACTIVE](psn-killactive.md) à la page actuelle.</span><span class="sxs-lookup"><span data-stu-id="c5c62-114">The property sheet sends the [PSN\_KILLACTIVE](psn-killactive.md) notification code to the current page.</span></span> <span data-ttu-id="c5c62-115">Si la page active retourne la **valeur false**, la feuille de propriétés envoie le code de notification d' [ \_ application PSN](psn-apply.md) à toutes les pages actives.</span><span class="sxs-lookup"><span data-stu-id="c5c62-115">If the current page returns **FALSE**, the property sheet sends the [PSN\_APPLY](psn-apply.md) notification code to all active pages.</span></span> <span data-ttu-id="c5c62-116">Vous pouvez envoyer le \_ message d’application PSM de manière explicite ou à l’aide de la macro [**PropSheet \_ apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) .</span><span class="sxs-lookup"><span data-stu-id="c5c62-116">You can send the PSM\_APPLY message explicitly or by using the [**PropSheet\_Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) macro.</span></span>

> [!Note]  
> <span data-ttu-id="c5c62-117">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="c5c62-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c5c62-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5c62-118">Requirements</span></span>



| <span data-ttu-id="c5c62-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5c62-119">Requirement</span></span> | <span data-ttu-id="c5c62-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5c62-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c62-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5c62-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c62-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5c62-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c5c62-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5c62-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c62-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5c62-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c5c62-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5c62-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5c62-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5c62-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





