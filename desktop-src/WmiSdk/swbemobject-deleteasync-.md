---
description: La \_ méthode DeleteAsync de SWbemObject supprime de manière asynchrone la classe actuelle ou l’instance actuelle.
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.tgt_platform: multiple
title: Méthode SWbemObject.DeleteAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7951b84a2b5d9f06061f4cefb04c797ccfea3ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521490"
---
# <a name="swbemobjectdeleteasync_-method"></a><span data-ttu-id="43136-103">SWbemObject. DeleteAsync, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="43136-103">SWbemObject.DeleteAsync\_ method</span></span>

<span data-ttu-id="43136-104">La **méthode \_ DeleteAsync** de [**SWbemObject**](swbemobject.md) supprime de manière asynchrone la classe actuelle ou l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="43136-104">The **DeleteAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously deletes either the current class or the current instance.</span></span> <span data-ttu-id="43136-105">Si un fournisseur dynamique fournit la classe ou l’instance, il n’est pas toujours possible de supprimer cet objet, sauf si le fournisseur prend en charge la suppression de classe ou d’instance.</span><span class="sxs-lookup"><span data-stu-id="43136-105">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="43136-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="43136-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="43136-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43136-107">Syntax</span></span>


```VB
SWbemObject.DeleteAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="43136-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43136-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43136-109">*objWbemSink* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43136-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43136-110">Récepteur d’objets qui retourne le résultat de l’opération de suppression.</span><span class="sxs-lookup"><span data-stu-id="43136-110">Object sink that returns the outcome of the delete operation.</span></span>

</dd> <dt>

<span data-ttu-id="43136-111">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="43136-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43136-112">Entier qui détermine le comportement de l’appel.</span><span class="sxs-lookup"><span data-stu-id="43136-112">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="43136-113">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="43136-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="43136-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="43136-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="43136-115">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**SWbemSink. OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="43136-115">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="43136-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="43136-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="43136-117">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="43136-117">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="43136-118">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="43136-118">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43136-119">Ce paramètre n’est généralement pas défini.</span><span class="sxs-lookup"><span data-stu-id="43136-119">This parameter is typically undefined.</span></span> <span data-ttu-id="43136-120">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="43136-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="43136-121">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="43136-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="43136-122">*objWbemAsyncContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="43136-122">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43136-123">Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="43136-123">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="43136-124">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="43136-124">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="43136-125">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="43136-125">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="43136-126">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="43136-126">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="43136-127">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="43136-127">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43136-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43136-128">Return value</span></span>

<span data-ttu-id="43136-129">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="43136-129">This method does not return a value.</span></span> <span data-ttu-id="43136-130">Si cet appel réussit, le résultat de l’opération de suppression est fourni par le biais du récepteur d’objets fourni.</span><span class="sxs-lookup"><span data-stu-id="43136-130">If this call is successful, the result of the delete operation is provided through the supplied object sink.</span></span>

## <a name="error-codes"></a><span data-ttu-id="43136-131">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="43136-131">Error codes</span></span>

<span data-ttu-id="43136-132">À la fin de la **méthode \_ DeleteAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="43136-132">After the completion of the **DeleteAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="43136-133">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="43136-133">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="43136-134">Le contexte actuel ne dispose pas des droits de sécurité adéquats pour supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="43136-134">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="43136-135">**wbemErrFailed** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="43136-135">**wbemErrFailed** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="43136-136">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="43136-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="43136-137">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="43136-137">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="43136-138">La classe spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="43136-138">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="43136-139">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="43136-139">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="43136-140">Impossible de supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="43136-140">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="43136-141">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="43136-141">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="43136-142">L’objet n’existait pas.</span><span class="sxs-lookup"><span data-stu-id="43136-142">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="43136-143">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="43136-143">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="43136-144">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="43136-144">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43136-145">Notes</span><span class="sxs-lookup"><span data-stu-id="43136-145">Remarks</span></span>

<span data-ttu-id="43136-146">Cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="43136-146">This call returns immediately.</span></span> <span data-ttu-id="43136-147">L’État est retourné à l’appelant via un rappel remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="43136-147">The status is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="43136-148">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="43136-148">An asynchronous callback allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="43136-149">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="43136-149">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="43136-150">Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone.</span><span class="sxs-lookup"><span data-stu-id="43136-150">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="43136-151">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="43136-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43136-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43136-152">Requirements</span></span>



| <span data-ttu-id="43136-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43136-153">Requirement</span></span> | <span data-ttu-id="43136-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="43136-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43136-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43136-155">Minimum supported client</span></span><br/> | <span data-ttu-id="43136-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43136-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43136-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43136-157">Minimum supported server</span></span><br/> | <span data-ttu-id="43136-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43136-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43136-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="43136-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="43136-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="43136-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="43136-161">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="43136-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="43136-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="43136-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="43136-163">DLL</span><span class="sxs-lookup"><span data-stu-id="43136-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43136-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43136-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="43136-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="43136-165">CLSID</span></span><br/>                    | <span data-ttu-id="43136-166">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="43136-166">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="43136-167">IID</span><span class="sxs-lookup"><span data-stu-id="43136-167">IID</span></span><br/>                      | <span data-ttu-id="43136-168">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="43136-168">IID\_ISWbemObject</span></span><br/>                                                            |



 

