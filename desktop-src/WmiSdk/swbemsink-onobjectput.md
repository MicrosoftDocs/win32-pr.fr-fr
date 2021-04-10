---
description: L’événement OnObjectPut d’un objet SWbemSink est déclenché lorsqu’une opération put asynchrone est terminée. Cet événement retourne le chemin d’accès de l’objet de l’instance ou de la classe enregistrée.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents :: OnObjectPut, événement (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c6ed42105efe407558d80cd108e657e396e88763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210728"
---
# <a name="iswbemsinkeventsonobjectput-event"></a><span data-ttu-id="2d5da-104">Événement ISWbemSinkEvents :: OnObjectPut</span><span class="sxs-lookup"><span data-stu-id="2d5da-104">ISWbemSinkEvents::OnObjectPut event</span></span>

<span data-ttu-id="2d5da-105">L’événement **OnObjectPut** d’un objet [**SWbemSink**](swbemsink.md) est déclenché lorsqu’une opération put asynchrone est terminée.</span><span class="sxs-lookup"><span data-stu-id="2d5da-105">The **OnObjectPut** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous Put operation is complete.</span></span> <span data-ttu-id="2d5da-106">Cet événement retourne le chemin d’accès de l’objet de l’instance ou de la classe enregistrée.</span><span class="sxs-lookup"><span data-stu-id="2d5da-106">This event returns the object path of the instance or the saved class.</span></span>

<span data-ttu-id="2d5da-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2d5da-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d5da-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d5da-108">Syntax</span></span>


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="2d5da-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d5da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d5da-110">*objWbemObjectPath*</span><span class="sxs-lookup"><span data-stu-id="2d5da-110">*objWbemObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="2d5da-111">Objet [**SWbemObjectPath**](swbemobjectpath.md) , qui contient le chemin d’accès de l’objet de l’instance ou de la classe que l’opération Put écrit dans WMI.</span><span class="sxs-lookup"><span data-stu-id="2d5da-111">An [**SWbemObjectPath**](swbemobjectpath.md) object, that contains the object path of the instance or class that the put operation writes to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="2d5da-112">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="2d5da-112">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="2d5da-113">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui est passé à l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="2d5da-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="2d5da-114">Utilisez ce paramètre pour identifier l’origine de l’appel asynchrone qui déclenche cet événement lorsque plusieurs appels asynchrones sont effectués à l’aide de ce récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="2d5da-114">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d5da-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d5da-115">Return value</span></span>

<span data-ttu-id="2d5da-116">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2d5da-116">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2d5da-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="2d5da-117">Error codes</span></span>

<span data-ttu-id="2d5da-118">Une fois l’événement **OnObjectPut** terminé, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2d5da-118">After the completion of the **OnObjectPut** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="2d5da-119">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2d5da-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2d5da-120">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2d5da-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2d5da-121">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="2d5da-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2d5da-122">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="2d5da-122">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2d5da-123">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="2d5da-123">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="2d5da-124">Une erreur réseau s’est produite, empêchant le fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="2d5da-124">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d5da-125">Notes</span><span class="sxs-lookup"><span data-stu-id="2d5da-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2d5da-126">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="2d5da-126">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="2d5da-127">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="2d5da-127">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="2d5da-128">Pour éliminer les risques, utilisez une communication semi-synchrone ou une communication synchrone.</span><span class="sxs-lookup"><span data-stu-id="2d5da-128">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="2d5da-129">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2d5da-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d5da-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d5da-130">Requirements</span></span>



| <span data-ttu-id="2d5da-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d5da-131">Requirement</span></span> | <span data-ttu-id="2d5da-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d5da-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5da-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d5da-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2d5da-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d5da-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d5da-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d5da-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2d5da-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d5da-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d5da-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d5da-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d5da-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d5da-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d5da-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="2d5da-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d5da-140"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d5da-140"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2d5da-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2d5da-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d5da-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d5da-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2d5da-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="2d5da-143">CLSID</span></span><br/>                    | <span data-ttu-id="2d5da-144">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="2d5da-144">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="2d5da-145">IID</span><span class="sxs-lookup"><span data-stu-id="2d5da-145">IID</span></span><br/>                      | <span data-ttu-id="2d5da-146">IID \_ ISWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="2d5da-146">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="2d5da-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d5da-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d5da-148">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="2d5da-148">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

