---
title: Message PSM_CANCELTOCLOSE (Prsht. h)
description: Envoyé par une application lorsqu’elle a effectué des modifications depuis la dernière \_ notification d’application PSN qui ne peut pas être annulée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet CancelToClose.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- PSM_CANCELTOCLOSE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105277"
---
# <a name="psm_canceltoclose-message"></a><span data-ttu-id="82374-105">\_Message PSM CANCELTOCLOSE</span><span class="sxs-lookup"><span data-stu-id="82374-105">PSM\_CANCELTOCLOSE message</span></span>

<span data-ttu-id="82374-106">Envoyé par une application lorsqu’elle a effectué des modifications depuis la dernière notification d' [ \_ application PSN](psn-apply.md) qui ne peut pas être annulée.</span><span class="sxs-lookup"><span data-stu-id="82374-106">Sent by an application when it has performed changes since the most recent [PSN\_APPLY](psn-apply.md) notification that cannot be canceled.</span></span> <span data-ttu-id="82374-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .</span><span class="sxs-lookup"><span data-stu-id="82374-107">You can send this message explicitly or by using the [**PropSheet\_CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="82374-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82374-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82374-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82374-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82374-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="82374-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="82374-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82374-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82374-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="82374-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82374-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82374-113">Return value</span></span>

<span data-ttu-id="82374-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="82374-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82374-115">Notes</span><span class="sxs-lookup"><span data-stu-id="82374-115">Remarks</span></span>

<span data-ttu-id="82374-116">**PSM \_ CANCELTOCLOSE** désactive le bouton **Annuler** et remplace le texte du bouton **OK** par « fermer ».</span><span class="sxs-lookup"><span data-stu-id="82374-116">**PSM\_CANCELTOCLOSE** disables the **Cancel** button and changes the text of the **OK** button to "Close".</span></span>

<span data-ttu-id="82374-117">La plupart des feuilles de propriétés attendent d’effectuer des modifications irréversibles jusqu’à la réception d’une \_ notification d’application PSN.</span><span class="sxs-lookup"><span data-stu-id="82374-117">Most property sheets wait to perform irreversible changes until a PSN\_APPLY notification is received.</span></span> <span data-ttu-id="82374-118">Toutefois, dans certains cas, une feuille de propriétés peut apporter des modifications irréversibles en dehors de la \_ séquence de réinitialisation PSN Apply/PSN standard \_ .</span><span class="sxs-lookup"><span data-stu-id="82374-118">However, in some circumstances, a property sheet may make irreversible changes outside the standard PSN\_APPLY/PSN\_RESET sequence.</span></span> <span data-ttu-id="82374-119">Par exemple, une feuille de propriétés qui contient un bouton **modifier** utilisé pour afficher une boîte de dialogue de sous-boîte de dialogue pour la modification d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="82374-119">One example is a property sheet that contains an **Edit** button that is used to display a subdialog box for editing a property.</span></span> <span data-ttu-id="82374-120">Quand l’utilisateur clique sur **OK** pour envoyer la modification, la page de la feuille de propriétés comporte plusieurs options.</span><span class="sxs-lookup"><span data-stu-id="82374-120">When the user clicks **OK** to submit the change, the property sheet page has several options.</span></span>

-   <span data-ttu-id="82374-121">Il peut enregistrer les modifications, mais attendre qu’il reçoive une \_ notification d’application PSN pour les appliquer.</span><span class="sxs-lookup"><span data-stu-id="82374-121">It can record the changes, but wait until it receives a PSN\_APPLY notification to apply them.</span></span> <span data-ttu-id="82374-122">Il s’agit de l’approche privilégiée.</span><span class="sxs-lookup"><span data-stu-id="82374-122">This is the preferred approach.</span></span>
-   <span data-ttu-id="82374-123">Il peut appliquer les modifications immédiatement après avoir quitté la boîte de dialogue, mais conserver les paramètres d’origine.</span><span class="sxs-lookup"><span data-stu-id="82374-123">It can apply the changes immediately after exiting the subdialog box, but remember the original settings.</span></span> <span data-ttu-id="82374-124">Ces paramètres peuvent être utilisés pour restaurer l’état d’origine si une \_ notification de réinitialisation de PSN est reçue.</span><span class="sxs-lookup"><span data-stu-id="82374-124">Those settings can be used to restore the original state if a PSN\_RESET notification is received.</span></span>
-   <span data-ttu-id="82374-125">Il peut appliquer les modifications immédiatement et ne pas tenter de restaurer les paramètres d’origine lorsqu’il reçoit une notification de [ \_ réinitialisation PSN](psn-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="82374-125">It can apply the changes immediately and not attempt to restore the original settings when it receives a [PSN\_RESET](psn-reset.md) notification.</span></span> <span data-ttu-id="82374-126">Cette approche n’est pas recommandée, mais elle peut s’avérer nécessaire si les modifications sont trop éloignées pour que les deux autres options soient pratiques.</span><span class="sxs-lookup"><span data-stu-id="82374-126">This approach is not recommended, but may be necessary if the changes are too far-reaching for the other two options to be practical.</span></span>

<span data-ttu-id="82374-127">Pour la troisième option, les applications doivent envoyer un message **\_ CANCELTOCLOSE PSM** à la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="82374-127">For the third option, applications should send a **PSM\_CANCELTOCLOSE** message to the property sheet.</span></span> <span data-ttu-id="82374-128">Elle indique à l’utilisateur que les modifications apportées à la sous-boîte de dialogue ne peuvent pas être inversées en cliquant sur le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="82374-128">It indicates to the user that the changes made with the subdialog box cannot be reversed by clicking the **Cancel** button.</span></span>

> [!Note]  
> <span data-ttu-id="82374-129">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="82374-129">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="82374-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82374-130">Requirements</span></span>



| <span data-ttu-id="82374-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82374-131">Requirement</span></span> | <span data-ttu-id="82374-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="82374-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82374-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82374-133">Minimum supported client</span></span><br/> | <span data-ttu-id="82374-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82374-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="82374-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82374-135">Minimum supported server</span></span><br/> | <span data-ttu-id="82374-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82374-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="82374-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="82374-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="82374-138"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="82374-138"><dt>Prsht.h</dt></span></span> </dl> |



 

 





