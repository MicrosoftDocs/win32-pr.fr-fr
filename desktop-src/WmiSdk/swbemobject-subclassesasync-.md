---
description: La \_ méthode SubclassesAsync de SWbemObject fournit de manière asynchrone les sous-classes de l’objet actuel, qui doit être une classe.
ms.assetid: 14d4a609-3aa4-49bd-bea4-6a71bc24d9dd
ms.tgt_platform: multiple
title: Méthode SWbemObject.SubclassesAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6e922953e9f25aae2e47ea572678790b1228a581
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210547"
---
# <a name="swbemobjectsubclassesasync_-method"></a><span data-ttu-id="4b929-103">SWbemObject. SubclassesAsync, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="4b929-103">SWbemObject.SubclassesAsync\_ method</span></span>

<span data-ttu-id="4b929-104">La **méthode \_ SubclassesAsync** de [**SWbemObject**](swbemobject.md) fournit de manière asynchrone les sous-classes de l’objet actuel, qui doit être une classe.</span><span class="sxs-lookup"><span data-stu-id="4b929-104">The **SubclassesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the subclasses of the current object, which must be a class.</span></span>

<span data-ttu-id="4b929-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4b929-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b929-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b929-106">Syntax</span></span>


```VB
SWbemObject.SubclassesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4b929-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b929-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b929-108">*objWbemSink* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b929-108">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b929-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4b929-109">Required.</span></span> <span data-ttu-id="4b929-110">Récepteur d’objets qui reçoit les objets de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="4b929-110">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="4b929-111">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4b929-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b929-112">Détermine le détail de l’énumération des appels.</span><span class="sxs-lookup"><span data-stu-id="4b929-112">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="4b929-113">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b929-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="4b929-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="4b929-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4b929-115">Force l’énumération récursive dans toutes les sous-classes dérivées de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4b929-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="4b929-116">La classe parent elle-même n’est pas retournée dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="4b929-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="4b929-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="4b929-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="4b929-118">Valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="4b929-118">Default for this parameter.</span></span> <span data-ttu-id="4b929-119">Elle force l’énumération à inclure uniquement les sous-classes immédiates de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4b929-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="4b929-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="4b929-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="4b929-121">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**SWbemSink. OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="4b929-121">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="4b929-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="4b929-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4b929-123">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="4b929-123">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="4b929-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="4b929-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="4b929-125">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="4b929-125">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="4b929-126">Pour plus d’informations sur les qualificateurs modifiés, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="4b929-126">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4b929-127">*objWbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4b929-127">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b929-128">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="4b929-128">Typically, this is undefined.</span></span> <span data-ttu-id="4b929-129">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="4b929-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="4b929-130">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="4b929-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="4b929-131">*objWbemAsyncContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4b929-131">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b929-132">Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="4b929-132">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="4b929-133">Utilisez ce paramètre lorsque vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="4b929-133">Use this parameter when you make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="4b929-134">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="4b929-134">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="4b929-135">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="4b929-135">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="4b929-136">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4b929-136">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b929-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b929-137">Return value</span></span>

<span data-ttu-id="4b929-138">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4b929-138">This method does not return a value.</span></span> <span data-ttu-id="4b929-139">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) pour chaque instance.</span><span class="sxs-lookup"><span data-stu-id="4b929-139">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event for each instance.</span></span> <span data-ttu-id="4b929-140">Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="4b929-140">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4b929-141">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4b929-141">Error codes</span></span>

<span data-ttu-id="4b929-142">À la fin de la **méthode \_ SubclassesAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="4b929-142">After the completion of the **SubclassesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4b929-143">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="4b929-143">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="4b929-144">L’utilisateur actuel n’est pas autorisé à afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="4b929-144">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="4b929-145">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="4b929-145">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4b929-146">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4b929-146">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4b929-147">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="4b929-147">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="4b929-148">La classe spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4b929-148">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="4b929-149">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="4b929-149">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4b929-150">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="4b929-150">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="4b929-151">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="4b929-151">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="4b929-152">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="4b929-152">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b929-153">Notes</span><span class="sxs-lookup"><span data-stu-id="4b929-153">Remarks</span></span>

<span data-ttu-id="4b929-154">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4b929-154">This call returns immediately.</span></span> <span data-ttu-id="4b929-155">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="4b929-155">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="4b929-156">Pour traiter chaque objet lorsqu’il arrive, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="4b929-156">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="4b929-157">Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="4b929-157">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="4b929-158">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="4b929-158">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="4b929-159">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="4b929-159">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="4b929-160">Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone.</span><span class="sxs-lookup"><span data-stu-id="4b929-160">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="4b929-161">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4b929-161">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="4b929-162">Il est recommandé que les scripts vérifient la source de l’appel à l’aide d’un paramètre *objWbemAsyncContext* .</span><span class="sxs-lookup"><span data-stu-id="4b929-162">It is recommended that scripts verify the source of the call by using an *objWbemAsyncContext* parameter.</span></span>

<span data-ttu-id="4b929-163">Il n’y a pas d’erreur pour que la collection retournée n’ait aucun élément, s’il n’existe aucune sous-classe de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="4b929-163">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="4b929-164">La **méthode \_ SubclassesAsync** fonctionne uniquement pour les objets de classe.</span><span class="sxs-lookup"><span data-stu-id="4b929-164">The **SubclassesAsync\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b929-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b929-165">Requirements</span></span>



| <span data-ttu-id="4b929-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b929-166">Requirement</span></span> | <span data-ttu-id="4b929-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b929-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b929-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b929-168">Minimum supported client</span></span><br/> | <span data-ttu-id="4b929-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b929-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b929-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b929-170">Minimum supported server</span></span><br/> | <span data-ttu-id="4b929-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b929-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b929-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b929-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b929-173"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b929-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b929-174">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4b929-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b929-175"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4b929-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4b929-176">DLL</span><span class="sxs-lookup"><span data-stu-id="4b929-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b929-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b929-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4b929-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="4b929-178">CLSID</span></span><br/>                    | <span data-ttu-id="4b929-179">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="4b929-179">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="4b929-180">IID</span><span class="sxs-lookup"><span data-stu-id="4b929-180">IID</span></span><br/>                      | <span data-ttu-id="4b929-181">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="4b929-181">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="4b929-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b929-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b929-183">**M**</span><span class="sxs-lookup"><span data-stu-id="4b929-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="4b929-184">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="4b929-184">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="4b929-185">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="4b929-185">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> </dl>

 

