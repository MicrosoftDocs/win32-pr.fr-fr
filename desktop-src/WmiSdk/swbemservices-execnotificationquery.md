---
description: Exécute une requête pour recevoir des événements. L’appel est retourné immédiatement.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: SWbemServices.Exeméthode cNotificationQuery (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533924"
---
# <a name="swbemservicesexecnotificationquery-method"></a><span data-ttu-id="69da9-104">SWbemServices.Exeméthode cNotificationQuery</span><span class="sxs-lookup"><span data-stu-id="69da9-104">SWbemServices.ExecNotificationQuery method</span></span>

<span data-ttu-id="69da9-105">La méthode **ExecNotificationQuery** de l’objet [**SWbemServices**](swbemservices.md) exécute une requête pour recevoir des événements.</span><span class="sxs-lookup"><span data-stu-id="69da9-105">The **ExecNotificationQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="69da9-106">L’appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="69da9-106">The call returns immediately.</span></span> <span data-ttu-id="69da9-107">L’utilisateur peut interroger l’énumérateur retourné pour les événements à mesure qu’ils arrivent.</span><span class="sxs-lookup"><span data-stu-id="69da9-107">The user can poll the returned enumerator for events as they arrive.</span></span>

<span data-ttu-id="69da9-108">La méthode est appelée en mode semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="69da9-108">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="69da9-109">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="69da9-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="69da9-110">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="69da9-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="69da9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69da9-111">Syntax</span></span>


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="69da9-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69da9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69da9-113">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="69da9-113">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="69da9-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="69da9-114">Required.</span></span> <span data-ttu-id="69da9-115">Chaîne qui contient le texte de la requête relative aux événements.</span><span class="sxs-lookup"><span data-stu-id="69da9-115">String that contains the text of the event-related query.</span></span> <span data-ttu-id="69da9-116">Ce paramètre ne peut pas être vide.</span><span class="sxs-lookup"><span data-stu-id="69da9-116">This parameter cannot be blank.</span></span> <span data-ttu-id="69da9-117">Pour plus d’informations sur la création de chaînes de requête WMI, consultez [interrogation avec WQL](querying-with-wql.md) et la référence [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="69da9-117">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="69da9-118">*strQueryLanguage* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="69da9-118">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="69da9-119">Chaîne qui contient le langage de requête à utiliser.</span><span class="sxs-lookup"><span data-stu-id="69da9-119">String that contains the query language to be used.</span></span> <span data-ttu-id="69da9-120">S’il est spécifié, cette valeur doit être « WQL ».</span><span class="sxs-lookup"><span data-stu-id="69da9-120">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="69da9-121">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="69da9-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="69da9-122">Il s’agit d’un entier qui détermine le comportement de la requête.</span><span class="sxs-lookup"><span data-stu-id="69da9-122">This is an integer that determines the behavior of the query.</span></span> <span data-ttu-id="69da9-123">La valeur par défaut est **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="69da9-123">The default value is **wbemFlagReturnImmediately** + **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="69da9-124">Si vous spécifiez ce paramètre, ce paramètre doit être défini à la fois sur **wbemFlagReturnImmediately** et **wbemFlagForwardOnly** , sinon l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="69da9-124">If you specify this parameter, this parameter must be set to both **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** or the call fails.</span></span> <span data-ttu-id="69da9-125">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="69da9-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="69da9-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="69da9-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="69da9-127">Entraîne le retour d’un énumérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="69da9-127">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="69da9-128">Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="69da9-128">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="69da9-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="69da9-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="69da9-130">Provoque le retour immédiat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="69da9-130">Causes the call to return immediately.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="69da9-131">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="69da9-131">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="69da9-132">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="69da9-132">Typically, this is undefined.</span></span> <span data-ttu-id="69da9-133">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="69da9-133">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="69da9-134">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="69da9-134">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69da9-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69da9-135">Return value</span></span>

<span data-ttu-id="69da9-136">Si aucune erreur ne se produit, cette méthode retourne un objet [**SWbemEventSource**](swbemeventsource.md) .</span><span class="sxs-lookup"><span data-stu-id="69da9-136">If no error occurs, this method returns an [**SWbemEventSource**](swbemeventsource.md) object.</span></span> <span data-ttu-id="69da9-137">Vous pouvez appeler la méthode [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) pour récupérer les événements à mesure qu’ils arrivent.</span><span class="sxs-lookup"><span data-stu-id="69da9-137">You can call the [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="69da9-138">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="69da9-138">Error codes</span></span>

<span data-ttu-id="69da9-139">À la fin de la méthode **ExecNotificationQuery** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="69da9-139">After the completion of the **ExecNotificationQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="69da9-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="69da9-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="69da9-141">L’utilisateur actuel n’est pas autorisé à afficher le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="69da9-141">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="69da9-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="69da9-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="69da9-143">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="69da9-143">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="69da9-144">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="69da9-144">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="69da9-145">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="69da9-145">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="69da9-146">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="69da9-146">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="69da9-147">La syntaxe de la requête n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="69da9-147">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="69da9-148">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="69da9-148">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="69da9-149">Le langage de la requête demandé n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="69da9-149">The requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="69da9-150">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="69da9-150">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="69da9-151">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="69da9-151">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69da9-152">Notes</span><span class="sxs-lookup"><span data-stu-id="69da9-152">Remarks</span></span>

<span data-ttu-id="69da9-153">Contrairement à la méthode [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) , **ExecNotificationQuery** retourne les objets de type d’événement qui sont générés par des événements futurs plutôt que par des objets existants.</span><span class="sxs-lookup"><span data-stu-id="69da9-153">Unlike the [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method, **ExecNotificationQuery** returns event type objects that are generated by future events rather than existing objects.</span></span> <span data-ttu-id="69da9-154">Les objets d’événement que les demandes **ExecNotificationQuery** peuvent être intrinsèques (par exemple, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ou extrinsèques (tels que les événements de fournisseur de Registre comme les événements [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ou SNMP).</span><span class="sxs-lookup"><span data-stu-id="69da9-154">The event objects that **ExecNotificationQuery** requests can either be intrinsic (such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) or extrinsic (such as registry provider events like [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="69da9-155">Pour plus d’informations, consultez [détermination du type d’événement pour la réception et la](determining-the-type-of-event-to-receive.md) [réception des notifications d’événements](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="69da9-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md) and [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

<span data-ttu-id="69da9-156">Il existe des limites concernant le nombre de mots clés **and** et **or** qui peuvent être utilisés dans les requêtes WQL.</span><span class="sxs-lookup"><span data-stu-id="69da9-156">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="69da9-157">Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne le code d’erreur de  **\_ \_ \_ violation de quota E WBEM** en tant que valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="69da9-157">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="69da9-158">La limite des mots clés WQL dépend de la complexité de la requête.</span><span class="sxs-lookup"><span data-stu-id="69da9-158">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="69da9-159">Exemples</span><span class="sxs-lookup"><span data-stu-id="69da9-159">Examples</span></span>

<span data-ttu-id="69da9-160">L’exemple de code VBScript suivant surveille les modifications apportées aux volumes sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="69da9-160">The following VBScript code example monitors changes to volumes on a local computer.</span></span> <span data-ttu-id="69da9-161">Notez que [**Win32 \_ VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) est un événement extrinsèque qui est défini par un fournisseur qui n’est pas un événement intrinsèque défini par WMI.</span><span class="sxs-lookup"><span data-stu-id="69da9-161">Note that [**Win32\_VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) is an extrinsic event that is defined by a provider not an intrinsic WMI-defined event.</span></span> <span data-ttu-id="69da9-162">Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="69da9-162">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



<span data-ttu-id="69da9-163">L’exemple de code VBScript suivant surveille la suppression des processus.</span><span class="sxs-lookup"><span data-stu-id="69da9-163">The following VBScript code example monitors process deletion.</span></span> <span data-ttu-id="69da9-164">Si vous supprimez un processus dans le gestionnaire des tâches ou fermez une application, le script affiche un message.</span><span class="sxs-lookup"><span data-stu-id="69da9-164">If you delete a process in Task Manager or close an application, then the script displays a message.</span></span> <span data-ttu-id="69da9-165">Notez que ce script interroge un événement intrinsèque défini par WMI- [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="69da9-165">Note that this script queries an intrinsic event that is defined by WMI - [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span>


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a><span data-ttu-id="69da9-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69da9-166">Requirements</span></span>



| <span data-ttu-id="69da9-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69da9-167">Requirement</span></span> | <span data-ttu-id="69da9-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="69da9-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69da9-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69da9-169">Minimum supported client</span></span><br/> | <span data-ttu-id="69da9-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69da9-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69da9-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69da9-171">Minimum supported server</span></span><br/> | <span data-ttu-id="69da9-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69da9-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69da9-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="69da9-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="69da9-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="69da9-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="69da9-175">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="69da9-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="69da9-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="69da9-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="69da9-177">DLL</span><span class="sxs-lookup"><span data-stu-id="69da9-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69da9-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69da9-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="69da9-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="69da9-179">CLSID</span></span><br/>                    | <span data-ttu-id="69da9-180">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="69da9-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="69da9-181">IID</span><span class="sxs-lookup"><span data-stu-id="69da9-181">IID</span></span><br/>                      | <span data-ttu-id="69da9-182">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="69da9-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="69da9-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69da9-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69da9-184">**M**</span><span class="sxs-lookup"><span data-stu-id="69da9-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="69da9-185">**SWbemEventSource.NextEvent**</span><span class="sxs-lookup"><span data-stu-id="69da9-185">**SWbemEventSource.NextEvent**</span></span>](swbemeventsource-nextevent.md)
</dt> <dt>

[<span data-ttu-id="69da9-186">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="69da9-186">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="69da9-187">Réception d’un événement WMI</span><span class="sxs-lookup"><span data-stu-id="69da9-187">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> <dt>

[<span data-ttu-id="69da9-188">Interrogation avec WQL</span><span class="sxs-lookup"><span data-stu-id="69da9-188">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="69da9-189">WQL (SQL pour WMI)</span><span class="sxs-lookup"><span data-stu-id="69da9-189">WQL (SQL for WMI)</span></span>](wql-sql-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="69da9-190">Détermination du type d’événement à recevoir</span><span class="sxs-lookup"><span data-stu-id="69da9-190">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

