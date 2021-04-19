---
description: La ligne \_ PROXYSTATUS le message est envoyé lorsque les proxies disponibles changent sur une ligne ouverte par l’application.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: Message LINE_PROXYSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542371"
---
# <a name="line_proxystatus-message"></a><span data-ttu-id="7f13e-103">\_Message PROXYSTATUS de ligne</span><span class="sxs-lookup"><span data-stu-id="7f13e-103">LINE\_PROXYSTATUS message</span></span>

<span data-ttu-id="7f13e-104">La **ligne \_ PROXYSTATUS** le message est envoyé lorsque les proxies disponibles changent sur une ligne ouverte par l’application.</span><span class="sxs-lookup"><span data-stu-id="7f13e-104">The **LINE\_PROXYSTATUS** message is sent when the available proxies change on a line that the application currently has open.</span></span>

<span data-ttu-id="7f13e-105">TAPISRV génère ce message pendant une fonction [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) à l’aide de LINEPROXYSTATUS \_ Open et LINEPROXYSTATUS \_ ALLOPENFORACD ou d’une fonction [**LINECLOSE**](/windows/desktop/api/Tapi/nf-tapi-lineclose) à l’aide de LINEPROXYSTATUS \_ Close (toutes les [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md)).</span><span class="sxs-lookup"><span data-stu-id="7f13e-105">TAPISRV generates this message during a [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) function using LINEPROXYSTATUS\_OPEN and LINEPROXYSTATUS\_ALLOPENFORACD or a [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) function using LINEPROXYSTATUS\_CLOSE (all [**LINEPROXYSTATUS\_ Constants**](lineproxystatus--constants.md)).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7f13e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f13e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f13e-107">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="7f13e-107">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7f13e-108">Handle de l’application sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="7f13e-108">The application's handle to the line device.</span></span> <span data-ttu-id="7f13e-109">Cela est relatif au gestionnaire de l’agent.</span><span class="sxs-lookup"><span data-stu-id="7f13e-109">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="7f13e-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="7f13e-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7f13e-111">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="7f13e-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="7f13e-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7f13e-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="7f13e-113">Spécifie l’état de la file d’attente qui a changé.</span><span class="sxs-lookup"><span data-stu-id="7f13e-113">Specifies the queue status that has changed.</span></span> <span data-ttu-id="7f13e-114">Il peut s’agir d’une ou plusieurs des [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="7f13e-114">Can be one or more of the [**LINEPROXYSTATUS\_ constants**](lineproxystatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f13e-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7f13e-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="7f13e-116">Si *dwParam1* a la valeur LINEPROXYSTATUS \_ Open ou LINEPROXYSTATUS \_ Close, *dwParam2* indique le type de requête proxy associé, qui est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7f13e-116">If *dwParam1* is set to LINEPROXYSTATUS\_OPEN or LINEPROXYSTATUS\_CLOSE, *dwParam2* indicates the related proxy request type, which is one of the following:</span></span>

-   <span data-ttu-id="7f13e-117">LINEPROXYREQUEST \_ SETAGENTGROUP</span><span class="sxs-lookup"><span data-stu-id="7f13e-117">LINEPROXYREQUEST\_SETAGENTGROUP</span></span>
-   <span data-ttu-id="7f13e-118">LINEPROXYREQUEST \_ SETAGENTSTATE</span><span class="sxs-lookup"><span data-stu-id="7f13e-118">LINEPROXYREQUEST\_SETAGENTSTATE</span></span>
-   <span data-ttu-id="7f13e-119">LINEPROXYREQUEST \_ SETAGENTACTIVITY</span><span class="sxs-lookup"><span data-stu-id="7f13e-119">LINEPROXYREQUEST\_SETAGENTACTIVITY</span></span>
-   <span data-ttu-id="7f13e-120">LINEPROXYREQUEST \_ GETAGENTCAPS</span><span class="sxs-lookup"><span data-stu-id="7f13e-120">LINEPROXYREQUEST\_GETAGENTCAPS</span></span>
-   <span data-ttu-id="7f13e-121">LINEPROXYREQUEST \_ GETAGENTSTATUS</span><span class="sxs-lookup"><span data-stu-id="7f13e-121">LINEPROXYREQUEST\_GETAGENTSTATUS</span></span>
-   <span data-ttu-id="7f13e-122">LINEPROXYREQUEST \_ AGENTSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="7f13e-122">LINEPROXYREQUEST\_AGENTSPECIFIC</span></span>
-   <span data-ttu-id="7f13e-123">LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST</span><span class="sxs-lookup"><span data-stu-id="7f13e-123">LINEPROXYREQUEST\_GETAGENTACTIVITYLIST</span></span>
-   <span data-ttu-id="7f13e-124">LINEPROXYREQUEST \_ GETAGENTGROUPLIST</span><span class="sxs-lookup"><span data-stu-id="7f13e-124">LINEPROXYREQUEST\_GETAGENTGROUPLIST</span></span>
-   <span data-ttu-id="7f13e-125">LINEPROXYREQUEST \_ CREATEAGENT</span><span class="sxs-lookup"><span data-stu-id="7f13e-125">LINEPROXYREQUEST\_CREATEAGENT</span></span>
-   <span data-ttu-id="7f13e-126">LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD</span><span class="sxs-lookup"><span data-stu-id="7f13e-126">LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="7f13e-127">LINEPROXYREQUEST \_ GETAGENTINFO</span><span class="sxs-lookup"><span data-stu-id="7f13e-127">LINEPROXYREQUEST\_GETAGENTINFO</span></span>
-   <span data-ttu-id="7f13e-128">LINEPROXYREQUEST \_ CREATEAGENTSESSION</span><span class="sxs-lookup"><span data-stu-id="7f13e-128">LINEPROXYREQUEST\_CREATEAGENTSESSION</span></span>
-   <span data-ttu-id="7f13e-129">LINEPROXYREQUEST \_ GETAGENTSESSIONLIST</span><span class="sxs-lookup"><span data-stu-id="7f13e-129">LINEPROXYREQUEST\_GETAGENTSESSIONLIST</span></span>
-   <span data-ttu-id="7f13e-130">LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE</span><span class="sxs-lookup"><span data-stu-id="7f13e-130">LINEPROXYREQUEST\_SETAGENTSESSIONSTATE</span></span>
-   <span data-ttu-id="7f13e-131">LINEPROXYREQUEST \_ GETAGENTSESSIONINFO</span><span class="sxs-lookup"><span data-stu-id="7f13e-131">LINEPROXYREQUEST\_GETAGENTSESSIONINFO</span></span>
-   <span data-ttu-id="7f13e-132">LINEPROXYREQUEST \_ GETQUEUELIST</span><span class="sxs-lookup"><span data-stu-id="7f13e-132">LINEPROXYREQUEST\_GETQUEUELIST</span></span>
-   <span data-ttu-id="7f13e-133">LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD</span><span class="sxs-lookup"><span data-stu-id="7f13e-133">LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="7f13e-134">LINEPROXYREQUEST \_ GETQUEUEINFO</span><span class="sxs-lookup"><span data-stu-id="7f13e-134">LINEPROXYREQUEST\_GETQUEUEINFO</span></span>
-   <span data-ttu-id="7f13e-135">LINEPROXYREQUEST \_ GETGROUPLIST</span><span class="sxs-lookup"><span data-stu-id="7f13e-135">LINEPROXYREQUEST\_GETGROUPLIST</span></span>
-   <span data-ttu-id="7f13e-136">LINEPROXYREQUEST \_ SETAGENTSTATEEX</span><span class="sxs-lookup"><span data-stu-id="7f13e-136">LINEPROXYREQUEST\_SETAGENTSTATEEX</span></span>

<span data-ttu-id="7f13e-137">Sinon, *dwParam2* a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="7f13e-137">Otherwise, *dwParam2* is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7f13e-138">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="7f13e-138">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="7f13e-139">Réservé.</span><span class="sxs-lookup"><span data-stu-id="7f13e-139">Reserved.</span></span> <span data-ttu-id="7f13e-140">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="7f13e-140">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f13e-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f13e-141">Requirements</span></span>



| <span data-ttu-id="7f13e-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f13e-142">Requirement</span></span> | <span data-ttu-id="7f13e-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f13e-143">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7f13e-144">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="7f13e-144">TAPI version</span></span><br/> | <span data-ttu-id="7f13e-145">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="7f13e-145">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="7f13e-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f13e-146">Header</span></span><br/>       | <dl> <span data-ttu-id="7f13e-147"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f13e-147"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f13e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f13e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f13e-149">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="7f13e-149">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="7f13e-150">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="7f13e-150">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="7f13e-151">**PROXYREQUEST de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="7f13e-151">**LINE\_PROXYREQUEST**</span></span>](line-proxyrequest.md)
</dt> <dt>

[<span data-ttu-id="7f13e-152">**\_Constantes LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="7f13e-152">**LINEPROXYREQUEST\_ Constants**</span></span>](lineproxyrequest--constants.md)
</dt> </dl>

 

 




