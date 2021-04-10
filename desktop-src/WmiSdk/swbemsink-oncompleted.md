---
description: L’événement OnCompleted d’un objet SWbemSink est déclenché lorsqu’un appel asynchrone est terminé. Cet événement indique à l’application cliente le résultat d’une opération asynchrone et fournit des informations d’erreur lorsque l’appel asynchrone échoue.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents :: OnCompleted, événement (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114850"
---
# <a name="iswbemsinkeventsoncompleted-event"></a><span data-ttu-id="0f6a6-104">Événement ISWbemSinkEvents :: OnCompleted</span><span class="sxs-lookup"><span data-stu-id="0f6a6-104">ISWbemSinkEvents::OnCompleted event</span></span>

<span data-ttu-id="0f6a6-105">L’événement **OnCompleted** d’un objet [**SWbemSink**](swbemsink.md) est déclenché lorsqu’un appel asynchrone est terminé.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-105">The **OnCompleted** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous call is complete.</span></span> <span data-ttu-id="0f6a6-106">Cet événement indique à l’application cliente le résultat d’une opération asynchrone et fournit des informations d’erreur lorsque l’appel asynchrone échoue.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-106">This event indicates to the client application, the result of an asynchronous operation, and provides error information when the asynchronous call fails.</span></span>

<span data-ttu-id="0f6a6-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0f6a6-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6a6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f6a6-108">Syntax</span></span>


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="0f6a6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f6a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f6a6-110">*iHResult*</span><span class="sxs-lookup"><span data-stu-id="0f6a6-110">*iHResult*</span></span> 
</dt> <dd>

<span data-ttu-id="0f6a6-111">HRESULT de la méthode asynchrone terminée.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-111">The HRESULT of the completed asynchronous method.</span></span> <span data-ttu-id="0f6a6-112">HRESULT est identique à la valeur retournée à partir d’une [API com](com-api-for-wmi.md) équivalente pour l’appel de méthode WMI.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-112">The HRESULT is the same as the value that is returned from an equivalent [COM API for WMI](com-api-for-wmi.md) method call.</span></span> <span data-ttu-id="0f6a6-113">Vérifiez cette valeur pour déterminer si l’appel asynchrone a réussi ou non.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-113">Check this value to determine whether or not the asynchronous call is successful.</span></span> <span data-ttu-id="0f6a6-114">Si l’appel asynchrone réussit, ce paramètre contient WBEM \_ S \_ no \_ Error (0).</span><span class="sxs-lookup"><span data-stu-id="0f6a6-114">If the asynchronous call is successful, this parameter contains WBEM\_S\_NO\_ERROR (0).</span></span> <span data-ttu-id="0f6a6-115">Si l’appel asynchrone échoue, ce paramètre contient un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-115">If the asynchronous call fails, this parameter contains an error code.</span></span>

</dd> <dt>

<span data-ttu-id="0f6a6-116">*objWbemErrorObject*</span><span class="sxs-lookup"><span data-stu-id="0f6a6-116">*objWbemErrorObject*</span></span> 
</dt> <dd>

<span data-ttu-id="0f6a6-117">Contient un objet [**SWbemLastError**](swbemlasterror.md) en cas d’échec de la méthode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-117">Contains an [**SWbemLastError**](swbemlasterror.md) object when the asynchronous method fails.</span></span>

</dd> <dt>

<span data-ttu-id="0f6a6-118">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="0f6a6-118">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="0f6a6-119">Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui est passé à l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-119">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="0f6a6-120">Utilisez ce paramètre pour identifier l’origine de l’appel asynchrone qui déclenche cet événement lorsque plusieurs appels asynchrones sont effectués à l’aide de ce récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-120">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f6a6-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f6a6-121">Return value</span></span>

<span data-ttu-id="0f6a6-122">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-122">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0f6a6-123">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0f6a6-123">Error codes</span></span>

<span data-ttu-id="0f6a6-124">Une fois l’événement **OnCompleted** terminé, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-124">After completion of the **OnCompleted** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="0f6a6-125">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0f6a6-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0f6a6-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-126">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="0f6a6-127">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="0f6a6-127">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0f6a6-128">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-128">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0f6a6-129">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="0f6a6-129">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="0f6a6-130">Une erreur réseau s’est produite, empêchant le fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-130">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f6a6-131">Notes</span><span class="sxs-lookup"><span data-stu-id="0f6a6-131">Remarks</span></span>

<span data-ttu-id="0f6a6-132">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="0f6a6-133">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="0f6a6-134">Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone.</span><span class="sxs-lookup"><span data-stu-id="0f6a6-134">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="0f6a6-135">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0f6a6-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6a6-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f6a6-136">Requirements</span></span>



| <span data-ttu-id="0f6a6-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f6a6-137">Requirement</span></span> | <span data-ttu-id="0f6a6-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f6a6-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6a6-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f6a6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0f6a6-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f6a6-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f6a6-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f6a6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0f6a6-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f6a6-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f6a6-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f6a6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f6a6-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f6a6-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f6a6-145">MIDL</span><span class="sxs-lookup"><span data-stu-id="0f6a6-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f6a6-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f6a6-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="0f6a6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0f6a6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f6a6-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f6a6-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f6a6-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="0f6a6-149">CLSID</span></span><br/>                    | <span data-ttu-id="0f6a6-150">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="0f6a6-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="0f6a6-151">IID</span><span class="sxs-lookup"><span data-stu-id="0f6a6-151">IID</span></span><br/>                      | <span data-ttu-id="0f6a6-152">IID \_ ISWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="0f6a6-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



 

