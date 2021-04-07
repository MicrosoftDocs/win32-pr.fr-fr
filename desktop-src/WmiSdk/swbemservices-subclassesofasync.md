---
description: Retourne une collection de sous-classes pour une classe spécifiée.
ms.assetid: a9d16ee9-992e-4ce5-9c03-0a2c9958588c
ms.tgt_platform: multiple
title: SWbemServices. SubclassesOfAsync, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8d325c96ea1a292d8ac3afc76bfea619fe5a143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952345"
---
# <a name="swbemservicessubclassesofasync-method"></a><span data-ttu-id="b5201-103">SWbemServices. SubclassesOfAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="b5201-103">SWbemServices.SubclassesOfAsync method</span></span>

<span data-ttu-id="b5201-104">La méthode **SubclassesOfAsync** de l’objet [**SWbemServices**](swbemservices.md) retourne une collection de sous-classes pour une classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b5201-104">The **SubclassesOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of subclasses for a specified class.</span></span> <span data-ttu-id="b5201-105">Utilisez cette méthode uniquement pour les objets de classe.</span><span class="sxs-lookup"><span data-stu-id="b5201-105">Only use this method for class objects.</span></span>

<span data-ttu-id="b5201-106">Cette méthode est appelée en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b5201-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="b5201-107">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b5201-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b5201-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b5201-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5201-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5201-109">Syntax</span></span>


```VB
SWbemServices.SubclassesOfAsync( _
  ByVal ObjWbemSink, _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b5201-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5201-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5201-111">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="b5201-111">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="b5201-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b5201-112">Required.</span></span> <span data-ttu-id="b5201-113">Récepteur d’objets qui reçoit les sous-classes de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b5201-113">Object sink that receives the subclasses asynchronously.</span></span> <span data-ttu-id="b5201-114">Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.</span><span class="sxs-lookup"><span data-stu-id="b5201-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="b5201-115">*strSuperclass* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b5201-115">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5201-116">Spécifie un nom de classe parente.</span><span class="sxs-lookup"><span data-stu-id="b5201-116">Specifies a parent class name.</span></span> <span data-ttu-id="b5201-117">Seules les classes qui sont des sous-classes de cette classe sont retournées dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="b5201-117">Only the classes that are subclasses of this class are returned in the enumerator.</span></span> <span data-ttu-id="b5201-118">Si ce paramètre est vide et si *IFlags* est **wbemQueryFlagShallow**, seules les classes de niveau supérieur sont retournées (c’est-à-dire les classes qui n’ont pas de classe parente).</span><span class="sxs-lookup"><span data-stu-id="b5201-118">If this parameter is blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="b5201-119">Si ce paramètre est vide et si *IFlags* est **wbemQueryFlagDeep**, toutes les classes de l’espace de noms sont retournées.</span><span class="sxs-lookup"><span data-stu-id="b5201-119">If this parameter is blank, and if *iFlags* is **wbemQueryFlagDeep**, all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="b5201-120">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b5201-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5201-121">Détermine la profondeur de l’énumération des appels.</span><span class="sxs-lookup"><span data-stu-id="b5201-121">Determines the depth of the call enumeration.</span></span> <span data-ttu-id="b5201-122">La valeur par défaut de ce paramètre est **wbemQueryFlagDeep**.</span><span class="sxs-lookup"><span data-stu-id="b5201-122">The default value for this parameter is **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="b5201-123">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b5201-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="b5201-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="b5201-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="b5201-125">Force l’énumération à inclure uniquement les sous-classes immédiates de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b5201-125">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="b5201-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b5201-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b5201-127">Valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="b5201-127">Default for this parameter.</span></span> <span data-ttu-id="b5201-128">Cette valeur force l’énumération récursive dans toutes les sous-classes dérivées de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b5201-128">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="b5201-129">La classe parente n’est pas retournée dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="b5201-129">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="b5201-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="b5201-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="b5201-131">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="b5201-131">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="b5201-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b5201-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b5201-133">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="b5201-133">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b5201-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b5201-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b5201-135">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="b5201-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="b5201-136">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b5201-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b5201-137">*objwbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b5201-137">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5201-138">En général, ce paramètre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="b5201-138">Typically, this parameter is undefined.</span></span> <span data-ttu-id="b5201-139">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="b5201-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b5201-140">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="b5201-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="b5201-141">*objWbemAsyncContext* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b5201-141">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5201-142">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="b5201-142">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="b5201-143">Utilisez ce paramètre pour effectuer plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="b5201-143">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="b5201-144">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="b5201-144">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="b5201-145">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b5201-145">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="b5201-146">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b5201-146">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5201-147">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5201-147">Return value</span></span>

<span data-ttu-id="b5201-148">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b5201-148">This method does not return a value.</span></span> <span data-ttu-id="b5201-149">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) par instance.</span><span class="sxs-lookup"><span data-stu-id="b5201-149">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="b5201-150">Après la dernière instance, le récepteur d’objets reçoit un événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b5201-150">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b5201-151">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b5201-151">Error codes</span></span>

<span data-ttu-id="b5201-152">À la fin de la méthode **SubclassesOfAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="b5201-152">After the completion of the **SubclassesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="b5201-153">Une collection retournée avec zéro élément n’est pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="b5201-153">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="b5201-154">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b5201-154">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b5201-155">L’utilisateur actuel n’a pas l’autorisation d’afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="b5201-155">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="b5201-156">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b5201-156">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b5201-157">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b5201-157">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b5201-158">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="b5201-158">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="b5201-159">La classe spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="b5201-159">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b5201-160">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b5201-160">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b5201-161">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="b5201-161">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="b5201-162">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b5201-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b5201-163">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="b5201-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5201-164">Notes</span><span class="sxs-lookup"><span data-stu-id="b5201-164">Remarks</span></span>

<span data-ttu-id="b5201-165">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b5201-165">This call returns immediately.</span></span> <span data-ttu-id="b5201-166">Les objets et l’État demandés sont retournés à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="b5201-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b5201-167">Pour traiter chaque objet lorsqu’il arrive, créez un *objWbemSink*. Sous-routine d’événement [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="b5201-167">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="b5201-168">Une fois que tous les objets sont retournés, vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b5201-168">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="b5201-169">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="b5201-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b5201-170">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="b5201-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b5201-171">Pour éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="b5201-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5201-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5201-172">Requirements</span></span>



| <span data-ttu-id="b5201-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5201-173">Requirement</span></span> | <span data-ttu-id="b5201-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5201-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5201-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5201-175">Minimum supported client</span></span><br/> | <span data-ttu-id="b5201-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5201-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5201-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5201-177">Minimum supported server</span></span><br/> | <span data-ttu-id="b5201-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5201-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5201-179">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5201-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5201-180"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5201-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5201-181">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b5201-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5201-182"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5201-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5201-183">DLL</span><span class="sxs-lookup"><span data-stu-id="b5201-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5201-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5201-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b5201-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="b5201-185">CLSID</span></span><br/>                    | <span data-ttu-id="b5201-186">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="b5201-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="b5201-187">IID</span><span class="sxs-lookup"><span data-stu-id="b5201-187">IID</span></span><br/>                      | <span data-ttu-id="b5201-188">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="b5201-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b5201-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5201-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5201-190">**M**</span><span class="sxs-lookup"><span data-stu-id="b5201-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="b5201-191">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="b5201-191">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

