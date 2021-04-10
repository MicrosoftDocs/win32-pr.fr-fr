---
description: L’événement OnObjectReady d’un objet SWbemSink est déclenché lorsqu’une opération asynchrone retourne un objet.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents :: OnObjectReady, événement (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114846"
---
# <a name="iswbemsinkeventsonobjectready-event"></a><span data-ttu-id="5e95c-103">Événement ISWbemSinkEvents :: OnObjectReady</span><span class="sxs-lookup"><span data-stu-id="5e95c-103">ISWbemSinkEvents::OnObjectReady event</span></span>

<span data-ttu-id="5e95c-104">L’événement **OnObjectReady** d’un objet [**SWbemSink**](swbemsink.md) est déclenché lorsqu’une opération asynchrone retourne un objet.</span><span class="sxs-lookup"><span data-stu-id="5e95c-104">The **OnObjectReady** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous operation returns an object.</span></span> <span data-ttu-id="5e95c-105">Utilisez cet événement pour traiter des objets à partir d’appels asynchrones tels que [**SWbemObject. InstancesAsync \_**](swbemobject-instancesasync-.md) ou [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="5e95c-105">Use this event to process objects from asynchronous calls such as [**SWbemObject.InstancesAsync\_**](swbemobject-instancesasync-.md) or [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span></span> <span data-ttu-id="5e95c-106">**OnObjectReady** retourne un [**SWbemObject**](swbemobject.md) chaque fois que l’énumération est terminée.</span><span class="sxs-lookup"><span data-stu-id="5e95c-106">**OnObjectReady** returns one [**SWbemObject**](swbemobject.md) each time until the enumeration is complete.</span></span>

<span data-ttu-id="5e95c-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5e95c-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e95c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e95c-108">Syntax</span></span>


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="5e95c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e95c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e95c-110">*objWbemObject*</span><span class="sxs-lookup"><span data-stu-id="5e95c-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="5e95c-111">Objet [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="5e95c-111">An [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="5e95c-112">Cela est similaire à ce qui est retourné par l’équivalent synchrone de l’appel asynchrone qui déclenche cet événement.</span><span class="sxs-lookup"><span data-stu-id="5e95c-112">This is similar to what is returned by the synchronous equivalent of the asynchronous call that triggers this event.</span></span> <span data-ttu-id="5e95c-113">Par exemple, un appel à la méthode [**SWbemServices. GetAsync**](swbemservices-getasync.md) renvoie un **SWbemObject** dans le *paramètre objWbemObject* de l’événement **OnObjectReady** de l’objet [**SWbemSink**](swbemsink.md) , qui est passé comme paramètre *objWbemObject* de l’appel d’origine.</span><span class="sxs-lookup"><span data-stu-id="5e95c-113">For example, a call to the [**SWbemServices.GetAsync**](swbemservices-getasync.md) method returns an **SWbemObject** in the *objWbemObject* parameter of the **OnObjectReady** event of the [**SWbemSink**](swbemsink.md) object, which is passed as the *objWbemObject* parameter of the original call.</span></span> <span data-ttu-id="5e95c-114">Le même objet **SWbemObject** peut être obtenu à l’aide d’un appel synchrone équivalent à [**SWbemServices. obtenir**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="5e95c-114">The same **SWbemObject** object can be obtained by using an equivalent synchronous call to [**SWbemServices.Get**](swbemservices-get.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e95c-115">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="5e95c-115">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="5e95c-116">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui est passé à l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="5e95c-116">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="5e95c-117">Utilisez ce paramètre pour identifier l’origine de l’appel asynchrone qui déclenche cet événement lorsque plusieurs appels asynchrones sont effectués à l’aide de ce récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="5e95c-117">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e95c-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e95c-118">Return value</span></span>

<span data-ttu-id="5e95c-119">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5e95c-119">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5e95c-120">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5e95c-120">Error codes</span></span>

<span data-ttu-id="5e95c-121">Une fois l’événement **OnObjectReady** terminé, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5e95c-121">After the completion of the **OnObjectReady** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="5e95c-122">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5e95c-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5e95c-123">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5e95c-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5e95c-124">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5e95c-124">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5e95c-125">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5e95c-125">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5e95c-126">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="5e95c-126">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="5e95c-127">Une erreur réseau s’est produite, empêchant le fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="5e95c-127">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e95c-128">Notes</span><span class="sxs-lookup"><span data-stu-id="5e95c-128">Remarks</span></span>

<span data-ttu-id="5e95c-129">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="5e95c-129">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="5e95c-130">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="5e95c-130">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="5e95c-131">Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone.</span><span class="sxs-lookup"><span data-stu-id="5e95c-131">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="5e95c-132">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5e95c-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e95c-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e95c-133">Requirements</span></span>



| <span data-ttu-id="5e95c-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e95c-134">Requirement</span></span> | <span data-ttu-id="5e95c-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e95c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e95c-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e95c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5e95c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e95c-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e95c-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e95c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5e95c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e95c-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e95c-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e95c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e95c-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e95c-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e95c-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="5e95c-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e95c-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e95c-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e95c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5e95c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e95c-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e95c-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5e95c-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="5e95c-146">CLSID</span></span><br/>                    | <span data-ttu-id="5e95c-147">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="5e95c-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="5e95c-148">IID</span><span class="sxs-lookup"><span data-stu-id="5e95c-148">IID</span></span><br/>                      | <span data-ttu-id="5e95c-149">IID \_ ISWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="5e95c-149">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="5e95c-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e95c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e95c-151">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="5e95c-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

