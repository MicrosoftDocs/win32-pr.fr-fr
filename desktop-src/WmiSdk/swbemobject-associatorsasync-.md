---
description: La \_ méthode AssociatorsAsync de SWbemObject obtient les objets (classes ou instances) associés à l’objet actuel. Ces objets sont appelés points de terminaison. Cette méthode exécute la même fonction que les ASSOCIateurs de la requête WQL.
ms.assetid: c71e11cd-39a5-40d8-b279-f5ee9ff3ae04
ms.tgt_platform: multiple
title: Méthode SWbemObject.AssociatorsAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fe7a592327b6952308e44ac054fb94e21aa6d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516983"
---
# <a name="swbemobjectassociatorsasync_-method"></a><span data-ttu-id="cb949-105">SWbemObject. AssociatorsAsync, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="cb949-105">SWbemObject.AssociatorsAsync\_ method</span></span>

<span data-ttu-id="cb949-106">La **méthode \_ AssociatorsAsync** de [**SWbemObject**](swbemobject.md) obtient les objets (classes ou instances) associés à l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="cb949-106">The **AssociatorsAsync\_** method of [**SWbemObject**](swbemobject.md) obtains objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="cb949-107">Ces objets sont appelés points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="cb949-107">These objects are called endpoints.</span></span> <span data-ttu-id="cb949-108">Cette méthode exécute la même fonction que les ASSOCIateurs de la requête WQL.</span><span class="sxs-lookup"><span data-stu-id="cb949-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="cb949-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="cb949-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb949-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb949-110">Syntax</span></span>


```VB
SWbemObject.AssociatorsAsync_( _
  ByVal objWbemSink, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="cb949-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb949-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb949-112">*objWbemSink* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cb949-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="cb949-113">Required.</span></span> <span data-ttu-id="cb949-114">Récepteur d’objets qui reçoit les objets de façon asynchrone en tant que rappel.</span><span class="sxs-lookup"><span data-stu-id="cb949-114">Object sink that receives the objects asynchronously as a callback.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-115">*strAssocClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-115">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-116">Chaîne qui contient une classe d’association.</span><span class="sxs-lookup"><span data-stu-id="cb949-116">String that contains an association class.</span></span> <span data-ttu-id="cb949-117">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent être associés à la source par le biais de la classe d’association spécifiée ou d’une classe dérivée de cette classe d’association.</span><span class="sxs-lookup"><span data-stu-id="cb949-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-118">*strResultClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-118">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-119">Chaîne qui contient un nom de classe.</span><span class="sxs-lookup"><span data-stu-id="cb949-119">String that contains a class name.</span></span> <span data-ttu-id="cb949-120">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent appartenir ou être dérivés de la classe spécifiée dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="cb949-120">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-121">*strResultRole* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-121">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-122">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="cb949-122">String that contains a property name.</span></span> <span data-ttu-id="cb949-123">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent jouer un rôle particulier dans leur association avec l’objet source.</span><span class="sxs-lookup"><span data-stu-id="cb949-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="cb949-124">Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.</span><span class="sxs-lookup"><span data-stu-id="cb949-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-125">*strRole* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-125">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-126">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="cb949-126">String that contains a property name.</span></span> <span data-ttu-id="cb949-127">Si ce paramètre est spécifié, ce paramètre indique que les points de terminaison retournés doivent participer à une association avec l’objet source dans lequel l’objet source joue un rôle particulier.</span><span class="sxs-lookup"><span data-stu-id="cb949-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="cb949-128">Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.</span><span class="sxs-lookup"><span data-stu-id="cb949-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-129">*bClassesOnly* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-129">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-130">Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes.</span><span class="sxs-lookup"><span data-stu-id="cb949-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="cb949-131">Il s’agit des classes auxquelles les instances de point de terminaison appartiennent.</span><span class="sxs-lookup"><span data-stu-id="cb949-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="cb949-132">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="cb949-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-133">*bSchemaOnly* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-133">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-134">Valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données.</span><span class="sxs-lookup"><span data-stu-id="cb949-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="cb949-135">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="cb949-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="cb949-136">Elle peut uniquement avoir la valeur **true** si l’objet sur lequel cette méthode est appelée est une classe.</span><span class="sxs-lookup"><span data-stu-id="cb949-136">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="cb949-137">Quand la valeur est **true**, le jeu de points de terminaison retournés représente des classes qui sont correctement associées à la classe source dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="cb949-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-138">*strRequiredAssocQualifier* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-138">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-139">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="cb949-139">String that contains a qualifier name.</span></span> <span data-ttu-id="cb949-140">Si ce paramètre est spécifié, ce paramètre indique que les points de terminaison retournés doivent être associés à l’objet source par le biais d’une classe d’association qui inclut le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="cb949-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-141">*strRequiredQualifier* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-141">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-142">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="cb949-142">String that contains a qualifier name.</span></span> <span data-ttu-id="cb949-143">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent inclure le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="cb949-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-144">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-144">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-145">Entier spécifiant des indicateurs supplémentaires pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="cb949-145">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="cb949-146">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb949-146">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="cb949-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="cb949-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="cb949-148">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**SWbemSink. OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="cb949-148">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="cb949-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="cb949-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="cb949-150">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="cb949-150">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="cb949-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="cb949-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="cb949-152">Fait en sorte que WMI retourne les descriptions des propriétés et des classes localisées.</span><span class="sxs-lookup"><span data-stu-id="cb949-152">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="cb949-153">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="cb949-153">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cb949-154">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-154">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-155">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb949-155">Typically, this is undefined.</span></span> <span data-ttu-id="cb949-156">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="cb949-156">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="cb949-157">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="cb949-157">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-158">*objWbemAsyncContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cb949-158">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb949-159">Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="cb949-159">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="cb949-160">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="cb949-160">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="cb949-161">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="cb949-161">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="cb949-162">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="cb949-162">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="cb949-163">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cb949-163">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb949-164">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb949-164">Return value</span></span>

<span data-ttu-id="cb949-165">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cb949-165">This method does not return a value.</span></span> <span data-ttu-id="cb949-166">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance.</span><span class="sxs-lookup"><span data-stu-id="cb949-166">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="cb949-167">Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="cb949-167">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb949-168">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="cb949-168">Error codes</span></span>

<span data-ttu-id="cb949-169">À la fin de la méthode **AssociatorsAsync \_** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="cb949-169">After completion of the **AssociatorsAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="cb949-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="cb949-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="cb949-171">L’utilisateur actuel n’est pas autorisé à afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="cb949-171">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-172">**wbemErrFailed** -2147449889 (0x7FFF7C21)</span><span class="sxs-lookup"><span data-stu-id="cb949-172">**wbemErrFailed** - 2147449889 (0x7FFF7C21)</span></span>
</dt> <dd>

<span data-ttu-id="cb949-173">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cb949-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-174">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="cb949-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="cb949-175">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="cb949-175">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="cb949-176">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="cb949-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="cb949-177">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="cb949-177">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb949-178">Notes</span><span class="sxs-lookup"><span data-stu-id="cb949-178">Remarks</span></span>

<span data-ttu-id="cb949-179">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="cb949-179">This call returns immediately.</span></span> <span data-ttu-id="cb949-180">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="cb949-180">The requested objects and status are returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="cb949-181">Pour traiter chaque objet lorsqu’il arrive, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="cb949-181">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="cb949-182">Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="cb949-182">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="cb949-183">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="cb949-183">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="cb949-184">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="cb949-184">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="cb949-185">Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone.</span><span class="sxs-lookup"><span data-stu-id="cb949-185">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="cb949-186">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="cb949-186">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="cb949-187">Pour plus d’informations sur les ASSOCIateurs de requêtes WQL, d’instances source et de points de terminaison associés, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="cb949-187">For more information about the ASSOCIATORS OF associated WQL queries, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb949-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb949-188">Requirements</span></span>



| <span data-ttu-id="cb949-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb949-189">Requirement</span></span> | <span data-ttu-id="cb949-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb949-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb949-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb949-191">Minimum supported client</span></span><br/> | <span data-ttu-id="cb949-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb949-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb949-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb949-193">Minimum supported server</span></span><br/> | <span data-ttu-id="cb949-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb949-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb949-195">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb949-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb949-196"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb949-196"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb949-197">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cb949-197">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb949-198"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cb949-198"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cb949-199">DLL</span><span class="sxs-lookup"><span data-stu-id="cb949-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb949-200"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb949-200"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cb949-201">CLSID</span><span class="sxs-lookup"><span data-stu-id="cb949-201">CLSID</span></span><br/>                    | <span data-ttu-id="cb949-202">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="cb949-202">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="cb949-203">IID</span><span class="sxs-lookup"><span data-stu-id="cb949-203">IID</span></span><br/>                      | <span data-ttu-id="cb949-204">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="cb949-204">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="cb949-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb949-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb949-206">**M**</span><span class="sxs-lookup"><span data-stu-id="cb949-206">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="cb949-207">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="cb949-207">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="cb949-208">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="cb949-208">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="cb949-209">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="cb949-209">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

