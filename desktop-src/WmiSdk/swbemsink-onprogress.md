---
description: L’événement OnProgress de SWbemSink est déclenché lorsqu’un appel asynchrone retourne l’état d’un appel en cours.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents :: OnProgress, événement (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536663"
---
# <a name="iswbemsinkeventsonprogress-event"></a><span data-ttu-id="199e6-103">ISWbemSinkEvents :: OnProgress, événement</span><span class="sxs-lookup"><span data-stu-id="199e6-103">ISWbemSinkEvents::OnProgress event</span></span>

<span data-ttu-id="199e6-104">L’événement **OnProgress** de [**SWbemSink**](swbemsink.md) est déclenché lorsqu’un appel asynchrone retourne l’état d’un appel en cours.</span><span class="sxs-lookup"><span data-stu-id="199e6-104">The **OnProgress** event of [**SWbemSink**](swbemsink.md) is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="199e6-105">Si les événements, les instances ou les classes sont produits à partir d’un fournisseur qui prend en charge les mises à jour d’État, vous pouvez placer le code dans cet événement pour fournir aux utilisateurs des commentaires sur l’état d’une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="199e6-105">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to provide users with feedback about the status of an asynchronous operation.</span></span> <span data-ttu-id="199e6-106">Vous devez définir le paramètre *IFlags* de l’appel asynchrone à **wbemFlagSendStatus** (128/0x80) si vous souhaitez recevoir des mises à jour d’État, sinon cet événement n’est pas déclenché.</span><span class="sxs-lookup"><span data-stu-id="199e6-106">You must set the *iFlags* parameter of the asynchronous call to **wbemFlagSendStatus** (128/0x80) if you want to receive status updates, otherwise this event is not triggered.</span></span>

<span data-ttu-id="199e6-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="199e6-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="199e6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="199e6-108">Syntax</span></span>


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="199e6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="199e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="199e6-110">*iUpperBound*</span><span class="sxs-lookup"><span data-stu-id="199e6-110">*iUpperBound*</span></span> 
</dt> <dd>

<span data-ttu-id="199e6-111">Entier qui décrit le nombre total de tâches à effectuer.</span><span class="sxs-lookup"><span data-stu-id="199e6-111">Integer that describes the total number of tasks to complete.</span></span>

</dd> <dt>

<span data-ttu-id="199e6-112">*iCurrent*</span><span class="sxs-lookup"><span data-stu-id="199e6-112">*iCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="199e6-113">Élément en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="199e6-113">Current item that is being processed.</span></span>

</dd> <dt>

<span data-ttu-id="199e6-114">*strMessage*</span><span class="sxs-lookup"><span data-stu-id="199e6-114">*strMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="199e6-115">Message qui décrit l’état de la tâche en cours.</span><span class="sxs-lookup"><span data-stu-id="199e6-115">Message that describes the status of the current task.</span></span>

</dd> <dt>

<span data-ttu-id="199e6-116">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="199e6-116">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="199e6-117">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui est passé à l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="199e6-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="199e6-118">Utilisez ce paramètre pour identifier l’origine de l’appel asynchrone qui déclenche cet événement lorsque plusieurs appels asynchrones sont effectués à l’aide de ce récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="199e6-118">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="199e6-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="199e6-119">Return value</span></span>

<span data-ttu-id="199e6-120">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="199e6-120">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="199e6-121">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="199e6-121">Error codes</span></span>

<span data-ttu-id="199e6-122">Une fois l’événement **OnProgress** terminé, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="199e6-122">After the completion of the **OnProgress** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="199e6-123">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="199e6-123">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="199e6-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="199e6-124">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="199e6-125">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="199e6-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="199e6-126">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="199e6-126">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="199e6-127">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="199e6-127">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="199e6-128">Une erreur réseau s’est produite, empêchant le fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="199e6-128">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="199e6-129">Notes</span><span class="sxs-lookup"><span data-stu-id="199e6-129">Remarks</span></span>

<span data-ttu-id="199e6-130">L’événement **OnProgress** est déclenché lorsqu’un appel asynchrone retourne l’état d’un appel en cours.</span><span class="sxs-lookup"><span data-stu-id="199e6-130">The **OnProgress** event is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="199e6-131">Si les événements, les instances ou les classes sont produits à partir d’un fournisseur qui prend en charge les mises à jour d’État, vous pouvez placer le code dans cet événement pour permettre aux utilisateurs de fournir des commentaires sur l’état d’une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="199e6-131">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to give users feedback about the status of an asynchronous operation.</span></span>

> [!Note]  
> <span data-ttu-id="199e6-132">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="199e6-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="199e6-133">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="199e6-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="199e6-134">Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone.</span><span class="sxs-lookup"><span data-stu-id="199e6-134">To eliminate the risks, use semi-synchronous or synchronous communication.</span></span> <span data-ttu-id="199e6-135">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="199e6-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="199e6-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="199e6-136">Requirements</span></span>



| <span data-ttu-id="199e6-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="199e6-137">Requirement</span></span> | <span data-ttu-id="199e6-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="199e6-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="199e6-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="199e6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="199e6-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="199e6-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="199e6-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="199e6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="199e6-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="199e6-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="199e6-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="199e6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="199e6-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="199e6-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="199e6-145">MIDL</span><span class="sxs-lookup"><span data-stu-id="199e6-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="199e6-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="199e6-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="199e6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="199e6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="199e6-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="199e6-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="199e6-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="199e6-149">CLSID</span></span><br/>                    | <span data-ttu-id="199e6-150">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="199e6-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="199e6-151">IID</span><span class="sxs-lookup"><span data-stu-id="199e6-151">IID</span></span><br/>                      | <span data-ttu-id="199e6-152">IID \_ ISWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="199e6-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="199e6-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="199e6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="199e6-154">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="199e6-154">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

