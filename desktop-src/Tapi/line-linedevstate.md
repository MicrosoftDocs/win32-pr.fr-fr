---
description: Le \_ message LINEDEVSTATE de ligne TAPI est envoyé lorsque l’état d’un périphérique de ligne a changé. L’application peut appeler lineGetLineDevStatus pour déterminer le nouvel état de la ligne.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: Message LINE_LINEDEVSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537476"
---
# <a name="line_linedevstate-message"></a><span data-ttu-id="a6e45-104">\_Message LINEDEVSTATE de ligne</span><span class="sxs-lookup"><span data-stu-id="a6e45-104">LINE\_LINEDEVSTATE message</span></span>

<span data-ttu-id="a6e45-105">Le message **\_ LINEDEVSTATE de ligne** TAPI est envoyé lorsque l’état d’un périphérique de ligne a changé.</span><span class="sxs-lookup"><span data-stu-id="a6e45-105">The TAPI **LINE\_LINEDEVSTATE** message is sent when the state of a line device has changed.</span></span> <span data-ttu-id="a6e45-106">L’application peut appeler [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) pour déterminer le nouvel état de la ligne.</span><span class="sxs-lookup"><span data-stu-id="a6e45-106">The application can invoke [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) to determine the new status of the line.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="a6e45-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6e45-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6e45-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="a6e45-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a6e45-109">Handle de l’appareil de ligne.</span><span class="sxs-lookup"><span data-stu-id="a6e45-109">A handle to the line device.</span></span> <span data-ttu-id="a6e45-110">Ce paramètre est **null** lorsque *DWPARAM1* est LINEDEVSTATE \_ rein.</span><span class="sxs-lookup"><span data-stu-id="a6e45-110">This parameter is **NULL** when *dwParam1* is LINEDEVSTATE\_REINIT.</span></span>

</dd> <dt>

<span data-ttu-id="a6e45-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="a6e45-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="a6e45-112">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="a6e45-112">The callback instance supplied when opening the line.</span></span> <span data-ttu-id="a6e45-113">Si le paramètre *dwParam1* est LINEDEVSTATE \_ Réinit, le paramètre *dwCallbackInstance* n’est pas valide et a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="a6e45-113">If the *dwParam1* parameter is LINEDEVSTATE\_REINIT, the *dwCallbackInstance* parameter is not valid and is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a6e45-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a6e45-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="a6e45-115">Élément d’état de périphérique de ligne qui a changé.</span><span class="sxs-lookup"><span data-stu-id="a6e45-115">The line device status item that has changed.</span></span> <span data-ttu-id="a6e45-116">Le paramètre peut être une ou plusieurs des [**\_ constantes LINEDEVSTATE**](linedevstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="a6e45-116">The parameter can be one or more of the [**LINEDEVSTATE\_ constants**](linedevstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6e45-117">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="a6e45-117">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="a6e45-118">L’interprétation de ce paramètre dépend de la valeur de *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="a6e45-118">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="a6e45-119">Si *dwParam1* est LINEDEVSTATE \_ Ringing, *dwParam2* contient le mode Ring avec lequel le commutateur demande à la ligne de sonner.</span><span class="sxs-lookup"><span data-stu-id="a6e45-119">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam2* contains the ring mode with which the switch instructs the line to ring.</span></span> <span data-ttu-id="a6e45-120">Les modes Ring valides sont des nombres compris dans la plage **dwNumRingModes**, où **dwNumRingModes** est une fonctionnalité de périphérique en ligne.</span><span class="sxs-lookup"><span data-stu-id="a6e45-120">Valid ring modes are numbers in the range one to **dwNumRingModes**, where **dwNumRingModes** is a line device capability.</span></span>

<span data-ttu-id="a6e45-121">Si *dwParam1* est LINEDEVSTATE \_ Réinit et que le message a été émis par l’interface TAPI suite à la traduction d’un nouveau message d’API en message de réinitialisation, *DwParam2* contient le paramètre *dwMsg* du message d’origine (par exemple, [**line \_ Create**](line-create.md) ou Line \_ LINEDEVSTATE).</span><span class="sxs-lookup"><span data-stu-id="a6e45-121">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam2* contains the *dwMsg* parameter of the original message (for example, [**LINE\_CREATE**](line-create.md) or LINE\_LINEDEVSTATE).</span></span> <span data-ttu-id="a6e45-122">Si *dwParam2* est égal à zéro, cela indique que le message de réinitialisation est un message de réinitialisation « réel » qui oblige l’application à appeler [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) au plus tôt.</span><span class="sxs-lookup"><span data-stu-id="a6e45-122">If *dwParam2* is zero, this indicates that the REINIT message is a "real" REINIT message that requires the application to call [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) at its earliest convenience.</span></span>

</dd> <dt>

<span data-ttu-id="a6e45-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="a6e45-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="a6e45-124">L’interprétation de ce paramètre dépend de la valeur de *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="a6e45-124">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="a6e45-125">Si *dwParam1* est LINEDEVSTATE \_ Ringing, *dwParam3* contient le nombre de sonneries pour cet événement Ring.</span><span class="sxs-lookup"><span data-stu-id="a6e45-125">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam3* contains the ring count for this ring event.</span></span> <span data-ttu-id="a6e45-126">Le nombre de sonneries démarre à zéro.</span><span class="sxs-lookup"><span data-stu-id="a6e45-126">The ring count starts at zero.</span></span>

<span data-ttu-id="a6e45-127">Si *dwParam1* est LINEDEVSTATE \_ Réinit et que le message a été émis par l’interface TAPI suite à la traduction d’un nouveau message d’API en message de réinitialisation, *DwParam3* contient le paramètre *dwParam1* du message d’origine (par exemple, LINEDEVSTATE \_ TRANSLATECHANGE ou une autre \_ valeur LINEDEVSTATE, si *dwParam2* est \_ la ligne LINEDEVSTATE ou le nouvel identificateur de périphérique, si *dwParam2* est la [**ligne \_ Create**](line-create.md)).</span><span class="sxs-lookup"><span data-stu-id="a6e45-127">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam3* contains the *dwParam1* parameter of the original message (for example, LINEDEVSTATE\_TRANSLATECHANGE or some other LINEDEVSTATE\_ value, if *dwParam2* is LINE\_LINEDEVSTATE, or the new device identifier, if *dwParam2* is [**LINE\_CREATE**](line-create.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6e45-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6e45-128">Return value</span></span>

<span data-ttu-id="a6e45-129">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a6e45-129">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6e45-130">Notes</span><span class="sxs-lookup"><span data-stu-id="a6e45-130">Remarks</span></span>

<span data-ttu-id="a6e45-131">L’envoi de la **ligne \_ LINEDEVSTATE** message peut être contrôlé avec [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="a6e45-131">The sending of the **LINE\_LINEDEVSTATE** message can be controlled with [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="a6e45-132">Une application peut indiquer des modifications d’élément d’État sur lesquelles elle souhaite être notifiée.</span><span class="sxs-lookup"><span data-stu-id="a6e45-132">An application can indicate status item changes about which it wants to be notified.</span></span> <span data-ttu-id="a6e45-133">Par défaut, tous les rapports d’État sont désactivés, à l’exception de LINEDEVSTATE \_ reinit, qui ne peut pas être désactivé.</span><span class="sxs-lookup"><span data-stu-id="a6e45-133">By default, all status reporting is disabled except for LINEDEVSTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="a6e45-134">Ce message est envoyé à toutes les applications qui ont un handle vers la ligne, y compris celles qui ont appelé [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) avec le paramètre *DWPRIVILEGES* défini sur LINECALLPRIVILEGE \_ None, LINECALLPRIVILEGE \_ Owner, LINECALLPRIVILEGE \_ Monitor ou des combinaisons autorisées de ces.</span><span class="sxs-lookup"><span data-stu-id="a6e45-134">This message is sent to all applications that have a handle to the line, including those that called [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) with the *dwPrivileges* parameter set to LINECALLPRIVILEGE\_NONE, LINECALLPRIVILEGE\_OWNER, LINECALLPRIVILEGE\_MONITOR, or permitted combinations of these.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6e45-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6e45-135">Requirements</span></span>



| <span data-ttu-id="a6e45-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6e45-136">Requirement</span></span> | <span data-ttu-id="a6e45-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6e45-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a6e45-138">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="a6e45-138">TAPI version</span></span><br/> | <span data-ttu-id="a6e45-139">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a6e45-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a6e45-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6e45-140">Header</span></span><br/>       | <dl> <span data-ttu-id="a6e45-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6e45-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6e45-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6e45-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6e45-143">**fermeture de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="a6e45-143">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="a6e45-144">**création de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="a6e45-144">**LINE\_CREATE**</span></span>](line-create.md)
</dt> <dt>

[<span data-ttu-id="a6e45-145">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="a6e45-145">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="a6e45-146">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="a6e45-146">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="a6e45-147">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="a6e45-147">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="a6e45-148">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="a6e45-148">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="a6e45-149">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="a6e45-149">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="a6e45-150">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="a6e45-150">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="a6e45-151">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="a6e45-151">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="a6e45-152">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="a6e45-152">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[<span data-ttu-id="a6e45-153">**LINETRANSLATECAPS**</span><span class="sxs-lookup"><span data-stu-id="a6e45-153">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="a6e45-154">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="a6e45-154">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




