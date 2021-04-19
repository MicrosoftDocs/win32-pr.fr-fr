---
description: Retourne toutes les classes d’association ou instances qui font référence à une instance ou une classe source spécifique.
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.tgt_platform: multiple
title: SWbemServices. ReferencesToAsync, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 64a8b9b336a1e7aa6007b17d2e878f1ace5e6163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524971"
---
# <a name="swbemservicesreferencestoasync-method"></a><span data-ttu-id="eb10c-103">SWbemServices. ReferencesToAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="eb10c-103">SWbemServices.ReferencesToAsync method</span></span>

<span data-ttu-id="eb10c-104">La méthode **ReferencesToAsync** de l’objet [**SWbemServices**](swbemservices.md) retourne toutes les classes d’association ou les instances qui font référence à une classe ou une instance source spécifique.</span><span class="sxs-lookup"><span data-stu-id="eb10c-104">The **ReferencesToAsync** method of the [**SWbemServices**](swbemservices.md) object returns all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="eb10c-105">Cette méthode exécute la même fonction que les [références de](references-of-statement.md) la requête WQL.</span><span class="sxs-lookup"><span data-stu-id="eb10c-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="eb10c-106">Pour plus d’informations sur le mode asynchrone, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="eb10c-106">For more information about the asynchronous mode, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="eb10c-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eb10c-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb10c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb10c-108">Syntax</span></span>


```VB
SWbemServices.ReferencesToAsync( _
  ByVal ObjWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="eb10c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb10c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb10c-110">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="eb10c-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="eb10c-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="eb10c-111">Required.</span></span> <span data-ttu-id="eb10c-112">Récepteur d’objets qui reçoit les objets de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="eb10c-112">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="eb10c-113">Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.</span><span class="sxs-lookup"><span data-stu-id="eb10c-113">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-114">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="eb10c-114">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="eb10c-115">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="eb10c-115">Required.</span></span> <span data-ttu-id="eb10c-116">Chaîne qui contient le chemin d’accès de l’objet de la source pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="eb10c-116">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="eb10c-117">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="eb10c-117">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-118">*strResultClass* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb10c-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-119">Chaîne qui contient un nom de classe.</span><span class="sxs-lookup"><span data-stu-id="eb10c-119">String that contains a class name.</span></span> <span data-ttu-id="eb10c-120">Si ce paramètre est spécifié, ce paramètre indique que les objets d’association retournés doivent appartenir à la classe spécifiée dans ce paramètre ou en être dérivés.</span><span class="sxs-lookup"><span data-stu-id="eb10c-120">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-121">*strRole* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb10c-121">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-122">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="eb10c-122">String that contains a property name.</span></span> <span data-ttu-id="eb10c-123">Si ce paramètre est spécifié, ce paramètre indique que les objets d’association retournés doivent être limités à ceux dans lesquels l’objet source joue un rôle spécifique.</span><span class="sxs-lookup"><span data-stu-id="eb10c-123">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="eb10c-124">Le rôle est défini par le nom d’une propriété de référence spécifiée d’une association.</span><span class="sxs-lookup"><span data-stu-id="eb10c-124">The role is defined by the name of a specified reference property of an association.</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-125">*bClassesOnly* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb10c-125">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-126">Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes.</span><span class="sxs-lookup"><span data-stu-id="eb10c-126">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="eb10c-127">Il s’agit des classes auxquelles appartiennent les objets Association.</span><span class="sxs-lookup"><span data-stu-id="eb10c-127">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="eb10c-128">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="eb10c-128">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-129">*bSchemaOnly* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb10c-129">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-130">Valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données.</span><span class="sxs-lookup"><span data-stu-id="eb10c-130">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="eb10c-131">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="eb10c-131">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="eb10c-132">Elle ne peut avoir la valeur **true** que si le paramètre *strObjectPath* spécifie le chemin d’accès à l’objet d’une classe.</span><span class="sxs-lookup"><span data-stu-id="eb10c-132">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="eb10c-133">Quand la valeur est **true**, le jeu de points de terminaison retournés représente les classes associées à la classe source dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="eb10c-133">When set to **TRUE**, the set of returned endpoints represents classes that are associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-134">*strRequiredQualifier* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb10c-134">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-135">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="eb10c-135">String that contains a qualifier name.</span></span> <span data-ttu-id="eb10c-136">S’il est spécifié, ce paramètre indique que les objets Association retournés doivent inclure le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb10c-136">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-137">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb10c-137">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-138">Entier qui spécifie des indicateurs supplémentaires pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="eb10c-138">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="eb10c-139">La valeur par défaut de ce paramètre est **wbemFlagBidirectional**.</span><span class="sxs-lookup"><span data-stu-id="eb10c-139">The default for this parameter is **wbemFlagBidirectional**.</span></span> <span data-ttu-id="eb10c-140">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb10c-140">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="eb10c-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="eb10c-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="eb10c-142">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="eb10c-142">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="eb10c-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="eb10c-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="eb10c-144">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="eb10c-144">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="eb10c-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="eb10c-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="eb10c-146">Fait en sorte que Windows Management Instrumentation (WMI) retourne des données de modification de classe avec la définition de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="eb10c-146">Causes Windows Management Instrumentation (WMI) to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="eb10c-147">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="eb10c-147">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eb10c-148">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb10c-148">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-149">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="eb10c-149">Typically, this is undefined.</span></span> <span data-ttu-id="eb10c-150">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="eb10c-150">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="eb10c-151">Un fournisseur qui prend en charge ou requiert des informations de contexte doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="eb10c-151">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-152">*objWbemAsyncContext* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb10c-152">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-153">Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="eb10c-153">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="eb10c-154">Utilisez ce paramètre pour effectuer plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="eb10c-154">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="eb10c-155">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="eb10c-155">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="eb10c-156">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="eb10c-156">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="eb10c-157">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="eb10c-157">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb10c-158">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb10c-158">Return value</span></span>

<span data-ttu-id="eb10c-159">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="eb10c-159">This method does not return a value.</span></span> <span data-ttu-id="eb10c-160">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance.</span><span class="sxs-lookup"><span data-stu-id="eb10c-160">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="eb10c-161">Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="eb10c-161">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb10c-162">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="eb10c-162">Error codes</span></span>

<span data-ttu-id="eb10c-163">À la fin de la méthode **ReferencesToAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="eb10c-163">After the completion of the **ReferencesToAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="eb10c-164">Une collection retournée avec zéro élément n’est pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="eb10c-164">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="eb10c-165">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="eb10c-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-166">L’utilisateur actuel n’a pas l’autorisation d’afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="eb10c-166">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-167">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="eb10c-167">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-168">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="eb10c-168">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-169">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="eb10c-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-170">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb10c-170">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="eb10c-171">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="eb10c-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="eb10c-172">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="eb10c-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb10c-173">Notes</span><span class="sxs-lookup"><span data-stu-id="eb10c-173">Remarks</span></span>

<span data-ttu-id="eb10c-174">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="eb10c-174">This call returns immediately.</span></span> <span data-ttu-id="eb10c-175">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="eb10c-175">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="eb10c-176">Pour traiter chaque objet lorsqu’il retourne, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="eb10c-176">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="eb10c-177">Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="eb10c-177">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="eb10c-178">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="eb10c-178">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="eb10c-179">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="eb10c-179">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="eb10c-180">Pour éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="eb10c-180">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb10c-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb10c-181">Requirements</span></span>



| <span data-ttu-id="eb10c-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb10c-182">Requirement</span></span> | <span data-ttu-id="eb10c-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb10c-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb10c-184">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb10c-184">Minimum supported client</span></span><br/> | <span data-ttu-id="eb10c-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb10c-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb10c-186">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb10c-186">Minimum supported server</span></span><br/> | <span data-ttu-id="eb10c-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb10c-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb10c-188">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb10c-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb10c-189"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb10c-189"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb10c-190">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="eb10c-190">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb10c-191"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb10c-191"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb10c-192">DLL</span><span class="sxs-lookup"><span data-stu-id="eb10c-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb10c-193"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb10c-193"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb10c-194">CLSID</span><span class="sxs-lookup"><span data-stu-id="eb10c-194">CLSID</span></span><br/>                    | <span data-ttu-id="eb10c-195">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="eb10c-195">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="eb10c-196">IID</span><span class="sxs-lookup"><span data-stu-id="eb10c-196">IID</span></span><br/>                      | <span data-ttu-id="eb10c-197">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="eb10c-197">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="eb10c-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb10c-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb10c-199">**M**</span><span class="sxs-lookup"><span data-stu-id="eb10c-199">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="eb10c-200">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="eb10c-200">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="eb10c-201">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="eb10c-201">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="eb10c-202">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="eb10c-202">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

