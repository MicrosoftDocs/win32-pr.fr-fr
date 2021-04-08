---
description: La \_ méthode InstancesAsync de SWbemObject fournit de manière asynchrone les instances de l’objet de classe actuel. Cette méthode implémente une requête simple. Les requêtes plus complexes peuvent nécessiter l’utilisation de SWbemServices.ExecQuery.
ms.assetid: d10fcbbf-6110-4152-8201-db43dc7a3c14
ms.tgt_platform: multiple
title: Méthode SWbemObject.InstancesAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 800e28184593e339f739fb52d488803666f552c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863781"
---
# <a name="swbemobjectinstancesasync_-method"></a><span data-ttu-id="6c156-105">SWbemObject. InstancesAsync, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="6c156-105">SWbemObject.InstancesAsync\_ method</span></span>

<span data-ttu-id="6c156-106">La **méthode \_ InstancesAsync** de [**SWbemObject**](swbemobject.md) fournit de manière asynchrone les instances de l’objet de classe actuel.</span><span class="sxs-lookup"><span data-stu-id="6c156-106">The **InstancesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the instances of the current class object.</span></span> <span data-ttu-id="6c156-107">Cette méthode implémente une requête simple.</span><span class="sxs-lookup"><span data-stu-id="6c156-107">This method implements a simple query.</span></span> <span data-ttu-id="6c156-108">Les requêtes plus complexes peuvent nécessiter l’utilisation de [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="6c156-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="6c156-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6c156-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c156-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c156-110">Syntax</span></span>


```VB
SWbemObject.InstancesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6c156-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c156-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c156-112">*objWbemSink* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c156-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c156-113">Récepteur d’objets qui retourne les instances.</span><span class="sxs-lookup"><span data-stu-id="6c156-113">Object sink that returns the instances.</span></span>

</dd> <dt>

<span data-ttu-id="6c156-114">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6c156-114">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c156-115">Entier qui détermine le comportement de l’appel.</span><span class="sxs-lookup"><span data-stu-id="6c156-115">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="6c156-116">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6c156-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="6c156-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="6c156-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="6c156-118">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**SWbemSink. OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="6c156-118">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="6c156-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6c156-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6c156-120">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="6c156-120">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="6c156-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="6c156-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="6c156-122">Fait en sorte que WMI retourne les descriptions des propriétés et des classes localisées.</span><span class="sxs-lookup"><span data-stu-id="6c156-122">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="6c156-123">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="6c156-123">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6c156-124">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6c156-124">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c156-125">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="6c156-125">Typically, this is undefined.</span></span> <span data-ttu-id="6c156-126">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="6c156-126">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="6c156-127">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="6c156-127">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="6c156-128">*objWbemAsyncContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6c156-128">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6c156-129">Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="6c156-129">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="6c156-130">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="6c156-130">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="6c156-131">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="6c156-131">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="6c156-132">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="6c156-132">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="6c156-133">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6c156-133">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c156-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c156-134">Return value</span></span>

<span data-ttu-id="6c156-135">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6c156-135">This method does not return a value.</span></span> <span data-ttu-id="6c156-136">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance.</span><span class="sxs-lookup"><span data-stu-id="6c156-136">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="6c156-137">Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="6c156-137">After the last instance, the object sink will receive an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6c156-138">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6c156-138">Error codes</span></span>

<span data-ttu-id="6c156-139">À la fin de la **méthode \_ InstancesAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="6c156-139">After the completion of the **InstancesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6c156-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="6c156-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="6c156-141">L’utilisateur actuel n’est pas autorisé à afficher les instances de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6c156-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="6c156-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6c156-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6c156-143">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6c156-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6c156-144">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="6c156-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="6c156-145">La classe spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6c156-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6c156-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="6c156-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6c156-147">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6c156-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6c156-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6c156-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6c156-149">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="6c156-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c156-150">Notes</span><span class="sxs-lookup"><span data-stu-id="6c156-150">Remarks</span></span>

<span data-ttu-id="6c156-151">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6c156-151">This call returns immediately.</span></span> <span data-ttu-id="6c156-152">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="6c156-152">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="6c156-153">Pour traiter chaque objet lorsqu’il arrive, créez un *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="6c156-153">To process each object when it arrives, create an *objWbemSink*.</span></span> <span data-ttu-id="6c156-154">Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="6c156-154">[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="6c156-155">Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="6c156-155">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.</span></span> <span data-ttu-id="6c156-156">Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="6c156-156">[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="6c156-157">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="6c156-157">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="6c156-158">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="6c156-158">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="6c156-159">Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone.</span><span class="sxs-lookup"><span data-stu-id="6c156-159">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="6c156-160">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6c156-160">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="6c156-161">La **méthode \_ InstancesAsync** fonctionne uniquement pour les objets de classe.</span><span class="sxs-lookup"><span data-stu-id="6c156-161">The **InstancesAsync\_** method only works for class objects.</span></span> <span data-ttu-id="6c156-162">Il n’y a pas d’erreur pour que la collection retournée ait des éléments nuls (0).</span><span class="sxs-lookup"><span data-stu-id="6c156-162">It is not an error for the returned collection to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c156-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c156-163">Requirements</span></span>



| <span data-ttu-id="6c156-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c156-164">Requirement</span></span> | <span data-ttu-id="6c156-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c156-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c156-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c156-166">Minimum supported client</span></span><br/> | <span data-ttu-id="6c156-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c156-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c156-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c156-168">Minimum supported server</span></span><br/> | <span data-ttu-id="6c156-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c156-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c156-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c156-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c156-171"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c156-171"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c156-172">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6c156-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="6c156-173"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6c156-173"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6c156-174">DLL</span><span class="sxs-lookup"><span data-stu-id="6c156-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c156-175"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c156-175"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6c156-176">CLSID</span><span class="sxs-lookup"><span data-stu-id="6c156-176">CLSID</span></span><br/>                    | <span data-ttu-id="6c156-177">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="6c156-177">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="6c156-178">IID</span><span class="sxs-lookup"><span data-stu-id="6c156-178">IID</span></span><br/>                      | <span data-ttu-id="6c156-179">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="6c156-179">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="6c156-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c156-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c156-181">**M**</span><span class="sxs-lookup"><span data-stu-id="6c156-181">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="6c156-182">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="6c156-182">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

