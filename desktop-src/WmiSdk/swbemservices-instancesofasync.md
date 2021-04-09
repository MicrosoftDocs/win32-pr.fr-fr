---
description: Récupère les instances d’une classe spécifiée en fonction des critères spécifiés par l’utilisateur.
ms.assetid: 631cd749-9a39-4606-9a38-0b4bb5b4b2cd
ms.tgt_platform: multiple
title: SWbemServices. InstancesOfAsync, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c518cb38a0ecb221f4fcb0d0e7f9ce6dfc226ba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863758"
---
# <a name="swbemservicesinstancesofasync-method"></a><span data-ttu-id="d1c8c-103">SWbemServices. InstancesOfAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="d1c8c-103">SWbemServices.InstancesOfAsync method</span></span>

<span data-ttu-id="d1c8c-104">La méthode **InstancesOfAsync** de l’objet [**SWbemServices**](swbemservices.md) récupère les instances d’une classe spécifiée en fonction des critères spécifiés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-104">The **InstancesOfAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves instances of a specified class according to user-specified criteria.</span></span>

<span data-ttu-id="d1c8c-105">La méthode est appelée en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-105">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="d1c8c-106">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d1c8c-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d1c8c-107">Pour plus d’explications sur la syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d1c8c-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c8c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1c8c-108">Syntax</span></span>


```VB
SWbemServices.InstancesOfAsync( _
  ByVal ObjWbemSink, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d1c8c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1c8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c8c-110">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="d1c8c-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c8c-111">Récepteur d’objets qui reçoit les instances de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-111">Object sink that receives the instances asynchronously.</span></span> <span data-ttu-id="d1c8c-112">Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-112">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="d1c8c-113">*strClass*</span><span class="sxs-lookup"><span data-stu-id="d1c8c-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c8c-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-114">Required.</span></span> <span data-ttu-id="d1c8c-115">Chaîne qui contient le nom de la classe pour les instances de votre choix.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-115">String that contains the name of the class for the instances that you want.</span></span> <span data-ttu-id="d1c8c-116">Ce paramètre ne peut pas être vide.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-116">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="d1c8c-117">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d1c8c-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c8c-118">Détermine la profondeur de l’énumération des appels, et indique si l’appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-118">Determines the depth of the call enumeration, and whether or not the call returns immediately.</span></span> <span data-ttu-id="d1c8c-119">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="d1c8c-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d1c8c-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d1c8c-121">Force l’énumération à inclure uniquement les sous-classes immédiates de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-121">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="d1c8c-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d1c8c-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d1c8c-123">Valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-123">Default for this parameter.</span></span> <span data-ttu-id="d1c8c-124">Cette valeur force l’énumération à inclure toutes les classes dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-124">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="d1c8c-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d1c8c-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d1c8c-126">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-126">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="d1c8c-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d1c8c-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d1c8c-128">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-128">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="d1c8c-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d1c8c-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d1c8c-130">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-130">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="d1c8c-131">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="d1c8c-131">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d1c8c-132">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d1c8c-132">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c8c-133">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-133">Typically, this is undefined.</span></span> <span data-ttu-id="d1c8c-134">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d1c8c-135">Un fournisseur qui prend en charge ou requiert des informations de contexte doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-135">A provider that supports or requires context information information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="d1c8c-136">*objWbemAsyncContext* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d1c8c-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c8c-137">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-137">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="d1c8c-138">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-138">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="d1c8c-139">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="d1c8c-140">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c8c-140">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c8c-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1c8c-141">Return value</span></span>

<span data-ttu-id="d1c8c-142">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-142">This method does not return a value.</span></span> <span data-ttu-id="d1c8c-143">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-143">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="d1c8c-144">Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c8c-144">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d1c8c-145">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d1c8c-145">Error codes</span></span>

<span data-ttu-id="d1c8c-146">À la fin de la méthode **InstancesOfAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-146">Upon the completion of the **InstancesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d1c8c-147">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d1c8c-147">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d1c8c-148">L’utilisateur actuel n’a pas l’autorisation d’afficher les instances de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-148">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="d1c8c-149">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d1c8c-149">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d1c8c-150">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-150">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d1c8c-151">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="d1c8c-151">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="d1c8c-152">La classe spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-152">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d1c8c-153">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d1c8c-153">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d1c8c-154">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-154">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d1c8c-155">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d1c8c-155">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d1c8c-156">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-156">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1c8c-157">Notes</span><span class="sxs-lookup"><span data-stu-id="d1c8c-157">Remarks</span></span>

<span data-ttu-id="d1c8c-158">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-158">This call returns immediately.</span></span> <span data-ttu-id="d1c8c-159">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-159">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d1c8c-160">Pour traiter chaque objet lorsqu’il retourne, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c8c-160">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="d1c8c-161">Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c8c-161">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="d1c8c-162">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-162">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d1c8c-163">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-163">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d1c8c-164">Pour éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="d1c8c-164">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="d1c8c-165">La méthode **InstancesOfAsync** fonctionne uniquement pour les objets de classe.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-165">The **InstancesOfAsync** method only works for class objects.</span></span> <span data-ttu-id="d1c8c-166">Il n’y a pas d’erreur pour que l’énumérateur retourné ait des éléments nuls (0).</span><span class="sxs-lookup"><span data-stu-id="d1c8c-166">It is not an error for the returned enumerator to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c8c-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1c8c-167">Requirements</span></span>



| <span data-ttu-id="d1c8c-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1c8c-168">Requirement</span></span> | <span data-ttu-id="d1c8c-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1c8c-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c8c-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1c8c-170">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c8c-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1c8c-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1c8c-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1c8c-172">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c8c-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1c8c-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1c8c-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1c8c-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1c8c-175"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1c8c-175"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1c8c-176">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d1c8c-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1c8c-177"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1c8c-177"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1c8c-178">DLL</span><span class="sxs-lookup"><span data-stu-id="d1c8c-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1c8c-179"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1c8c-179"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1c8c-180">CLSID</span><span class="sxs-lookup"><span data-stu-id="d1c8c-180">CLSID</span></span><br/>                    | <span data-ttu-id="d1c8c-181">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="d1c8c-181">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="d1c8c-182">IID</span><span class="sxs-lookup"><span data-stu-id="d1c8c-182">IID</span></span><br/>                      | <span data-ttu-id="d1c8c-183">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="d1c8c-183">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d1c8c-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1c8c-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c8c-185">**M**</span><span class="sxs-lookup"><span data-stu-id="d1c8c-185">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="d1c8c-186">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="d1c8c-186">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

