---
description: Exécute une requête pour recevoir des événements.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: SWbemServices.Exeméthode cNotificationQueryAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524122"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a><span data-ttu-id="0e8df-103">SWbemServices.Exeméthode cNotificationQueryAsync</span><span class="sxs-lookup"><span data-stu-id="0e8df-103">SWbemServices.ExecNotificationQueryAsync method</span></span>

<span data-ttu-id="0e8df-104">La méthode **ExecNotificationQueryAsync** de l’objet [**SWbemServices**](swbemservices.md) exécute une requête pour recevoir des événements.</span><span class="sxs-lookup"><span data-stu-id="0e8df-104">The **ExecNotificationQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="0e8df-105">Cet appel est retourné immédiatement et les résultats et l’État sont retournés à l’appelant via des événements remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="0e8df-105">This call returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="0e8df-106">Les événements spécifiés dans la requête peuvent être des événements intrinsèques Windows Management Instrumentation (WMI), tels que [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), ou des événements extrinsèques, tels que [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) ou [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="0e8df-106">The events that are specified in the query can be intrinsic Windows Management Instrumentation (WMI) events, such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), or extrinsic events, such as [**Win32\_IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span> <span data-ttu-id="0e8df-107">Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="0e8df-107">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="0e8df-108">La méthode est appelée en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0e8df-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="0e8df-109">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0e8df-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="0e8df-110">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0e8df-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e8df-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e8df-111">Syntax</span></span>


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0e8df-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e8df-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e8df-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="0e8df-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8df-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0e8df-114">Required.</span></span> <span data-ttu-id="0e8df-115">Récepteur d’objets qui reçoit la notification d’événements de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0e8df-115">Object sink that receives the notification of events asynchronously.</span></span> <span data-ttu-id="0e8df-116">Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.</span><span class="sxs-lookup"><span data-stu-id="0e8df-116">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="0e8df-117">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="0e8df-117">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="0e8df-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0e8df-118">Required.</span></span> <span data-ttu-id="0e8df-119">Chaîne qui contient le texte de la requête relative aux événements.</span><span class="sxs-lookup"><span data-stu-id="0e8df-119">String that contains the text of the event-related query.</span></span> <span data-ttu-id="0e8df-120">Ce paramètre ne peut pas être vide.</span><span class="sxs-lookup"><span data-stu-id="0e8df-120">This parameter cannot be blank.</span></span> <span data-ttu-id="0e8df-121">Pour plus d’informations sur la création de chaînes de requête WMI, consultez [interrogation avec WQL](querying-with-wql.md) et la référence [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="0e8df-121">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="0e8df-122">*strQueryLanguage* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0e8df-122">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8df-123">Chaîne qui contient le langage de requête à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0e8df-123">String that contains the query language to be used.</span></span> <span data-ttu-id="0e8df-124">S’il est spécifié, cette valeur doit être « WQL ».</span><span class="sxs-lookup"><span data-stu-id="0e8df-124">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="0e8df-125">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0e8df-125">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8df-126">Entier qui détermine le comportement de la requête.</span><span class="sxs-lookup"><span data-stu-id="0e8df-126">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="0e8df-127">Ce paramètre peut être défini sur les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e8df-127">This parameter can be set to the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="0e8df-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="0e8df-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="0e8df-129">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="0e8df-129">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="0e8df-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0e8df-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0e8df-131">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="0e8df-131">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0e8df-132">*objwbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0e8df-132">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8df-133">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="0e8df-133">Typically, this is undefined.</span></span> <span data-ttu-id="0e8df-134">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui sert la demande.</span><span class="sxs-lookup"><span data-stu-id="0e8df-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="0e8df-135">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="0e8df-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="0e8df-136">*objWbemAsyncContext* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0e8df-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8df-137">Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="0e8df-137">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="0e8df-138">Utilisez ce paramètre pour effectuer plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="0e8df-138">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="0e8df-139">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="0e8df-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="0e8df-140">L’objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="0e8df-140">The **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="0e8df-141">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0e8df-141">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e8df-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e8df-142">Return value</span></span>

<span data-ttu-id="0e8df-143">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0e8df-143">This method does not return a value.</span></span> <span data-ttu-id="0e8df-144">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance.</span><span class="sxs-lookup"><span data-stu-id="0e8df-144">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="0e8df-145">Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="0e8df-145">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0e8df-146">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0e8df-146">Error codes</span></span>

<span data-ttu-id="0e8df-147">À la fin de la méthode **ExecNotificationQueryAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur identifiés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="0e8df-147">After the completion of the **ExecNotificationQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes identified in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="0e8df-148">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="0e8df-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="0e8df-149">L’utilisateur actuel n’est pas autorisé à afficher le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="0e8df-149">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="0e8df-150">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0e8df-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0e8df-151">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0e8df-151">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="0e8df-152">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="0e8df-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="0e8df-153">Un paramètre non valide est spécifié.</span><span class="sxs-lookup"><span data-stu-id="0e8df-153">Invalid parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="0e8df-154">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="0e8df-154">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="0e8df-155">La syntaxe de la requête n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0e8df-155">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0e8df-156">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="0e8df-156">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="0e8df-157">Le langage de requête demandé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0e8df-157">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0e8df-158">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="0e8df-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0e8df-159">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0e8df-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e8df-160">Notes</span><span class="sxs-lookup"><span data-stu-id="0e8df-160">Remarks</span></span>

<span data-ttu-id="0e8df-161">La méthode **ExecNotificationQueryAsync** retourne les objets de type d’événement générés par les événements futurs.</span><span class="sxs-lookup"><span data-stu-id="0e8df-161">The **ExecNotificationQueryAsync** method returns event type objects that future events generate.</span></span> <span data-ttu-id="0e8df-162">Les objets d’événement que les demandes **ExecNotificationQueryAsync** peuvent être intrinsèques (par exemple, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ou extrinsèques (par exemple, les événements [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ou SNMP).</span><span class="sxs-lookup"><span data-stu-id="0e8df-162">The event objects that **ExecNotificationQueryAsync** requests can be intrinsic (for example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md)), or extrinsic (for example, [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="0e8df-163">Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="0e8df-163">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="0e8df-164">L’appel à **ExecNotificationQueryAsync** retourne immédiatement.</span><span class="sxs-lookup"><span data-stu-id="0e8df-164">The call to **ExecNotificationQueryAsync** returns immediately.</span></span> <span data-ttu-id="0e8df-165">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="0e8df-165">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="0e8df-166">Pour traiter chaque objet lorsqu’il est retourné, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="0e8df-166">To process each object when it is returned, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="0e8df-167">Une fois tous les objets retournés, effectuez le traitement final pour implémenter le *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="0e8df-167">After all the objects are returned, perform the final processing to implement the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="0e8df-168">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="0e8df-168">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="0e8df-169">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="0e8df-169">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="0e8df-170">Pour éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="0e8df-170">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="0e8df-171">Il existe des limites concernant le nombre de mots clés **and** et **or** qui peuvent être utilisés dans les requêtes WQL.</span><span class="sxs-lookup"><span data-stu-id="0e8df-171">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="0e8df-172">Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne la valeur HRESULT Asan **HRESULT** du code d’erreur de **\_ \_ \_ violation de quota E WBEM** .</span><span class="sxs-lookup"><span data-stu-id="0e8df-172">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code asan **HRESULT** value.</span></span> <span data-ttu-id="0e8df-173">La limite des mots clés WQL dépend de la complexité de la requête.</span><span class="sxs-lookup"><span data-stu-id="0e8df-173">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="0e8df-174">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e8df-174">Examples</span></span>

<span data-ttu-id="0e8df-175">L’exemple de code VBScript suivant montre un script qui attend une notification d’événement WMI indiquant qu’un processus s’est terminé.</span><span class="sxs-lookup"><span data-stu-id="0e8df-175">The following VBScript code example shows a script that is waiting for a WMI event notification that indicates that a process has terminated.</span></span> <span data-ttu-id="0e8df-176">Il attend un événement intrinsèque WMI, une instance de la classe d’événements [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="0e8df-176">It is waiting for a WMI intrinsic event, an instance of the event class [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span> <span data-ttu-id="0e8df-177">**\_ \_ InstanceDeletionEvent** doit représenter la suppression d’une instance de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="0e8df-177">The **\_\_InstanceDeletionEvent** must represent the deletion of an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="0e8df-178">Pour plus d’informations sur les événements intrinsèques WMI, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="0e8df-178">For more information about WMI intrinsic events, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="0e8df-179">Le script suivant s’exécute indéfiniment jusqu’à ce que l’ordinateur soit redémarré, que WMI soit arrêté ou que le script soit arrêté.</span><span class="sxs-lookup"><span data-stu-id="0e8df-179">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="0e8df-180">Pour arrêter le script manuellement, utilisez le gestionnaire des tâches pour arrêter le processus.</span><span class="sxs-lookup"><span data-stu-id="0e8df-180">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="0e8df-181">Pour l’arrêter par programmation, utilisez la méthode [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) dans la classe de \_ processus Win32.</span><span class="sxs-lookup"><span data-stu-id="0e8df-181">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0e8df-182">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e8df-182">Requirements</span></span>



| <span data-ttu-id="0e8df-183">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e8df-183">Requirement</span></span> | <span data-ttu-id="0e8df-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e8df-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8df-185">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e8df-185">Minimum supported client</span></span><br/> | <span data-ttu-id="0e8df-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e8df-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e8df-187">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e8df-187">Minimum supported server</span></span><br/> | <span data-ttu-id="0e8df-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e8df-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e8df-189">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e8df-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e8df-190"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e8df-190"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e8df-191">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0e8df-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e8df-192"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e8df-192"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e8df-193">DLL</span><span class="sxs-lookup"><span data-stu-id="0e8df-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e8df-194"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e8df-194"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0e8df-195">CLSID</span><span class="sxs-lookup"><span data-stu-id="0e8df-195">CLSID</span></span><br/>                    | <span data-ttu-id="0e8df-196">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="0e8df-196">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="0e8df-197">IID</span><span class="sxs-lookup"><span data-stu-id="0e8df-197">IID</span></span><br/>                      | <span data-ttu-id="0e8df-198">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="0e8df-198">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="0e8df-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e8df-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e8df-200">**M**</span><span class="sxs-lookup"><span data-stu-id="0e8df-200">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="0e8df-201">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="0e8df-201">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="0e8df-202">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="0e8df-202">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
</dt> <dt>

[<span data-ttu-id="0e8df-203">Inscription pour les événements du Registre système</span><span class="sxs-lookup"><span data-stu-id="0e8df-203">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> <dt>

[<span data-ttu-id="0e8df-204">Détermination du type d’événement à recevoir</span><span class="sxs-lookup"><span data-stu-id="0e8df-204">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="0e8df-205">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="0e8df-205">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="0e8df-206">Définition de la sécurité sur un appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="0e8df-206">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

