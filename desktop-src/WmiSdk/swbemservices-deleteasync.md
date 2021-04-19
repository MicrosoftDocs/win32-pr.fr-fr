---
description: Supprime la classe ou l’instance spécifiée dans le chemin d’accès de l’objet.
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.tgt_platform: multiple
title: SWbemServices. DeleteAsync, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: adc8811c11f67b9fc92628740bd15df2086948d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536996"
---
# <a name="swbemservicesdeleteasync-method"></a><span data-ttu-id="123a7-103">SWbemServices. DeleteAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="123a7-103">SWbemServices.DeleteAsync method</span></span>

<span data-ttu-id="123a7-104">La méthode **DeleteAsync** de l’objet [**SWbemServices**](swbemservices.md) supprime la classe ou l’instance spécifiée dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="123a7-104">The **DeleteAsync** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance specified in the object path.</span></span> <span data-ttu-id="123a7-105">L’appel à **DeleteAsync** retourne immédiatement et les résultats et l’État sont retournés à l’appelant via des événements remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="123a7-105">The call to **DeleteAsync** returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="123a7-106">Pour plus d’informations sur la création d’un récepteur, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="123a7-106">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span> <span data-ttu-id="123a7-107">Vous ne pouvez supprimer que les objets de l’espace de noms auquel vous êtes connecté.</span><span class="sxs-lookup"><span data-stu-id="123a7-107">You can only delete objects in the namespace to which you are connected.</span></span>

<span data-ttu-id="123a7-108">Si un fournisseur dynamique fournit la classe ou l’instance, il n’est pas toujours possible de supprimer cet objet, sauf si le fournisseur prend en charge la suppression de classe ou d’instance.</span><span class="sxs-lookup"><span data-stu-id="123a7-108">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="123a7-109">La méthode est appelée en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="123a7-109">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="123a7-110">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="123a7-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="123a7-111">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="123a7-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="123a7-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="123a7-112">Syntax</span></span>


```VB
SWbemServices.DeleteAsync( _
  [ ByVal ObjWbemSink ], _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="123a7-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="123a7-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="123a7-114">*ObjWbemSink* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="123a7-114">*ObjWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="123a7-115">Récepteur d’objets qui reçoit les résultats de la suppression.</span><span class="sxs-lookup"><span data-stu-id="123a7-115">Object sink that receives the results of the deletion.</span></span> <span data-ttu-id="123a7-116">Créez un objet [**SWbemSink**](swbemsink.md) pour recevoir les objets.</span><span class="sxs-lookup"><span data-stu-id="123a7-116">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="123a7-117">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="123a7-117">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="123a7-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="123a7-118">Required.</span></span> <span data-ttu-id="123a7-119">Chaîne qui contient le chemin d’accès à l’objet que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="123a7-119">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="123a7-120">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="123a7-120">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="123a7-121">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="123a7-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="123a7-122">Détermine si les mises à jour d’État sont retournées.</span><span class="sxs-lookup"><span data-stu-id="123a7-122">Determines if status updates are returned.</span></span> <span data-ttu-id="123a7-123">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="123a7-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="123a7-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="123a7-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="123a7-125">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="123a7-125">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="123a7-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="123a7-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="123a7-127">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="123a7-127">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="123a7-128">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="123a7-128">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="123a7-129">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="123a7-129">Typically, this is undefined.</span></span> <span data-ttu-id="123a7-130">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="123a7-130">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="123a7-131">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="123a7-131">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="123a7-132">*objWbemAsyncContext* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="123a7-132">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="123a7-133">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="123a7-133">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="123a7-134">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="123a7-134">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="123a7-135">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="123a7-135">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="123a7-136">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="123a7-136">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="123a7-137">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="123a7-137">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="123a7-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="123a7-138">Return value</span></span>

<span data-ttu-id="123a7-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="123a7-139">This method does not return a value.</span></span> <span data-ttu-id="123a7-140">Si l’appel réussit, le récepteur d’objets reçoit la notification de la suppression.</span><span class="sxs-lookup"><span data-stu-id="123a7-140">If the call is successful, the object sink receives notification of the deletion.</span></span>

## <a name="error-codes"></a><span data-ttu-id="123a7-141">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="123a7-141">Error codes</span></span>

<span data-ttu-id="123a7-142">À la fin de la méthode **DeleteAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="123a7-142">After the completion of the **DeleteAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="123a7-143">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="123a7-143">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="123a7-144">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="123a7-144">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="123a7-145">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="123a7-145">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="123a7-146">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="123a7-146">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="123a7-147">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="123a7-147">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="123a7-148">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="123a7-148">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="123a7-149">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="123a7-149">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="123a7-150">Une erreur réseau s’est produite, empêchant le fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="123a7-150">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="123a7-151">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="123a7-151">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="123a7-152">Le nom d’utilisateur et le mot de passe actuels ou spécifiés ne sont pas valides ou autorisés à établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="123a7-152">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="123a7-153">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="123a7-153">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="123a7-154">L’élément demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="123a7-154">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="123a7-155">Notes</span><span class="sxs-lookup"><span data-stu-id="123a7-155">Remarks</span></span>

<span data-ttu-id="123a7-156">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="123a7-156">This call returns immediately.</span></span> <span data-ttu-id="123a7-157">L’état de l’opération de suppression est retourné à l’appelant via un rappel remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="123a7-157">The status of the delete operation is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="123a7-158">Vous pouvez effectuer le traitement final dans votre implémentation de *objWbemSink*. Événement [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="123a7-158">You can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="123a7-159">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="123a7-159">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="123a7-160">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="123a7-160">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="123a7-161">Pour éliminer les risques, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="123a7-161">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="123a7-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="123a7-162">Requirements</span></span>



| <span data-ttu-id="123a7-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="123a7-163">Requirement</span></span> | <span data-ttu-id="123a7-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="123a7-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="123a7-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="123a7-165">Minimum supported client</span></span><br/> | <span data-ttu-id="123a7-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="123a7-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="123a7-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="123a7-167">Minimum supported server</span></span><br/> | <span data-ttu-id="123a7-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="123a7-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="123a7-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="123a7-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="123a7-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="123a7-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="123a7-171">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="123a7-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="123a7-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="123a7-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="123a7-173">DLL</span><span class="sxs-lookup"><span data-stu-id="123a7-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="123a7-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="123a7-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="123a7-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="123a7-175">CLSID</span></span><br/>                    | <span data-ttu-id="123a7-176">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="123a7-176">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="123a7-177">IID</span><span class="sxs-lookup"><span data-stu-id="123a7-177">IID</span></span><br/>                      | <span data-ttu-id="123a7-178">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="123a7-178">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="123a7-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="123a7-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123a7-180">**M**</span><span class="sxs-lookup"><span data-stu-id="123a7-180">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="123a7-181">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="123a7-181">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

