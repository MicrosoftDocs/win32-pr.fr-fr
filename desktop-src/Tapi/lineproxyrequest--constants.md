---
description: Ces constantes sont utilisées dans deux contextes.
ms.assetid: 5c05a567-cc65-411e-b049-919a442c5c57
title: Constantes LINEPROXYREQUEST_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba34a3a7f7b1f41f0c32783c4132afcfafef1aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535323"
---
# <a name="lineproxyrequest_-constants"></a><span data-ttu-id="71fc5-103">\_Constantes LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="71fc5-103">LINEPROXYREQUEST\_ Constants</span></span>

<span data-ttu-id="71fc5-104">Ces constantes sont utilisées dans deux contextes.</span><span class="sxs-lookup"><span data-stu-id="71fc5-104">These constants are used in two contexts.</span></span> <span data-ttu-id="71fc5-105">Tout d’abord, elles peuvent être utilisées dans un tableau de valeurs **DWORD** dans la structure [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passée avec [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) lorsque l' \_ option de proxy LINEOPENOPTION est spécifiée, pour indiquer les fonctions que l’application est prête à gérer.</span><span class="sxs-lookup"><span data-stu-id="71fc5-105">First, they can be used in an array of **DWORD** values in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) when the LINEOPENOPTION\_PROXY option is specified, to indicate which functions the application is willing to handle.</span></span> <span data-ttu-id="71fc5-106">Deuxièmement, elles sont utilisées dans la [**ligne \_ PROXYREQUEST**](line-proxyrequest.md) transmise à l’application de gestionnaire par un message de **ligne \_ PROXYREQUEST** pour indiquer le type de demande à traiter et le format des données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="71fc5-106">Second, they are used in the [**LINE\_PROXYREQUEST**](line-proxyrequest.md) passed to the handler application by a **LINE\_PROXYREQUEST** message to indicate the type of request that is to be processed and the format of the data in the buffer.</span></span>

<dl> <dt>

<span data-ttu-id="71fc5-107"><span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**LINEPROXYREQUEST \_ AGENTSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="71fc5-107"><span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**LINEPROXYREQUEST\_AGENTSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-108">Associé à [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).</span><span class="sxs-lookup"><span data-stu-id="71fc5-108">Associated with [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-109"><span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**LINEPROXYREQUEST \_ CREATEAGENT**</span><span class="sxs-lookup"><span data-stu-id="71fc5-109"><span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**LINEPROXYREQUEST\_CREATEAGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-110">Associé à [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).</span><span class="sxs-lookup"><span data-stu-id="71fc5-110">Associated with [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-111"><span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**LINEPROXYREQUEST \_ CREATEAGENTSESSION**</span><span class="sxs-lookup"><span data-stu-id="71fc5-111"><span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**LINEPROXYREQUEST\_CREATEAGENTSESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-112">Associé à [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).</span><span class="sxs-lookup"><span data-stu-id="71fc5-112">Associated with [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-113"><span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST**</span><span class="sxs-lookup"><span data-stu-id="71fc5-113"><span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**LINEPROXYREQUEST\_GETAGENTACTIVITYLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-114">Associé à [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).</span><span class="sxs-lookup"><span data-stu-id="71fc5-114">Associated with [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-115"><span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**LINEPROXYREQUEST \_ GETAGENTCAPS**</span><span class="sxs-lookup"><span data-stu-id="71fc5-115"><span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**LINEPROXYREQUEST\_GETAGENTCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-116">Associé à [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).</span><span class="sxs-lookup"><span data-stu-id="71fc5-116">Associated with [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-117"><span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**LINEPROXYREQUEST \_ GETAGENTGROUPLIST**</span><span class="sxs-lookup"><span data-stu-id="71fc5-117"><span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**LINEPROXYREQUEST\_GETAGENTGROUPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-118">Associé à [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).</span><span class="sxs-lookup"><span data-stu-id="71fc5-118">Associated with [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-119"><span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**LINEPROXYREQUEST \_ GETAGENTINFO**</span><span class="sxs-lookup"><span data-stu-id="71fc5-119"><span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**LINEPROXYREQUEST\_GETAGENTINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-120">Associé à [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).</span><span class="sxs-lookup"><span data-stu-id="71fc5-120">Associated with [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-121"><span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**LINEPROXYREQUEST \_ GETAGENTSESSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="71fc5-121"><span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**LINEPROXYREQUEST\_GETAGENTSESSIONINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-122">Associé à [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).</span><span class="sxs-lookup"><span data-stu-id="71fc5-122">Associated with [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-123"><span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**LINEPROXYREQUEST \_ GETAGENTSESSIONLIST**</span><span class="sxs-lookup"><span data-stu-id="71fc5-123"><span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**LINEPROXYREQUEST\_GETAGENTSESSIONLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-124">Associé à [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).</span><span class="sxs-lookup"><span data-stu-id="71fc5-124">Associated with [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-125"><span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**LINEPROXYREQUEST \_ GETAGENTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="71fc5-125"><span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**LINEPROXYREQUEST\_GETAGENTSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-126">Associé à [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).</span><span class="sxs-lookup"><span data-stu-id="71fc5-126">Associated with [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-127"><span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST \_ GETGROUPLIST**</span><span class="sxs-lookup"><span data-stu-id="71fc5-127"><span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST\_GETGROUPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-128">Associé à [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).</span><span class="sxs-lookup"><span data-stu-id="71fc5-128">Associated with [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-129"><span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**LINEPROXYREQUEST \_ GETQUEUEINFO**</span><span class="sxs-lookup"><span data-stu-id="71fc5-129"><span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**LINEPROXYREQUEST\_GETQUEUEINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-130">Associé à [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).</span><span class="sxs-lookup"><span data-stu-id="71fc5-130">Associated with [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-131"><span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST \_ GETQUEUELIST**</span><span class="sxs-lookup"><span data-stu-id="71fc5-131"><span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST\_GETQUEUELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-132">Associé à [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).</span><span class="sxs-lookup"><span data-stu-id="71fc5-132">Associated with [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-133"><span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**LINEPROXYREQUEST \_ SETAGENTACTIVITY**</span><span class="sxs-lookup"><span data-stu-id="71fc5-133"><span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**LINEPROXYREQUEST\_SETAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-134">Associé à [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).</span><span class="sxs-lookup"><span data-stu-id="71fc5-134">Associated with [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-135"><span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**LINEPROXYREQUEST \_ SETAGENTGROUP**</span><span class="sxs-lookup"><span data-stu-id="71fc5-135"><span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**LINEPROXYREQUEST\_SETAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-136">Associé à [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).</span><span class="sxs-lookup"><span data-stu-id="71fc5-136">Associated with [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-137"><span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD**</span><span class="sxs-lookup"><span data-stu-id="71fc5-137"><span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-138">Associé à [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).</span><span class="sxs-lookup"><span data-stu-id="71fc5-138">Associated with [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-139"><span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE**</span><span class="sxs-lookup"><span data-stu-id="71fc5-139"><span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**LINEPROXYREQUEST\_SETAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-140">Associé à [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).</span><span class="sxs-lookup"><span data-stu-id="71fc5-140">Associated with [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-141"><span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**LINEPROXYREQUEST \_ SETAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="71fc5-141"><span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**LINEPROXYREQUEST\_SETAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-142">Associé à [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).</span><span class="sxs-lookup"><span data-stu-id="71fc5-142">Associated with [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-143"><span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**LINEPROXYREQUEST \_ SETAGENTSTATEEX**</span><span class="sxs-lookup"><span data-stu-id="71fc5-143"><span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**LINEPROXYREQUEST\_SETAGENTSTATEEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-144">Associé à [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).</span><span class="sxs-lookup"><span data-stu-id="71fc5-144">Associated with [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71fc5-145"><span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD**</span><span class="sxs-lookup"><span data-stu-id="71fc5-145"><span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71fc5-146">Associé à [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).</span><span class="sxs-lookup"><span data-stu-id="71fc5-146">Associated with [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71fc5-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71fc5-147">Requirements</span></span>



| <span data-ttu-id="71fc5-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71fc5-148">Requirement</span></span> | <span data-ttu-id="71fc5-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="71fc5-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71fc5-150">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="71fc5-150">TAPI version</span></span><br/> | <span data-ttu-id="71fc5-151">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="71fc5-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="71fc5-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="71fc5-152">Header</span></span><br/>       | <dl> <span data-ttu-id="71fc5-153"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="71fc5-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71fc5-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71fc5-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71fc5-155">Constantes de centre d’appels</span><span class="sxs-lookup"><span data-stu-id="71fc5-155">Call Center Constants</span></span>](call-center-constants.md)
</dt> <dt>

[<span data-ttu-id="71fc5-156">Fonctions du centre d’appels</span><span class="sxs-lookup"><span data-stu-id="71fc5-156">Call Center Functions</span></span>](call-center-functions.md)
</dt> </dl>

 

 




