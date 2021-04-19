---
description: La \_ méthode ReferencesAsync de SWbemObject fournit une collection de toutes les classes d’association ou instances qui font référence à l’objet actuel. Cette méthode exécute la même fonction que les références WQL de la requête.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: Méthode SWbemObject.ReferencesAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: aa4b85475a0dc9f736254c8f207469a52897b7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529756"
---
# <a name="swbemobjectreferencesasync_-method"></a><span data-ttu-id="0b1ed-104">SWbemObject. ReferencesAsync, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="0b1ed-104">SWbemObject.ReferencesAsync\_ method</span></span>

<span data-ttu-id="0b1ed-105">La **méthode \_ ReferencesAsync** de [**SWbemObject**](swbemobject.md) fournit une collection de toutes les classes d’association ou instances qui font référence à l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-105">The **ReferencesAsync\_** method of [**SWbemObject**](swbemobject.md) supplies a collection of all association classes or instances that refer to the current object.</span></span> <span data-ttu-id="0b1ed-106">Cette méthode exécute la même fonction que les [références WQL de](references-of-statement.md) la requête.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-106">This method performs the same function that the WQL [REFERENCES OF](references-of-statement.md) query performs.</span></span>

<span data-ttu-id="0b1ed-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0b1ed-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b1ed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b1ed-108">Syntax</span></span>


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0b1ed-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b1ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b1ed-110">*objWbemSink* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b1ed-110">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-111">Required.</span></span> <span data-ttu-id="0b1ed-112">Récepteur d’objets qui reçoit les objets de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-112">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="0b1ed-113">*strResultClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0b1ed-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-114">Chaîne qui contient un nom de classe.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-114">String that contains a class name.</span></span> <span data-ttu-id="0b1ed-115">S’il est spécifié, ce paramètre indique que les objets d’association retournés doivent appartenir ou être dérivés de la classe spécifiée dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-115">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0b1ed-116">*strRole* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0b1ed-116">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-117">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-117">String that contains a property name.</span></span> <span data-ttu-id="0b1ed-118">Si ce paramètre est spécifié, ce paramètre indique que les objets d’association retournés doivent être limités à ceux dans lesquels l’objet source joue un rôle spécifique.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-118">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="0b1ed-119">Le nom d’une propriété de référence spécifiée définit le rôle d’une association.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-119">The name of a specified reference property defines the role of an association.</span></span>

</dd> <dt>

<span data-ttu-id="0b1ed-120">*bClassesOnly* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0b1ed-120">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-121">Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-121">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="0b1ed-122">Il s’agit des classes auxquelles appartiennent les objets Association.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-122">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="0b1ed-123">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-123">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0b1ed-124">*bSchemaOnly* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0b1ed-124">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-125">Valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-125">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="0b1ed-126">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-126">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="0b1ed-127">Elle peut uniquement avoir la valeur **true** si l’objet sur lequel cette méthode est appelée est une classe.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-127">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="0b1ed-128">Quand la valeur est **true**, le jeu de points de terminaison retournés représente des classes qui sont correctement associées à la classe source dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-128">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="0b1ed-129">*strRequiredQualifier* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0b1ed-129">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-130">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-130">String that contains a qualifier name.</span></span> <span data-ttu-id="0b1ed-131">S’il est spécifié, ce paramètre indique que les objets Association retournés doivent inclure le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-131">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="0b1ed-132">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0b1ed-132">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-133">Entier spécifiant des indicateurs supplémentaires pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-133">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="0b1ed-134">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-134">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="0b1ed-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="0b1ed-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="0b1ed-136">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**SWbemSink. OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-136">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="0b1ed-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0b1ed-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0b1ed-138">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-138">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="0b1ed-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="0b1ed-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="0b1ed-140">Fait en sorte que Windows Management Instrumentation (WMI) retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-140">Causes Windows Management Instrumentation (WMI) to return class amendment data with the base class definition.</span></span> <span data-ttu-id="0b1ed-141">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="0b1ed-141">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0b1ed-142">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0b1ed-142">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-143">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-143">Typically, this is undefined.</span></span> <span data-ttu-id="0b1ed-144">Dans le cas contraire, il s’agit d’un objet [SWbemNamedValueSet](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-144">Otherwise, this is an [SWbemNamedValueSet](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="0b1ed-145">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="0b1ed-146">*objWbemAsyncContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0b1ed-146">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-147">Il s’agit d’un objet [SWbemNamedValueSet](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-147">This is an [SWbemNamedValueSet](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="0b1ed-148">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="0b1ed-149">Pour utiliser ce paramètre, créez un objet SWbemNamedValueSet et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-149">To use this parameter, create an SWbemNamedValueSet object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="0b1ed-150">Cet objet SWbemNamedValueSet est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1ed-150">This SWbemNamedValueSet object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="0b1ed-151">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0b1ed-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b1ed-152">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b1ed-152">Return value</span></span>

<span data-ttu-id="0b1ed-153">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-153">This method does not return a value.</span></span> <span data-ttu-id="0b1ed-154">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-154">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="0b1ed-155">Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1ed-155">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b1ed-156">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0b1ed-156">Error codes</span></span>

<span data-ttu-id="0b1ed-157">À la fin de la **méthode \_ ReferencesAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-157">After the completion of the **ReferencesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="0b1ed-158">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="0b1ed-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-159">L’utilisateur actuel n’est pas autorisé à afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-159">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="0b1ed-160">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0b1ed-160">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-161">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-161">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="0b1ed-162">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="0b1ed-162">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-163">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-163">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="0b1ed-164">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="0b1ed-164">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0b1ed-165">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-165">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b1ed-166">Notes</span><span class="sxs-lookup"><span data-stu-id="0b1ed-166">Remarks</span></span>

<span data-ttu-id="0b1ed-167">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-167">This call returns immediately.</span></span> <span data-ttu-id="0b1ed-168">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-168">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="0b1ed-169">Pour traiter chaque objet lorsqu’il arrive, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1ed-169">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="0b1ed-170">Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="0b1ed-170">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="0b1ed-171">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-171">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="0b1ed-172">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-172">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="0b1ed-173">Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone.</span><span class="sxs-lookup"><span data-stu-id="0b1ed-173">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="0b1ed-174">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0b1ed-174">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="0b1ed-175">Pour plus d’informations sur les références des objets de requête WQL, d’instances source et d’association associés, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0b1ed-175">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1ed-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b1ed-176">Requirements</span></span>



| <span data-ttu-id="0b1ed-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b1ed-177">Requirement</span></span> | <span data-ttu-id="0b1ed-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1ed-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1ed-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b1ed-179">Minimum supported client</span></span><br/> | <span data-ttu-id="0b1ed-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b1ed-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b1ed-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b1ed-181">Minimum supported server</span></span><br/> | <span data-ttu-id="0b1ed-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b1ed-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b1ed-183">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b1ed-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b1ed-184"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b1ed-184"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b1ed-185">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0b1ed-185">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b1ed-186"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0b1ed-186"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0b1ed-187">DLL</span><span class="sxs-lookup"><span data-stu-id="0b1ed-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b1ed-188"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b1ed-188"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b1ed-189">CLSID</span><span class="sxs-lookup"><span data-stu-id="0b1ed-189">CLSID</span></span><br/>                    | <span data-ttu-id="0b1ed-190">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="0b1ed-190">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="0b1ed-191">IID</span><span class="sxs-lookup"><span data-stu-id="0b1ed-191">IID</span></span><br/>                      | <span data-ttu-id="0b1ed-192">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="0b1ed-192">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="0b1ed-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b1ed-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b1ed-194">**M**</span><span class="sxs-lookup"><span data-stu-id="0b1ed-194">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="0b1ed-195">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="0b1ed-195">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="0b1ed-196">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="0b1ed-196">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="0b1ed-197">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="0b1ed-197">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="0b1ed-198">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="0b1ed-198">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

