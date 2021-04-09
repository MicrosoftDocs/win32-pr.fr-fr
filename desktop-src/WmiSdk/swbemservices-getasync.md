---
description: Récupère un objet, qui est une définition de classe ou une instance, en fonction du chemin d’accès de l’objet.
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: SWbemServices. GetAsync, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 451f13bde9458e7d57ec393f42b92a4092c99924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863761"
---
# <a name="swbemservicesgetasync-method"></a><span data-ttu-id="35d7e-103">SWbemServices. GetAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="35d7e-103">SWbemServices.GetAsync method</span></span>

<span data-ttu-id="35d7e-104">La méthode **GetAsync** de l’objet [**SWbemServices**](swbemservices.md) récupère un objet, qui est une définition de classe ou une instance, en fonction du chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35d7e-104">The **GetAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is a class definition or an instance, based on the object path.</span></span>

<span data-ttu-id="35d7e-105">Cette méthode récupère uniquement les objets de l’espace de noms associé à l’objet [**SWbemServices**](swbemservices.md) actif.</span><span class="sxs-lookup"><span data-stu-id="35d7e-105">This method retrieves only objects from the namespace that is associated with the current [**SWbemServices**](swbemservices.md) object.</span></span>

<span data-ttu-id="35d7e-106">Cette méthode est appelée en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="35d7e-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="35d7e-107">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="35d7e-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="35d7e-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="35d7e-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="35d7e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35d7e-109">Syntax</span></span>


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="35d7e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35d7e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35d7e-111">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="35d7e-111">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="35d7e-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="35d7e-112">Required.</span></span> <span data-ttu-id="35d7e-113">Récepteur d’objets qui obtient des objets de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="35d7e-113">Object sink that gets objects asynchronously.</span></span> <span data-ttu-id="35d7e-114">Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.</span><span class="sxs-lookup"><span data-stu-id="35d7e-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="35d7e-115">*strObjectPath* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="35d7e-115">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35d7e-116">Chemin d’accès de l’objet que vous souhaitez récupérer.</span><span class="sxs-lookup"><span data-stu-id="35d7e-116">Path of the object that you want to retrieve.</span></span> <span data-ttu-id="35d7e-117">Si cette valeur est vide, l’objet vide retourné peut devenir une nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="35d7e-117">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="35d7e-118">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="35d7e-118">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="35d7e-119">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="35d7e-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35d7e-120">Entier qui détermine le comportement de l’appel.</span><span class="sxs-lookup"><span data-stu-id="35d7e-120">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="35d7e-121">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="35d7e-121">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="35d7e-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="35d7e-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="35d7e-123">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="35d7e-123">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="35d7e-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="35d7e-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="35d7e-125">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="35d7e-125">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="35d7e-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="35d7e-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="35d7e-127">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="35d7e-127">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="35d7e-128">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="35d7e-128">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="35d7e-129">*objwbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="35d7e-129">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35d7e-130">En règle générale, cette valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="35d7e-130">Typically, this value is undefined.</span></span> <span data-ttu-id="35d7e-131">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="35d7e-131">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="35d7e-132">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="35d7e-132">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="35d7e-133">*objWbemAsyncContext* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="35d7e-133">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35d7e-134">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="35d7e-134">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="35d7e-135">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="35d7e-135">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="35d7e-136">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="35d7e-136">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="35d7e-137">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="35d7e-137">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="35d7e-138">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="35d7e-138">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35d7e-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35d7e-139">Return value</span></span>

<span data-ttu-id="35d7e-140">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="35d7e-140">This method does not return a value.</span></span> <span data-ttu-id="35d7e-141">En cas de réussite, le récepteur reçoit un événement [**OnObjectReady**](swbemsink-onobjectready.md) lorsque l’objet est disponible.</span><span class="sxs-lookup"><span data-stu-id="35d7e-141">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event when the object is available.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35d7e-142">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="35d7e-142">Error codes</span></span>

<span data-ttu-id="35d7e-143">À la fin de la méthode **GetAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="35d7e-143">After the completion of the **GetAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="35d7e-144">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="35d7e-144">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="35d7e-145">L’utilisateur actuel n’a pas l’autorisation d’accéder à l’objet.</span><span class="sxs-lookup"><span data-stu-id="35d7e-145">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="35d7e-146">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="35d7e-146">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="35d7e-147">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="35d7e-147">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="35d7e-148">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="35d7e-148">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="35d7e-149">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="35d7e-149">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="35d7e-150">**wbemErrInvalidObjectPath** -2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="35d7e-150">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="35d7e-151">Le chemin d’accès spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="35d7e-151">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="35d7e-152">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="35d7e-152">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="35d7e-153">L’objet demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="35d7e-153">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="35d7e-154">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="35d7e-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="35d7e-155">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="35d7e-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35d7e-156">Notes</span><span class="sxs-lookup"><span data-stu-id="35d7e-156">Remarks</span></span>

<span data-ttu-id="35d7e-157">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="35d7e-157">This call returns immediately.</span></span> <span data-ttu-id="35d7e-158">L’objet et l’État demandés sont retournés à l’appelant via un rappel remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="35d7e-158">The requested object and status are returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="35d7e-159">Pour traiter l’objet lorsqu’il retourne, créez un *objWbemSink*. [**OnObjectReady**](swbemsink-onobjectready.md), ou *objWbemSink*. Sous-routine d’événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="35d7e-159">To process the object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md), or an *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event subroutine.</span></span>

<span data-ttu-id="35d7e-160">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="35d7e-160">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="35d7e-161">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="35d7e-161">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="35d7e-162">Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone.</span><span class="sxs-lookup"><span data-stu-id="35d7e-162">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="35d7e-163">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="35d7e-163">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35d7e-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35d7e-164">Requirements</span></span>



| <span data-ttu-id="35d7e-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35d7e-165">Requirement</span></span> | <span data-ttu-id="35d7e-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="35d7e-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35d7e-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35d7e-167">Minimum supported client</span></span><br/> | <span data-ttu-id="35d7e-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35d7e-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35d7e-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35d7e-169">Minimum supported server</span></span><br/> | <span data-ttu-id="35d7e-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35d7e-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35d7e-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="35d7e-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="35d7e-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="35d7e-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="35d7e-173">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="35d7e-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="35d7e-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35d7e-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35d7e-175">DLL</span><span class="sxs-lookup"><span data-stu-id="35d7e-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35d7e-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35d7e-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="35d7e-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="35d7e-177">CLSID</span></span><br/>                    | <span data-ttu-id="35d7e-178">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="35d7e-178">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="35d7e-179">IID</span><span class="sxs-lookup"><span data-stu-id="35d7e-179">IID</span></span><br/>                      | <span data-ttu-id="35d7e-180">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="35d7e-180">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="35d7e-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35d7e-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d7e-182">**M**</span><span class="sxs-lookup"><span data-stu-id="35d7e-182">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="35d7e-183">**M**</span><span class="sxs-lookup"><span data-stu-id="35d7e-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

