---
description: Le message CALLINFO de ligne TAPI \_ est envoyé lorsque les informations sur l’appel de l’appel spécifié ont été modifiées. L’application peut appeler lineGetCallInfo pour déterminer les informations d’appel actuelles.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: Message LINE_CALLINFO (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541114"
---
# <a name="line_callinfo-message"></a><span data-ttu-id="8ac72-104">\_Message CALLINFO de ligne</span><span class="sxs-lookup"><span data-stu-id="8ac72-104">LINE\_CALLINFO message</span></span>

<span data-ttu-id="8ac72-105">Le message **\_ CALLINFO de ligne** TAPI est envoyé lorsque les informations sur l’appel de l’appel spécifié ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="8ac72-105">The TAPI **LINE\_CALLINFO** message is sent when the call information about the specified call has changed.</span></span> <span data-ttu-id="8ac72-106">L’application peut appeler [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) pour déterminer les informations d’appel actuelles.</span><span class="sxs-lookup"><span data-stu-id="8ac72-106">The application can invoke [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the current call information.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="8ac72-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ac72-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ac72-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="8ac72-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac72-109">Handle de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8ac72-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="8ac72-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="8ac72-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac72-111">Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8ac72-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="8ac72-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8ac72-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac72-113">Élément d’informations d’appel qui a changé.</span><span class="sxs-lookup"><span data-stu-id="8ac72-113">The call information item that has changed.</span></span> <span data-ttu-id="8ac72-114">Il peut s’agir d’une ou plusieurs des [**\_ constantes LINECALLINFOSTATE**](linecallinfostate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8ac72-114">Can be one or more of the [**LINECALLINFOSTATE\_ constants**](linecallinfostate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ac72-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8ac72-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac72-116">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="8ac72-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8ac72-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="8ac72-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="8ac72-118">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="8ac72-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ac72-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ac72-119">Return value</span></span>

<span data-ttu-id="8ac72-120">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8ac72-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ac72-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8ac72-121">Remarks</span></span>

<span data-ttu-id="8ac72-122">Un **message \_ CALLINFO de ligne** avec une indication *NumOwnersIncr*, *NumOwnersDecr* et/ou *NumMonitorsChanged* est envoyé aux applications qui ont déjà un handle pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="8ac72-122">A **LINE\_CALLINFO** message with a *NumOwnersIncr*, *NumOwnersDecr*, and/or *NumMonitorsChanged* indication is sent to applications that already have a handle for the call.</span></span> <span data-ttu-id="8ac72-123">Cela peut être le résultat d’une autre application modifiant la propriété ou la surveillance d’un appel avec [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)et [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span><span class="sxs-lookup"><span data-stu-id="8ac72-123">This can be the result of another application changing ownership or monitorship to a call with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls), and [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span></span>

<span data-ttu-id="8ac72-124">Ces **messages \_ CALLINFO de ligne** ne sont pas envoyés lorsqu’une notification d’un nouvel appel est fournie dans un message de [**ligne \_ CALLSTATE**](line-callstate.md) , car les informations d’appel reflètent déjà le nombre correct de propriétaires et de moniteurs au moment où la ligne \_ CALLSTATE messages sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="8ac72-124">These **LINE\_CALLINFO** messages are not sent when a notification of a new call is provided in a [**LINE\_CALLSTATE**](line-callstate.md) message, because the call information already reflects the correct number of owners and monitors at the time the LINE\_CALLSTATE messages are sent.</span></span> <span data-ttu-id="8ac72-125">**Ligne \_** Les messages CALLINFO sont également supprimés dans le cas où un appel est offert par l’interface TAPI à des analyses via le \_ mécanisme LINECALLSTATE inconnu.</span><span class="sxs-lookup"><span data-stu-id="8ac72-125">**LINE\_CALLINFO** messages are also suppressed in the case where a call is offered by TAPI to monitors through the LINECALLSTATE\_UNKNOWN mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="8ac72-126">L’application qui provoque une modification du nombre de propriétaires ou d’analyses (par exemple, en appelant [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) ou [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) ne reçoit pas lui-même un message indiquant que la modification a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="8ac72-126">The application that causes a change in the number of owners or monitors (for example, by invoking [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) or [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) does not itself receive a message indicating that the change has been done.</span></span>

 

<span data-ttu-id="8ac72-127">Aucun **message \_ CALLINFO de ligne** n’est envoyé pour un appel une fois que l’appel est passé à l’état *inactif* .</span><span class="sxs-lookup"><span data-stu-id="8ac72-127">No **LINE\_CALLINFO** messages are sent for a call after the call has entered the *idle* state.</span></span> <span data-ttu-id="8ac72-128">Plus précisément, les modifications du nombre de propriétaires et de moniteurs ne sont pas signalées, car les applications libèrent leurs Handles pour l’appel inactif.</span><span class="sxs-lookup"><span data-stu-id="8ac72-128">Specifically, changes in the number of owners and monitors are not reported as applications deallocate their handles for the idle call.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ac72-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ac72-129">Requirements</span></span>



| <span data-ttu-id="8ac72-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ac72-130">Requirement</span></span> | <span data-ttu-id="8ac72-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ac72-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8ac72-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8ac72-132">TAPI version</span></span><br/> | <span data-ttu-id="8ac72-133">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8ac72-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8ac72-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ac72-134">Header</span></span><br/>       | <dl> <span data-ttu-id="8ac72-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ac72-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ac72-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ac72-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac72-137">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="8ac72-137">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="8ac72-138">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="8ac72-138">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="8ac72-139">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="8ac72-139">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="8ac72-140">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="8ac72-140">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="8ac72-141">**lineGetNewCalls**</span><span class="sxs-lookup"><span data-stu-id="8ac72-141">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[<span data-ttu-id="8ac72-142">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="8ac72-142">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="8ac72-143">**lineSetCallPrivilege**</span><span class="sxs-lookup"><span data-stu-id="8ac72-143">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[<span data-ttu-id="8ac72-144">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="8ac72-144">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




