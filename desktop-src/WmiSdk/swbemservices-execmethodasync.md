---
description: SWbemServices.Exeméthode cMethodAsync-exécute une méthode exportée par un fournisseur de méthode.
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Exeméthode cMethodAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105587"
---
# <a name="swbemservicesexecmethodasync-method"></a><span data-ttu-id="6f3d2-103">SWbemServices.Exeméthode cMethodAsync</span><span class="sxs-lookup"><span data-stu-id="6f3d2-103">SWbemServices.ExecMethodAsync method</span></span>

<span data-ttu-id="6f3d2-104">La méthode **ExecMethodAsync** de l’objet [**SWbemServices**](swbemservices.md) exécute une méthode qui est exportée par un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-104">The **ExecMethodAsync** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="6f3d2-105">L’appel retourne immédiatement au client tandis que les paramètres entrants sont transmis au fournisseur approprié dans lequel la méthode s’exécute.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-105">The call immediately returns to the client while the inbound parameters are forwarded to the appropriate provider where the method executes.</span></span> <span data-ttu-id="6f3d2-106">Les informations et l’État sont retournés à l’appelant via des événements remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-106">Information and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="6f3d2-107">Le fournisseur, plutôt que Windows Management Instrumentation (WMI), implémente la méthode.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-107">The provider, rather than Windows Management Instrumentation (WMI), implements the method.</span></span>

<span data-ttu-id="6f3d2-108">La méthode est appelée en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="6f3d2-109">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="6f3d2-110">Pour plus d’informations et pour obtenir une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-110">For more information and an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f3d2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f3d2-111">Syntax</span></span>


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6f3d2-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f3d2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f3d2-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="6f3d2-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="6f3d2-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-114">Required.</span></span> <span data-ttu-id="6f3d2-115">Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-115">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span> <span data-ttu-id="6f3d2-116">Récepteur d’objets qui reçoit le résultat de l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-116">Object sink that receives the result of the method call.</span></span> <span data-ttu-id="6f3d2-117">Les paramètres sortants sont envoyés à l’événement [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) du récepteur d’objets fourni.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-117">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="6f3d2-118">Les résultats du mécanisme d’appel sont envoyés à l’événement [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) du récepteur d’objets fourni.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-118">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="6f3d2-119">N’oubliez pas que **SWbemSink. OnCompleted** ne reçoit pas le code de retour de la méthode WMI.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-119">Be aware that **SWbemSink.OnCompleted** does not receive the return code of the WMI method.</span></span> <span data-ttu-id="6f3d2-120">Toutefois, elle reçoit le code de retour du mécanisme réel de retour d’appel et est utile uniquement pour vérifier que l’appel s’est produit ou qu’il a échoué pour des raisons mécaniques.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-120">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span> <span data-ttu-id="6f3d2-121">Le code de résultat retourné par la méthode WMI est retourné dans l’objet de paramètre sortant fourni à **SWbemSink. OnObjectReady**.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-121">The result code that is returned from the WMI method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="6f3d2-122">Si un code d’erreur est retourné, l’objet [**IWbemObjectSink**](iwbemobjectsink.md) fourni n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-122">If any error code is returned, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="6f3d2-123">Si l’appel réussit, l’implémentation **IWbemObjectSink** de l’utilisateur est appelée pour indiquer le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-123">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6f3d2-124">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="6f3d2-124">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="6f3d2-125">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-125">Required.</span></span> <span data-ttu-id="6f3d2-126">Chaîne qui contient le chemin d’accès de l’objet pour lequel la méthode est exécutée.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-126">A string that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="6f3d2-127">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-127">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f3d2-128">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="6f3d2-128">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="6f3d2-129">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-129">Required.</span></span> <span data-ttu-id="6f3d2-130">Nom de la méthode à exécuter.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-130">The name of the method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="6f3d2-131">*objWbemInParams* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6f3d2-131">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f3d2-132">Objet [**SWbemObject**](swbemobject.md) qui contient les paramètres d’entrée de la méthode exécutée.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-132">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method that is executed.</span></span> <span data-ttu-id="6f3d2-133">Par défaut, ce paramètre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-133">By default, this parameter is undefined.</span></span> <span data-ttu-id="6f3d2-134">Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-134">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f3d2-135">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6f3d2-135">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f3d2-136">Entier qui détermine le comportement de l’appel.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-136">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="6f3d2-137">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="6f3d2-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="6f3d2-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="6f3d2-139">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-139">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="6f3d2-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6f3d2-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6f3d2-141">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-141">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6f3d2-142">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6f3d2-142">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f3d2-143">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-143">Typically, this is undefined.</span></span> <span data-ttu-id="6f3d2-144">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-144">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="6f3d2-145">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="6f3d2-146">*objWbemAsyncContext* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6f3d2-146">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f3d2-147">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-147">A [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="6f3d2-148">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="6f3d2-149">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-149">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="6f3d2-150">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="6f3d2-150">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="6f3d2-151">Pour plus d’informations, consultez [création d’un appel asynchrone avec VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-151">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f3d2-152">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6f3d2-152">Return value</span></span>

<span data-ttu-id="6f3d2-153">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-153">This method does not return a value.</span></span> <span data-ttu-id="6f3d2-154">Si l’appel réussit, un objet de [**paramètres de paramètre**](swbemmethod-outparameters.md) , qui est également un [**SWbemObject**](swbemobject.md) est fourni au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-154">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) is supplied to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="6f3d2-155">L’objet de **paramètres** de sortie retournés contient les paramètres de sortie et la valeur de retour pour la méthode en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-155">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span> <span data-ttu-id="6f3d2-156">Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-156">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="6f3d2-157">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6f3d2-157">Error codes</span></span>

<span data-ttu-id="6f3d2-158">Une fois la méthode **ExecMethodAsync** terminée, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-158">After the completion of the **ExecMethodAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes listed in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6f3d2-159">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6f3d2-159">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6f3d2-160">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-160">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="6f3d2-161">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="6f3d2-161">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="6f3d2-162">La classe spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-162">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6f3d2-163">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="6f3d2-163">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6f3d2-164">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-164">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6f3d2-165">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6f3d2-165">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6f3d2-166">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-166">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6f3d2-167">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="6f3d2-167">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="6f3d2-168">La méthode demandée n’était pas disponible.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-168">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="6f3d2-169">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="6f3d2-169">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="6f3d2-170">L’utilisateur actuel n’a pas été autorisé à exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-170">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f3d2-171">Notes </span><span class="sxs-lookup"><span data-stu-id="6f3d2-171">Remarks</span></span>

<span data-ttu-id="6f3d2-172">Si la méthode exécutée a des paramètres d’entrée, [**l’objet**](swbemmethod-inparameters.md) InParameters dans le paramètre *objWbemInParam* doit être le même que la description dans les rubriques construire des objets inserts [et analyse des objets de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="6f3d2-172">If the method executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object in the *objWbemInParam* parameter must be the same as the description in the [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md) topics.</span></span>

<span data-ttu-id="6f3d2-173">Utilisez **SWbemServices.ExecMethodAsync** comme alternative à l’accès direct pour l’exécution d’une [*méthode de fournisseur*](gloss-p.md) lorsqu’il n’est pas possible d’exécuter une méthode directement.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-173">Use **SWbemServices.ExecMethodAsync** as an alternative to direct access for executing a [*provider method*](gloss-p.md) when it is not possible to execute a method directly.</span></span> <span data-ttu-id="6f3d2-174">Par exemple, utilisez-le avec un langage de script qui ne prend pas en charge les paramètres de sortie, autrement dit, si votre méthode a des paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-174">For example, use it with a scripting language that does not support output parameters, that is, if your method has OUT parameters.</span></span> <span data-ttu-id="6f3d2-175">Dans le cas contraire, il est recommandé d’utiliser l’accès direct pour appeler une méthode.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-175">Otherwise, it is recommended that you use direct access to invoke a method.</span></span> <span data-ttu-id="6f3d2-176">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-176">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="6f3d2-177">La méthode **SWbemServices.ExecMethodAsync** requiert un chemin d’accès à un objet.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-177">The **SWbemServices.ExecMethodAsync** method requires an object path.</span></span> <span data-ttu-id="6f3d2-178">Si le script contient déjà un objet [**SWbemObject**](swbemobject.md) , vous pouvez appeler [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-178">If the script already contains an [**SWbemObject**](swbemobject.md) object, you can call [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>

<span data-ttu-id="6f3d2-179">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-179">This call returns immediately.</span></span> <span data-ttu-id="6f3d2-180">Les informations d’État sont retournées à l’appelant via les rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-180">The status information is returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="6f3d2-181">Pour poursuivre le traitement lorsque l’appel est terminé, implémentez une sous-routine pour *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="6f3d2-181">To continue processing when the call is completed, implement a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="6f3d2-182">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-182">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="6f3d2-183">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-183">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="6f3d2-184">Pour plus d’informations sur la façon d’éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-184">For more information about how to eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="6f3d2-185">Utilisez le paramètre *objWbemAsyncContext* pour vérifier la source d’un appel.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-185">Use the *objWbemAsyncContext* parameter to verify the source of a call.</span></span>

## <a name="examples"></a><span data-ttu-id="6f3d2-186">Exemples</span><span class="sxs-lookup"><span data-stu-id="6f3d2-186">Examples</span></span>

<span data-ttu-id="6f3d2-187">L’exemple de code suivant montre la méthode **ExecMethodAsync** .</span><span class="sxs-lookup"><span data-stu-id="6f3d2-187">The following code example shows the **ExecMethodAsync** method.</span></span> <span data-ttu-id="6f3d2-188">Le script crée un [**objet \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) qui représente un processus qui exécute le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="6f3d2-188">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="6f3d2-189">Il illustre la configuration d’un objet [**Parameters**](swbemmethod-inparameters.md) et l’obtention des résultats d’un objet de [**paramètres de paramètres**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="6f3d2-189">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="6f3d2-190">Pour obtenir un script qui montre les mêmes opérations exécutées de façon synchrone, consultez [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-190">For a script that shows the same operations performed synchronously, see [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="6f3d2-191">Pour obtenir un exemple d’utilisation de l’accès direct, consultez [créer une méthode dans la classe \_ processus Win32](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-191">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="6f3d2-192">Pour obtenir un exemple de la même opération à l’aide de [**SWbemObject**](swbemobject.md), consultez [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="6f3d2-192">For an example of the same operation using [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="6f3d2-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f3d2-193">Requirements</span></span>



| <span data-ttu-id="6f3d2-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f3d2-194">Requirement</span></span> | <span data-ttu-id="6f3d2-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f3d2-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f3d2-196">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f3d2-196">Minimum supported client</span></span><br/> | <span data-ttu-id="6f3d2-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f3d2-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f3d2-198">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f3d2-198">Minimum supported server</span></span><br/> | <span data-ttu-id="6f3d2-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f3d2-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f3d2-200">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f3d2-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f3d2-201"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f3d2-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f3d2-202">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6f3d2-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f3d2-203"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f3d2-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f3d2-204">DLL</span><span class="sxs-lookup"><span data-stu-id="6f3d2-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f3d2-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f3d2-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f3d2-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="6f3d2-206">CLSID</span></span><br/>                    | <span data-ttu-id="6f3d2-207">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="6f3d2-207">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="6f3d2-208">IID</span><span class="sxs-lookup"><span data-stu-id="6f3d2-208">IID</span></span><br/>                      | <span data-ttu-id="6f3d2-209">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="6f3d2-209">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="6f3d2-210">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f3d2-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f3d2-211">**M**</span><span class="sxs-lookup"><span data-stu-id="6f3d2-211">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="6f3d2-212">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="6f3d2-212">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="6f3d2-213">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="6f3d2-213">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="6f3d2-214">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="6f3d2-214">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="6f3d2-215">Appel d’une méthode de fournisseur</span><span class="sxs-lookup"><span data-stu-id="6f3d2-215">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="6f3d2-216">Manipulation des informations relatives aux classes et aux instances</span><span class="sxs-lookup"><span data-stu-id="6f3d2-216">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

