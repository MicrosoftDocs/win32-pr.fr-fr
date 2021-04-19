---
description: Retourne une collection d’objets (classes ou instances) appelées points de terminaison associés à un objet spécifié.
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: SWbemServices. AssociatorsOfAsync, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d83f2eb33b7cd2d6ce6345d9b40a2367539dfec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516980"
---
# <a name="swbemservicesassociatorsofasync-method"></a><span data-ttu-id="34065-103">SWbemServices. AssociatorsOfAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="34065-103">SWbemServices.AssociatorsOfAsync method</span></span>

<span data-ttu-id="34065-104">La méthode **AssociatorsOfAsync** de l’objet [**SWbemServices**](swbemservices.md) retourne une collection d’objets (classes ou instances) appelées points de terminaison associés à un objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="34065-104">The **AssociatorsOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="34065-105">L’appel à **AssociatorsOfAsync** retourne immédiatement, et les résultats et l’État sont retournés à l’appelant via des événements remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="34065-105">The call to **AssociatorsOfAsync** returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="34065-106">Pour gérer chaque objet retourné, créez un *objWbemSink*. Gestionnaire d’événements [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="34065-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event handler.</span></span>

<span data-ttu-id="34065-107">Une fois que tous les objets arrivent, le traitement s’effectue dans le *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="34065-107">After all the objects arrive, processing is done in the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span> <span data-ttu-id="34065-108">Cette méthode exécute la même fonction que les ASSOCIateurs de la requête WQL.</span><span class="sxs-lookup"><span data-stu-id="34065-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span> <span data-ttu-id="34065-109">Pour plus d’informations sur la création d’un récepteur, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="34065-109">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="34065-110">La méthode est appelée en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="34065-110">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="34065-111">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="34065-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="34065-112">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="34065-112">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="34065-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34065-113">Syntax</span></span>


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="34065-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34065-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34065-115">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="34065-115">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="34065-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="34065-116">Required.</span></span> <span data-ttu-id="34065-117">Récepteur d’objets qui reçoit les objets de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="34065-117">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="34065-118">Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.</span><span class="sxs-lookup"><span data-stu-id="34065-118">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="34065-119">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="34065-119">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="34065-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="34065-120">Required.</span></span> <span data-ttu-id="34065-121">Chaîne qui contient le chemin d’accès de l’objet de la classe ou de l’instance source.</span><span class="sxs-lookup"><span data-stu-id="34065-121">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="34065-122">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="34065-122">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="34065-123">*strAssocClass* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-123">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-124">Chaîne qui contient une classe d’association.</span><span class="sxs-lookup"><span data-stu-id="34065-124">String that contains an association class.</span></span> <span data-ttu-id="34065-125">Quand ce paramètre est spécifié, ce paramètre indique que les points de terminaison retournés doivent être associés à la source par le biais de la classe d’association spécifiée ou d’une classe dérivée de cette classe d’association.</span><span class="sxs-lookup"><span data-stu-id="34065-125">When specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="34065-126">*strResultClass* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-126">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-127">Chaîne qui contient un nom de classe.</span><span class="sxs-lookup"><span data-stu-id="34065-127">String that contains a class name.</span></span> <span data-ttu-id="34065-128">S’il est spécifié, ce paramètre facultatif indique que les points de terminaison retournés doivent appartenir ou être dérivés de la classe spécifiée dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="34065-128">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="34065-129">*strResultRole* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-129">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-130">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="34065-130">String that contains a property name.</span></span> <span data-ttu-id="34065-131">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent jouer un rôle particulier dans leur association avec l’objet source.</span><span class="sxs-lookup"><span data-stu-id="34065-131">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="34065-132">Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.</span><span class="sxs-lookup"><span data-stu-id="34065-132">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="34065-133">*strRole* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-133">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-134">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="34065-134">String that contains a property name.</span></span> <span data-ttu-id="34065-135">Si ce paramètre est spécifié, ce paramètre indique que les points de terminaison retournés doivent participer à une association avec l’objet source dans lequel l’objet source joue un rôle particulier.</span><span class="sxs-lookup"><span data-stu-id="34065-135">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="34065-136">Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.</span><span class="sxs-lookup"><span data-stu-id="34065-136">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="34065-137">*bClassesOnly* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-137">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-138">Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes.</span><span class="sxs-lookup"><span data-stu-id="34065-138">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="34065-139">Il s’agit des classes auxquelles les instances de point de terminaison appartiennent.</span><span class="sxs-lookup"><span data-stu-id="34065-139">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="34065-140">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="34065-140">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="34065-141">*bSchemaOnly* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-141">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-142">Valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données.</span><span class="sxs-lookup"><span data-stu-id="34065-142">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="34065-143">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="34065-143">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="34065-144">Elle ne peut avoir la valeur **true** que si le paramètre *strObjectPath* spécifie le chemin d’accès à l’objet d’une classe.</span><span class="sxs-lookup"><span data-stu-id="34065-144">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="34065-145">Quand la valeur est **true**, le jeu de points de terminaison retournés représente des classes qui sont associées correctement à la classe source dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="34065-145">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="34065-146">*strRequiredAssocQualifier* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-146">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-147">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="34065-147">String that contains a qualifier name.</span></span> <span data-ttu-id="34065-148">Si ce paramètre est spécifié, ce paramètre indique que les points de terminaison retournés doivent être associés à l’objet source par le biais d’une classe d’association qui inclut le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="34065-148">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="34065-149">*strRequiredQualifier* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-149">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-150">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="34065-150">String that contains a qualifier name.</span></span> <span data-ttu-id="34065-151">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent inclure le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="34065-151">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="34065-152">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-152">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-153">Entier qui spécifie les indicateurs supplémentaires pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="34065-153">Integer that specifies the additional flags to the operation.</span></span> <span data-ttu-id="34065-154">La valeur par défaut de ce paramètre est **wbemFlagDontSendStatus**.</span><span class="sxs-lookup"><span data-stu-id="34065-154">The default for this parameter is **wbemFlagDontSendStatus**.</span></span> <span data-ttu-id="34065-155">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="34065-155">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="34065-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="34065-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="34065-157">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="34065-157">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="34065-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="34065-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="34065-159">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="34065-159">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="34065-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="34065-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="34065-161">Fait en sorte que WMI retourne des données de modification de classe avec la définition de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="34065-161">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="34065-162">Pour plus d’informations sur les qualificateurs modifiés, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="34065-162">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="34065-163">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-163">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-164">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="34065-164">Typically, this is undefined.</span></span> <span data-ttu-id="34065-165">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="34065-165">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="34065-166">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="34065-166">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="34065-167">*objWbemAsyncContext* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="34065-167">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34065-168">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="34065-168">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="34065-169">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="34065-169">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="34065-170">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="34065-170">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="34065-171">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="34065-171">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="34065-172">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="34065-172">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34065-173">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34065-173">Return value</span></span>

<span data-ttu-id="34065-174">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="34065-174">This method does not return a value.</span></span> <span data-ttu-id="34065-175">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance.</span><span class="sxs-lookup"><span data-stu-id="34065-175">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="34065-176">Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="34065-176">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="34065-177">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="34065-177">Error codes</span></span>

<span data-ttu-id="34065-178">À la fin de la méthode **AssociatorsOfAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="34065-178">After the completion of the **AssociatorsOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="34065-179">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="34065-179">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="34065-180">L’utilisateur actuel n’a pas l’autorisation d’afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="34065-180">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="34065-181">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="34065-181">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="34065-182">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="34065-182">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="34065-183">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="34065-183">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="34065-184">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="34065-184">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="34065-185">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="34065-185">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="34065-186">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="34065-186">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="34065-187">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="34065-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="34065-188">L’élément demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="34065-188">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34065-189">Notes</span><span class="sxs-lookup"><span data-stu-id="34065-189">Remarks</span></span>

<span data-ttu-id="34065-190">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="34065-190">This call returns immediately.</span></span> <span data-ttu-id="34065-191">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="34065-191">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="34065-192">Pour traiter chaque objet lorsqu’il retourne, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="34065-192">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="34065-193">Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="34065-193">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="34065-194">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="34065-194">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="34065-195">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="34065-195">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="34065-196">Pour éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="34065-196">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="34065-197">Utilisez le paramètre *objWbemAsyncContext* dans les scripts pour vérifier la source d’un appel.</span><span class="sxs-lookup"><span data-stu-id="34065-197">Use the *objWbemAsyncContext* parameter in scripts to verify the source of a call.</span></span>

## <a name="requirements"></a><span data-ttu-id="34065-198">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34065-198">Requirements</span></span>



| <span data-ttu-id="34065-199">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34065-199">Requirement</span></span> | <span data-ttu-id="34065-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="34065-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34065-201">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34065-201">Minimum supported client</span></span><br/> | <span data-ttu-id="34065-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34065-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34065-203">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34065-203">Minimum supported server</span></span><br/> | <span data-ttu-id="34065-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34065-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34065-205">En-tête</span><span class="sxs-lookup"><span data-stu-id="34065-205">Header</span></span><br/>                   | <dl> <span data-ttu-id="34065-206"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="34065-206"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="34065-207">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="34065-207">Type library</span></span><br/>             | <dl> <span data-ttu-id="34065-208"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="34065-208"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="34065-209">DLL</span><span class="sxs-lookup"><span data-stu-id="34065-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34065-210"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34065-210"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="34065-211">CLSID</span><span class="sxs-lookup"><span data-stu-id="34065-211">CLSID</span></span><br/>                    | <span data-ttu-id="34065-212">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="34065-212">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="34065-213">IID</span><span class="sxs-lookup"><span data-stu-id="34065-213">IID</span></span><br/>                      | <span data-ttu-id="34065-214">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="34065-214">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="34065-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34065-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34065-216">**M**</span><span class="sxs-lookup"><span data-stu-id="34065-216">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="34065-217">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="34065-217">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="34065-218">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="34065-218">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="34065-219">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="34065-219">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="34065-220">**SWbemObject. ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="34065-220">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)
</dt> <dt>

[<span data-ttu-id="34065-221">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="34065-221">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="34065-222">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="34065-222">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

