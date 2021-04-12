---
description: La \_ méthode ExecMethodAsync de SWbemObject exécute de manière asynchrone une méthode exportée par un fournisseur de méthode.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: SWbemObject.Exeméthode cMethodAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210417"
---
# <a name="swbemobjectexecmethodasync_-method"></a><span data-ttu-id="fa728-103">SWbemObject.Exe\_ méthode cMethodAsync</span><span class="sxs-lookup"><span data-stu-id="fa728-103">SWbemObject.ExecMethodAsync\_ method</span></span>

<span data-ttu-id="fa728-104">La **méthode \_ ExecMethodAsync** de [**SWbemObject**](swbemobject.md) exécute de manière asynchrone une méthode exportée par un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="fa728-104">The **ExecMethodAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously executes a method that a method provider exports.</span></span> <span data-ttu-id="fa728-105">Cette méthode est similaire à [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), mais fonctionne directement sur l’objet de la méthode à exécuter.</span><span class="sxs-lookup"><span data-stu-id="fa728-105">This method is similar to [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), but operates directly on the object of the method to be executed.</span></span> <span data-ttu-id="fa728-106">Windows Management Instrumentation (WMI) n’implémente pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="fa728-106">Windows Management Instrumentation (WMI) does not implement this method.</span></span> <span data-ttu-id="fa728-107">Le fournisseur implémente cette méthode.</span><span class="sxs-lookup"><span data-stu-id="fa728-107">The provider implements this method.</span></span>

<span data-ttu-id="fa728-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fa728-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa728-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa728-109">Syntax</span></span>


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="fa728-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa728-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa728-111">*objWbemSink* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa728-111">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa728-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="fa728-112">Required.</span></span> <span data-ttu-id="fa728-113">Il s’agit du récepteur d’objets qui reçoit les résultats de l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="fa728-113">This is the object sink that receives the results of the method call.</span></span> <span data-ttu-id="fa728-114">Les paramètres sortants sont envoyés à l’événement [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) du récepteur d’objets fourni.</span><span class="sxs-lookup"><span data-stu-id="fa728-114">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="fa728-115">Les résultats du mécanisme d’appel sont envoyés à l’événement [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) du récepteur d’objets fourni.</span><span class="sxs-lookup"><span data-stu-id="fa728-115">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="fa728-116">Notez que **SWbemSink. OnCompleted** ne reçoit pas le code de retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="fa728-116">Notice that **SWbemSink.OnCompleted** does not receive the return code of the method.</span></span> <span data-ttu-id="fa728-117">Toutefois, il reçoit le code de retour du mécanisme réel de retour d’appel et est utile uniquement pour vérifier que l’appel s’est produit ou qu’il a échoué pour des raisons mécaniques.</span><span class="sxs-lookup"><span data-stu-id="fa728-117">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred, or that it failed for mechanical reasons.</span></span> <span data-ttu-id="fa728-118">Le code de résultat retourné par la méthode est retourné dans l’objet de paramètre sortant fourni à **SWbemSink. OnObjectReady**.</span><span class="sxs-lookup"><span data-stu-id="fa728-118">The result code returned from the method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="fa728-119">Si un code d’erreur est retourné, l’objet [**IWbemObjectSink**](iwbemobjectsink.md) fourni n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="fa728-119">If any error code returns, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="fa728-120">Si l’appel réussit, l’implémentation **IWbemObjectSink** de l’utilisateur est appelée pour indiquer le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="fa728-120">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fa728-121">*strMethodName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa728-121">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa728-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="fa728-122">Required.</span></span> <span data-ttu-id="fa728-123">Il s’agit du nom de la méthode pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="fa728-123">This is the name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="fa728-124">*objwbemInParams* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fa728-124">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa728-125">Il s’agit d’un objet [**SWbemObject**](swbemobject.md) qui contient les paramètres d’entrée de la méthode en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fa728-125">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="fa728-126">Par défaut, ce paramètre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="fa728-126">By default, this parameter is undefined.</span></span> <span data-ttu-id="fa728-127">Pour plus d’informations, consultez [construction d’objets inparamètres](constructing-inparameters-objects.md) et [analyse d’objets de paramètres de paramètres](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fa728-127">For more information, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa728-128">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fa728-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa728-129">Entier qui détermine le comportement de l’appel.</span><span class="sxs-lookup"><span data-stu-id="fa728-129">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="fa728-130">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fa728-130">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="fa728-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="fa728-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="fa728-132">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**SWbemSink. OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="fa728-132">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="fa728-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="fa728-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="fa728-134">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="fa728-134">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fa728-135">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fa728-135">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa728-136">En règle générale, il n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="fa728-136">Typically, it is undefined.</span></span> <span data-ttu-id="fa728-137">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="fa728-137">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="fa728-138">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="fa728-138">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fa728-139">*objWbemAsyncContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fa728-139">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa728-140">Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="fa728-140">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="fa728-141">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="fa728-141">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="fa728-142">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="fa728-142">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="fa728-143">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="fa728-143">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="fa728-144">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="fa728-144">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa728-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa728-145">Return value</span></span>

<span data-ttu-id="fa728-146">Cette méthode n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="fa728-146">This method has no return values.</span></span> <span data-ttu-id="fa728-147">Si l’appel réussit, un objet de [**paramètres de paramètre**](swbemmethod-outparameters.md) , qui est également un objet [**SWbemObject**](swbemobject.md) , est fourni au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="fa728-147">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) object, is supplied to the sink specified in *objWbemSink*.</span></span> <span data-ttu-id="fa728-148">L’objet de **paramètres** de sortie retournés contient les paramètres de sortie et la valeur de retour pour la méthode en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fa728-148">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fa728-149">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fa728-149">Error codes</span></span>

<span data-ttu-id="fa728-150">Une fois la méthode **ExecMethodAsync \_** terminée, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="fa728-150">After completion of the **ExecMethodAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="fa728-151">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="fa728-151">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="fa728-152">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fa728-152">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="fa728-153">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="fa728-153">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="fa728-154">La classe spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="fa728-154">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fa728-155">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="fa728-155">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="fa728-156">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="fa728-156">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fa728-157">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="fa728-157">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="fa728-158">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="fa728-158">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fa728-159">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="fa728-159">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="fa728-160">La méthode demandée n’était pas disponible.</span><span class="sxs-lookup"><span data-stu-id="fa728-160">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="fa728-161">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="fa728-161">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="fa728-162">L’utilisateur actuel n’a pas été autorisé à exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="fa728-162">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa728-163">Notes</span><span class="sxs-lookup"><span data-stu-id="fa728-163">Remarks</span></span>

<span data-ttu-id="fa728-164">Utilisez la méthode **SWbemObject.Exe\_ cMethodAsync** comme alternative à l’accès direct pour l’exécution d’une [*méthode de fournisseur*](gloss-p.md) lorsque vous ne pouvez pas exécuter une méthode directement.</span><span class="sxs-lookup"><span data-stu-id="fa728-164">Use the **SWbemObject.ExecMethodAsync\_** method as an alternative to direct access for executing a [*provider method*](gloss-p.md) when you cannot execute a method directly.</span></span> <span data-ttu-id="fa728-165">Par exemple, si votre méthode a des paramètres out, utilisez la méthode **SWbemObject.ExecMethodAsync \_** avec un langage de script qui ne prend pas en charge les paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="fa728-165">For example, if your method has out parameters, use the **SWbemObject.ExecMethodAsync\_** method with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="fa728-166">Dans le cas contraire, il est recommandé d’appeler une méthode à l’aide d’un accès direct.</span><span class="sxs-lookup"><span data-stu-id="fa728-166">Otherwise, it is recommended that you invoke a method using direct access.</span></span> <span data-ttu-id="fa728-167">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="fa728-167">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="fa728-168">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="fa728-168">This call returns immediately.</span></span> <span data-ttu-id="fa728-169">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="fa728-169">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="fa728-170">Pour traiter chaque objet lorsqu’il arrive, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="fa728-170">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="fa728-171">Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="fa728-171">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="fa728-172">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="fa728-172">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="fa728-173">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="fa728-173">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="fa728-174">Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone.</span><span class="sxs-lookup"><span data-stu-id="fa728-174">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="fa728-175">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="fa728-175">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="fa728-176">Si la méthode en cours d’exécution a des paramètres d’entrée, l’objet [**Parameters**](swbemmethod-inparameters.md) et le paramètre *objWbemInParam* doivent être construits comme décrit dans [construction d’objets inparamètres](constructing-inparameters-objects.md) et [analyse d’objets de paramètres](parsing-outparameters-objects.md)de sortie.</span><span class="sxs-lookup"><span data-stu-id="fa728-176">If the method being executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object and *objWbemInParam* parameter must be constructed as described in [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="fa728-177">La méthode **SWbemObject.Exe\_ cMethodAsync** suppose que l’objet représenté par [**SWbemObject**](swbemobject.md) contient la méthode à exécuter.</span><span class="sxs-lookup"><span data-stu-id="fa728-177">The **SWbemObject.ExecMethodAsync\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="fa728-178">La méthode [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) requiert un chemin d’accès à un objet.</span><span class="sxs-lookup"><span data-stu-id="fa728-178">The [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) method requires an object path.</span></span>

## <a name="examples"></a><span data-ttu-id="fa728-179">Exemples</span><span class="sxs-lookup"><span data-stu-id="fa728-179">Examples</span></span>

<span data-ttu-id="fa728-180">L’exemple suivant illustre la méthode [**ExecMethodAsync**](swbemservices-execmethodasync.md) .</span><span class="sxs-lookup"><span data-stu-id="fa728-180">The following example shows the [**ExecMethodAsync**](swbemservices-execmethodasync.md) method.</span></span> <span data-ttu-id="fa728-181">Le script crée un [**objet \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) qui représente un processus qui exécute le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="fa728-181">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="fa728-182">Il illustre la configuration d’un objet [**Parameters**](swbemmethod-inparameters.md) et explique comment obtenir les résultats d’un objet de [**paramètres de paramètres**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="fa728-182">It shows setting up of [**InParameters**](swbemmethod-inparameters.md) object, and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span>

<span data-ttu-id="fa728-183">Pour obtenir un script qui montre les mêmes opérations exécutées de façon synchrone, consultez [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="fa728-183">For a script that shows the same operations performed synchronously, see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span> <span data-ttu-id="fa728-184">Pour obtenir un exemple d’utilisation de l’accès direct, consultez [**créer une méthode dans la classe \_ processus Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="fa728-184">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="fa728-185">Pour obtenir un exemple de la même opération à l’aide d’un objet [**SWbemServices**](swbemservices.md) , consultez [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="fa728-185">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span>


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="fa728-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa728-186">Requirements</span></span>



| <span data-ttu-id="fa728-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa728-187">Requirement</span></span> | <span data-ttu-id="fa728-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa728-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa728-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa728-189">Minimum supported client</span></span><br/> | <span data-ttu-id="fa728-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa728-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa728-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa728-191">Minimum supported server</span></span><br/> | <span data-ttu-id="fa728-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa728-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa728-193">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa728-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa728-194"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa728-194"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa728-195">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fa728-195">Type library</span></span><br/>             | <dl> <span data-ttu-id="fa728-196"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fa728-196"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fa728-197">DLL</span><span class="sxs-lookup"><span data-stu-id="fa728-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa728-198"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa728-198"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fa728-199">CLSID</span><span class="sxs-lookup"><span data-stu-id="fa728-199">CLSID</span></span><br/>                    | <span data-ttu-id="fa728-200">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="fa728-200">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="fa728-201">IID</span><span class="sxs-lookup"><span data-stu-id="fa728-201">IID</span></span><br/>                      | <span data-ttu-id="fa728-202">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="fa728-202">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="fa728-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa728-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa728-204">**M**</span><span class="sxs-lookup"><span data-stu-id="fa728-204">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="fa728-205">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="fa728-205">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

