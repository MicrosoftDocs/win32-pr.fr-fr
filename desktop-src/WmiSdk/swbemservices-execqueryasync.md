---
description: SWbemServices.Exeméthode cQueryAsync-exécute une requête pour récupérer des objets.
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: SWbemServices.Exeméthode cQueryAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5cd3fe778ca7338df6b2674a4930458ef9113a1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118377"
---
# <a name="swbemservicesexecqueryasync-method"></a><span data-ttu-id="b0491-103">SWbemServices.Exeméthode cQueryAsync</span><span class="sxs-lookup"><span data-stu-id="b0491-103">SWbemServices.ExecQueryAsync method</span></span>

<span data-ttu-id="b0491-104">La méthode **ExecQueryAsync** de l’objet [**SWbemServices**](swbemservices.md) exécute une requête pour récupérer des objets.</span><span class="sxs-lookup"><span data-stu-id="b0491-104">The **ExecQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="b0491-105">L’appel à cette méthode retourne immédiatement, et les résultats et l’État sont retournés à l’appelant via des événements remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="b0491-105">The call to this method returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b0491-106">Pour gérer chaque objet retourné, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="b0491-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span>

<span data-ttu-id="b0491-107">La méthode est appelée en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b0491-107">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="b0491-108">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b0491-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b0491-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b0491-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0491-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0491-110">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQueryAsync( _
  [ ByVal objWbemSink ], _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b0491-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0491-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0491-112">*objWbemSink* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b0491-112">*objWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0491-113">Récepteur d’objets qui exécute la requête de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b0491-113">Object sink that executes the query asynchronously.</span></span> <span data-ttu-id="b0491-114">Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.</span><span class="sxs-lookup"><span data-stu-id="b0491-114">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="b0491-115">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="b0491-115">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="b0491-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b0491-116">Required.</span></span> <span data-ttu-id="b0491-117">Chaîne qui contient le texte de la requête.</span><span class="sxs-lookup"><span data-stu-id="b0491-117">String that contains the text of the query.</span></span> <span data-ttu-id="b0491-118">Ce paramètre ne peut pas être vide.</span><span class="sxs-lookup"><span data-stu-id="b0491-118">This parameter cannot be blank.</span></span> <span data-ttu-id="b0491-119">Pour plus d’informations sur la création de chaînes de requête WMI, consultez [interrogation avec WQL](querying-with-wql.md) et la référence [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="b0491-119">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="b0491-120">*strQueryLanguage* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b0491-120">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0491-121">Chaîne qui contient le langage de requête à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b0491-121">String that contains the query language to be used.</span></span> <span data-ttu-id="b0491-122">S’il est spécifié, la valeur doit être « WQL ».</span><span class="sxs-lookup"><span data-stu-id="b0491-122">If specified, the value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="b0491-123">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b0491-123">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0491-124">Entier qui détermine le comportement de la requête.</span><span class="sxs-lookup"><span data-stu-id="b0491-124">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="b0491-125">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b0491-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="b0491-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="b0491-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="b0491-127">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="b0491-127">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="b0491-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b0491-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b0491-129">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="b0491-129">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="b0491-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="b0491-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="b0491-131">Utilisé pour un prototype.</span><span class="sxs-lookup"><span data-stu-id="b0491-131">Used for a prototype.</span></span> <span data-ttu-id="b0491-132">Elle empêche la requête de se produire et retourne à la place un objet qui ressemble à un objet de résultat standard.</span><span class="sxs-lookup"><span data-stu-id="b0491-132">It stops the query from happening and instead, returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b0491-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b0491-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b0491-134">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="b0491-134">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="b0491-135">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b0491-135">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b0491-136">*objwbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b0491-136">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0491-137">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="b0491-137">Typically, this is undefined.</span></span> <span data-ttu-id="b0491-138">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui sert la demande.</span><span class="sxs-lookup"><span data-stu-id="b0491-138">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="b0491-139">Un fournisseur qui prend en charge ou requiert des informations de contexte doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="b0491-139">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="b0491-140">*objWbemAsyncContext* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b0491-140">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0491-141">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="b0491-141">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="b0491-142">Utilisez ce paramètre pour effectuer plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="b0491-142">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="b0491-143">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="b0491-143">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="b0491-144">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b0491-144">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="b0491-145">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b0491-145">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0491-146">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0491-146">Return value</span></span>

<span data-ttu-id="b0491-147">Cette méthode n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b0491-147">This method has no return values.</span></span> <span data-ttu-id="b0491-148">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance.</span><span class="sxs-lookup"><span data-stu-id="b0491-148">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="b0491-149">Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b0491-149">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0491-150">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b0491-150">Error codes</span></span>

<span data-ttu-id="b0491-151">À la fin de la méthode **ExecQueryAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="b0491-151">After the completion of the **ExecQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b0491-152">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b0491-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b0491-153">L’utilisateur actuel n’a pas l’autorisation d’afficher le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="b0491-153">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="b0491-154">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b0491-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b0491-155">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b0491-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b0491-156">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b0491-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b0491-157">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="b0491-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="b0491-158">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="b0491-158">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="b0491-159">La syntaxe de la requête n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b0491-159">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b0491-160">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="b0491-160">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="b0491-161">Le langage de requête demandé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b0491-161">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b0491-162">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b0491-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b0491-163">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="b0491-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0491-164">Notes </span><span class="sxs-lookup"><span data-stu-id="b0491-164">Remarks</span></span>

<span data-ttu-id="b0491-165">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b0491-165">This call returns immediately.</span></span> <span data-ttu-id="b0491-166">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="b0491-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b0491-167">Pour traiter chaque objet lorsqu’il retourne, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="b0491-167">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="b0491-168">Une fois que tous les objets sont retournés, effectuez le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b0491-168">After all the objects are returned, perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="b0491-169">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="b0491-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b0491-170">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="b0491-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b0491-171">Pour éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="b0491-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="b0491-172">La méthode **ExecQueryAsync** retourne un jeu de résultats vide lorsqu’aucun objet ne correspond aux critères de la requête.</span><span class="sxs-lookup"><span data-stu-id="b0491-172">The **ExecQueryAsync** method returns an empty result set when there are no objects to match the criteria in the query.</span></span> <span data-ttu-id="b0491-173">Cette méthode retourne les propriétés de clé, que la propriété de [**clé**](standard-qualifiers.md) soit demandée ou non dans le paramètre *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="b0491-173">This method returns key properties whether or not the [**Key**](standard-qualifiers.md) property is requested in the *strQuery* parameter.</span></span>

<span data-ttu-id="b0491-174">Il existe des limites concernant le nombre de mots clés **and** et **or** qui peuvent être utilisés dans les requêtes WQL.</span><span class="sxs-lookup"><span data-stu-id="b0491-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="b0491-175">Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne le \_ code d’erreur de violation de quota E WBEM \_ \_ en tant que valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b0491-175">Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM\_E\_QUOTA\_VIOLATION error code as an **HRESULT** value.</span></span> <span data-ttu-id="b0491-176">La limite des mots clés WQL dépend de la complexité de la requête.</span><span class="sxs-lookup"><span data-stu-id="b0491-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0491-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0491-177">Requirements</span></span>



| <span data-ttu-id="b0491-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0491-178">Requirement</span></span> | <span data-ttu-id="b0491-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0491-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0491-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0491-180">Minimum supported client</span></span><br/> | <span data-ttu-id="b0491-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0491-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0491-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0491-182">Minimum supported server</span></span><br/> | <span data-ttu-id="b0491-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0491-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0491-184">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0491-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0491-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0491-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0491-186">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b0491-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="b0491-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b0491-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b0491-188">DLL</span><span class="sxs-lookup"><span data-stu-id="b0491-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0491-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0491-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b0491-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="b0491-190">CLSID</span></span><br/>                    | <span data-ttu-id="b0491-191">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="b0491-191">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="b0491-192">IID</span><span class="sxs-lookup"><span data-stu-id="b0491-192">IID</span></span><br/>                      | <span data-ttu-id="b0491-193">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="b0491-193">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b0491-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0491-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0491-195">**M**</span><span class="sxs-lookup"><span data-stu-id="b0491-195">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="b0491-196">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="b0491-196">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="b0491-197">**SWbemServices.**</span><span class="sxs-lookup"><span data-stu-id="b0491-197">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

