---
description: L’objet SWbemSink est implémenté par les applications clientes pour recevoir les résultats des opérations asynchrones et des notifications d’événements.
ms.assetid: a90777ef-fa26-4bfb-b196-c083a0c92a29
ms.tgt_platform: multiple
title: Objet SWbemSink (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink
- ISWbemSinkEvents
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b8007b7387a09e31f49dbc833f657bc959ee11e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541194"
---
# <a name="swbemsink-object"></a><span data-ttu-id="b1f96-103">Objet SWbemSink</span><span class="sxs-lookup"><span data-stu-id="b1f96-103">SWbemSink object</span></span>

<span data-ttu-id="b1f96-104">L’objet **SWbemSink** est implémenté par les applications clientes pour recevoir les résultats des opérations asynchrones et des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="b1f96-104">The **SWbemSink** object is implemented by client applications to receive the results of asynchronous operations and event notifications.</span></span> <span data-ttu-id="b1f96-105">Pour effectuer un appel asynchrone, vous devez créer une instance d’un objet **SWbemSink** et la passer en tant que paramètre *ObjWbemSink* .</span><span class="sxs-lookup"><span data-stu-id="b1f96-105">To make an asynchronous call, you must create an instance of an **SWbemSink** object and pass it as the *ObjWbemSink* parameter.</span></span> <span data-ttu-id="b1f96-106">Les événements de votre implémentation de **SWbemSink** sont déclenchés lorsque l’État ou les résultats sont retournés, ou lorsque l’appel est terminé.</span><span class="sxs-lookup"><span data-stu-id="b1f96-106">The events in your implementation of **SWbemSink** are triggered when status or results are returned, or when the call is complete.</span></span> <span data-ttu-id="b1f96-107">L’appel de VBScript **CreateObject** crée cet objet.</span><span class="sxs-lookup"><span data-stu-id="b1f96-107">The VBScript **CreateObject** call creates this object.</span></span>

## <a name="members"></a><span data-ttu-id="b1f96-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b1f96-108">Members</span></span>

<span data-ttu-id="b1f96-109">L’objet **SWbemSink** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b1f96-109">The **SWbemSink** object has these types of members:</span></span>

-   [<span data-ttu-id="b1f96-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b1f96-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b1f96-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b1f96-111">Methods</span></span>

<span data-ttu-id="b1f96-112">L’objet **SWbemSink** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b1f96-112">The **SWbemSink** object has these methods.</span></span>



| <span data-ttu-id="b1f96-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="b1f96-113">Method</span></span>                             | <span data-ttu-id="b1f96-114">Description</span><span class="sxs-lookup"><span data-stu-id="b1f96-114">Description</span></span>                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="b1f96-115">**Annuler**</span><span class="sxs-lookup"><span data-stu-id="b1f96-115">**Cancel**</span></span>](swbemsink-cancel.md) | <span data-ttu-id="b1f96-116">Annule toutes les opérations asynchrones associées à ce récepteur.</span><span class="sxs-lookup"><span data-stu-id="b1f96-116">Cancels all asynchronous operations that are associated with this sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b1f96-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b1f96-117">Remarks</span></span>

<span data-ttu-id="b1f96-118">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="b1f96-118">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b1f96-119">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="b1f96-119">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b1f96-120">Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone.</span><span class="sxs-lookup"><span data-stu-id="b1f96-120">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="b1f96-121">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b1f96-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

### <a name="events"></a><span data-ttu-id="b1f96-122">Événements</span><span class="sxs-lookup"><span data-stu-id="b1f96-122">Events</span></span>

<span data-ttu-id="b1f96-123">Vous pouvez implémenter des sous-routines à appeler lorsque des événements sont déclenchés.</span><span class="sxs-lookup"><span data-stu-id="b1f96-123">You can implement subroutines to be called when events are triggered.</span></span> <span data-ttu-id="b1f96-124">Par exemple, si vous souhaitez traiter chaque objet retourné par un appel de requête asynchrone comme [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), créez une sous-routine à l’aide du récepteur qui est spécifié dans l’appel asynchrone, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="b1f96-124">For example, if you want to process each object that is returned by an asynchronous query call such as [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), create a subroutine using the sink that is specified in the asynchronous call, as shown in the following example.</span></span>


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



<span data-ttu-id="b1f96-125">Utilisez le tableau suivant comme référence pour identifier les événements et les descriptions des déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="b1f96-125">Use the following table as a reference to identify events and trigger descriptions.</span></span>



| <span data-ttu-id="b1f96-126">Événement</span><span class="sxs-lookup"><span data-stu-id="b1f96-126">Event</span></span>                                            | <span data-ttu-id="b1f96-127">Description</span><span class="sxs-lookup"><span data-stu-id="b1f96-127">Description</span></span>                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="b1f96-128">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="b1f96-128">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="b1f96-129">Déclenché lorsqu’une opération asynchrone est terminée.</span><span class="sxs-lookup"><span data-stu-id="b1f96-129">Triggered when an asynchronous operation is complete.</span></span>                   |
| [<span data-ttu-id="b1f96-130">**OnObjectPut**</span><span class="sxs-lookup"><span data-stu-id="b1f96-130">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="b1f96-131">Déclenché lorsqu’une opération put asynchrone est terminée.</span><span class="sxs-lookup"><span data-stu-id="b1f96-131">Triggered when an asynchronous Put operation is complete.</span></span>               |
| [<span data-ttu-id="b1f96-132">**OnObjectReady**</span><span class="sxs-lookup"><span data-stu-id="b1f96-132">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="b1f96-133">Déclenché lorsqu’un objet fourni par un appel asynchrone est disponible.</span><span class="sxs-lookup"><span data-stu-id="b1f96-133">Triggered when an object provided by an asynchronous call is available.</span></span> |
| [<span data-ttu-id="b1f96-134">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="b1f96-134">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="b1f96-135">Déclenché pour fournir l’état d’une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b1f96-135">Triggered to provide the status of a asynchronous operation.</span></span>            |



 

<span data-ttu-id="b1f96-136">**Récupération asynchrone des statistiques des journaux des événements**</span><span class="sxs-lookup"><span data-stu-id="b1f96-136">**Asynchronously Retrieving Event Log Statistics**</span></span>

<span data-ttu-id="b1f96-137">WMI prend en charge les scripts asynchrones et semi-synchrones.</span><span class="sxs-lookup"><span data-stu-id="b1f96-137">WMI supports both asynchronous and semi-synchronous scripts.</span></span> <span data-ttu-id="b1f96-138">Lors de la récupération d’événements à partir des journaux des événements, les scripts asynchrones récupèrent souvent ces données beaucoup plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="b1f96-138">When retrieving events from the event logs, asynchronous scripts often retrieve this data much faster.</span></span>

<span data-ttu-id="b1f96-139">Dans un script asynchrone, une requête est émise et le contrôle est immédiatement retourné au script.</span><span class="sxs-lookup"><span data-stu-id="b1f96-139">In an asynchronous script, a query is issued and control is immediately returned to the script.</span></span> <span data-ttu-id="b1f96-140">La requête continue à traiter sur un thread distinct, tandis que le script commence immédiatement à agir sur les informations retournées.</span><span class="sxs-lookup"><span data-stu-id="b1f96-140">The query continues to process on a separate thread while the script begins to immediately act on the information that is returned.</span></span> <span data-ttu-id="b1f96-141">Les scripts asynchrones sont pilotés par les événements : chaque fois qu’un enregistrement d’événement est récupéré, l’événement OnObjectReady est déclenché.</span><span class="sxs-lookup"><span data-stu-id="b1f96-141">Asynchronous scripts are event driven: each time an event record is retrieved, the OnObjectReady event is fired.</span></span> <span data-ttu-id="b1f96-142">Une fois la requête terminée, l’événement OnCompleted se déclenche et le script peut continuer en fonction du fait que tous les enregistrements disponibles ont été retournés.</span><span class="sxs-lookup"><span data-stu-id="b1f96-142">When the query has completed, the OnCompleted event will fire, and the script can continue based on the fact that all the available records have been returned.</span></span>

<span data-ttu-id="b1f96-143">En revanche, dans un script semi-synchrone, une requête est émise et le script met en file d’attente une grande quantité d’informations extraites avant d’agir dessus.</span><span class="sxs-lookup"><span data-stu-id="b1f96-143">In a semi-synchronous script, by contrast, a query is issued and the script then queues a large amount of retrieved information before acting upon it.</span></span> <span data-ttu-id="b1f96-144">Pour de nombreux objets, le traitement semi-synchrone est approprié ; par exemple, lors de l’interrogation d’un lecteur de disque pour ses propriétés, il peut y avoir uniquement une seconde fractionnée entre le moment où la requête est émise et le moment où les informations sont retournées et exploitées.</span><span class="sxs-lookup"><span data-stu-id="b1f96-144">For many objects, semi-synchronous processing is adequate; for example, when querying a disk drive for its properties, there might be only a split second between the time the query is issued and the time the information is returned and acted upon.</span></span> <span data-ttu-id="b1f96-145">Cela est dû en grande partie au fait que la quantité d’informations renvoyées est relativement faible.</span><span class="sxs-lookup"><span data-stu-id="b1f96-145">This is due in large part to the fact that the amount of information returned is relatively small.</span></span>

<span data-ttu-id="b1f96-146">Toutefois, lors de l’interrogation d’un journal des événements, l’intervalle entre le moment où la requête est émise et le moment où un script semi-synchrone peut se terminer et le retour des informations peut prendre des heures.</span><span class="sxs-lookup"><span data-stu-id="b1f96-146">When querying an event log, however, the interval between the time the query is issued and the time that a semi-synchronous script can finish returning and acting on the information can take hours.</span></span> <span data-ttu-id="b1f96-147">En plus de cela, le script peut manquer de mémoire et échouer de manière autonome avant de terminer.</span><span class="sxs-lookup"><span data-stu-id="b1f96-147">On top of that, the script might run out of memory and fail on its own before completing.</span></span>

<span data-ttu-id="b1f96-148">Pour les journaux des événements avec un grand nombre d’enregistrements, la différence de temps de traitement peut être considérable.</span><span class="sxs-lookup"><span data-stu-id="b1f96-148">For event logs with a large number of records, the difference in processing time can be considerable.</span></span> <span data-ttu-id="b1f96-149">Sur un ordinateur de test basé sur Windows 2000 avec 2 000 enregistrements dans le journal des événements, une requête semi-synchrone qui a récupéré tous les événements et les a affichés dans une fenêtre de commande a duré 10 minutes 45 secondes.</span><span class="sxs-lookup"><span data-stu-id="b1f96-149">On a Windows 2000-based test computer with 2,000 records in the event log, a semi-synchronous query that retrieved all the events and displayed them in a command window took 10 minutes 45 seconds.</span></span> <span data-ttu-id="b1f96-150">Une requête asynchrone qui a effectué la même opération a duré une minute de 54 secondes.</span><span class="sxs-lookup"><span data-stu-id="b1f96-150">An asynchronous query that performed the same operation took one minute 54 seconds.</span></span>

## <a name="examples"></a><span data-ttu-id="b1f96-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="b1f96-151">Examples</span></span>

<span data-ttu-id="b1f96-152">Le code VBScript suivant interroge de manière asynchrone les journaux des événements pour tous les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="b1f96-152">The following VBScript asynchronously queries the event logs for all records.</span></span>


```VB
Const POPUP_DURATION = 10
Const OK_BUTTON = 0
Set objWSHShell = Wscript.CreateObject("Wscript.Shell")
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
objWMIService.InstancesOfAsync objSink, "Win32_NTLogEvent"
errReturn = objWshShell.Popup("Retrieving events", POPUP_DURATION, _
"Event Retrieval", OK_BUTTON)
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
 WScript.Echo "Asynchronous operation is done."
End Sub
Sub SINK_OnObjectReady(objEvent, objAsyncContext)
 Wscript.Echo "Category: " & objEvent.Category
 Wscript.Echo "Computer Name: " & objEvent.ComputerName
 Wscript.Echo "Event Code: " & objEvent.EventCode
 Wscript.Echo "Message: " & objEvent.Message
 Wscript.Echo "Record Number: " & objEvent.RecordNumber
 Wscript.Echo "Source Name: " & objEvent.SourceName
 Wscript.Echo "Time Written: " & objEvent.TimeWritten
 Wscript.Echo "Event Type: " & objEvent.Type
 Wscript.Echo "User: " & objEvent.User
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b1f96-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1f96-153">Requirements</span></span>



| <span data-ttu-id="b1f96-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1f96-154">Requirement</span></span> | <span data-ttu-id="b1f96-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1f96-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f96-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1f96-156">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f96-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1f96-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1f96-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1f96-158">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f96-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1f96-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1f96-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1f96-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1f96-161"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1f96-161"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1f96-162">MIDL</span><span class="sxs-lookup"><span data-stu-id="b1f96-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1f96-163"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1f96-163"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b1f96-164">DLL</span><span class="sxs-lookup"><span data-stu-id="b1f96-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1f96-165"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1f96-165"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b1f96-166">CLSID</span><span class="sxs-lookup"><span data-stu-id="b1f96-166">CLSID</span></span><br/>                    | <span data-ttu-id="b1f96-167">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="b1f96-167">CLSID\_SWbemSink</span></span><br/> <span data-ttu-id="b1f96-168">CLSID \_ SWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="b1f96-168">CLSID\_SWbemSinkEvents</span></span><br/>                           |
| <span data-ttu-id="b1f96-169">IID</span><span class="sxs-lookup"><span data-stu-id="b1f96-169">IID</span></span><br/>                      | <span data-ttu-id="b1f96-170">IID \_ ISWbemSink</span><span class="sxs-lookup"><span data-stu-id="b1f96-170">IID\_ISWbemSink</span></span><br/> <span data-ttu-id="b1f96-171">IID \_ ISWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="b1f96-171">IID\_ISWbemSinkEvents</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="b1f96-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1f96-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1f96-173">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="b1f96-173">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




