---
description: La méthode Cancel de l’objet SWbemSink annule toutes les opérations asynchrones en suspens associées à ce récepteur d’objets.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'ISWbemSink :: Cancel, méthode (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210729"
---
# <a name="iswbemsinkcancel-method"></a><span data-ttu-id="bbcd8-103">ISWbemSink :: Cancel, méthode</span><span class="sxs-lookup"><span data-stu-id="bbcd8-103">ISWbemSink::Cancel method</span></span>

<span data-ttu-id="bbcd8-104">La méthode **Cancel** de l’objet [**SWbemSink**](swbemsink.md) annule toutes les opérations asynchrones en suspens associées à ce récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-104">The **Cancel** method of the [**SWbemSink**](swbemsink.md) object cancels all outstanding asynchronous operations that are associated with this object sink.</span></span>

<span data-ttu-id="bbcd8-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bbcd8-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bbcd8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbcd8-106">Syntax</span></span>


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a><span data-ttu-id="bbcd8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbcd8-107">Parameters</span></span>

<span data-ttu-id="bbcd8-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbcd8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bbcd8-109">Return value</span></span>

<span data-ttu-id="bbcd8-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-110">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bbcd8-111">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="bbcd8-111">Error codes</span></span>

<span data-ttu-id="bbcd8-112">Une fois la méthode **Cancel** terminée, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-112">After the completion of the **Cancel** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="bbcd8-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="bbcd8-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bbcd8-114">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="bbcd8-115">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="bbcd8-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="bbcd8-116">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-116">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bbcd8-117">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="bbcd8-117">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="bbcd8-118">Une erreur réseau s’est produite, empêchant le fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-118">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="bbcd8-119">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="bbcd8-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="bbcd8-120">Le nom d’utilisateur et le mot de passe actuels ou spécifiés ne sont pas valides ou autorisés à établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-120">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bbcd8-121">Notes</span><span class="sxs-lookup"><span data-stu-id="bbcd8-121">Remarks</span></span>

<span data-ttu-id="bbcd8-122">Vous ne pouvez pas annuler un seul appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-122">You cannot cancel only one asynchronous call.</span></span> <span data-ttu-id="bbcd8-123">Si plusieurs appels asynchrones sont en attente qui utilisent ce récepteur d’objets, cette méthode annule tous les appels asynchrones à l’aide de ce récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-123">If multiple asynchronous calls are pending that use this object sink, then this method cancels all the asynchronous calls using this object sink.</span></span> <span data-ttu-id="bbcd8-124">Les appels asynchrones associés à d’autres récepteurs d’objets ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-124">Asynchronous calls that are associated with other object sinks continue unaffected.</span></span>

<span data-ttu-id="bbcd8-125">Vous ne pouvez pas assigner à ce récepteur la valeur **Nothing** pour annuler une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-125">You cannot assign this sink to **Nothing** to cancel an asynchronous operation.</span></span> <span data-ttu-id="bbcd8-126">Vous devez appeler la méthode **Cancel** pour que WMI interrompe l’opération et libère les ressources associées.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-126">You must call the **Cancel** method to make WMI discontinue the operation and free the associated resources.</span></span> <span data-ttu-id="bbcd8-127">Cela est très important avec les opérations asynchrones longues, telles que les requêtes, ou les opérations qui ne se terminent jamais, telles que [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="bbcd8-127">This is very important with lengthy asynchronous operations, such as queries, or operations that never complete, such as [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span>

> [!Note]  
> <span data-ttu-id="bbcd8-128">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-128">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="bbcd8-129">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-129">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="bbcd8-130">Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-130">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="bbcd8-131">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="bbcd8-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="bbcd8-132">L’exemple suivant montre comment annuler un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-132">The following example shows you how to cancel an asynchronous call.</span></span>


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a><span data-ttu-id="bbcd8-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbcd8-133">Requirements</span></span>



| <span data-ttu-id="bbcd8-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbcd8-134">Requirement</span></span> | <span data-ttu-id="bbcd8-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbcd8-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbcd8-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbcd8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bbcd8-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbcd8-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bbcd8-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbcd8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bbcd8-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbcd8-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bbcd8-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="bbcd8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbcd8-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbcd8-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbcd8-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="bbcd8-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bbcd8-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bbcd8-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="bbcd8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="bbcd8-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbcd8-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbcd8-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bbcd8-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="bbcd8-146">CLSID</span></span><br/>                    | <span data-ttu-id="bbcd8-147">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="bbcd8-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="bbcd8-148">IID</span><span class="sxs-lookup"><span data-stu-id="bbcd8-148">IID</span></span><br/>                      | <span data-ttu-id="bbcd8-149">IID \_ ISWbemSink</span><span class="sxs-lookup"><span data-stu-id="bbcd8-149">IID\_ISWbemSink</span></span><br/>                                                              |



## <a name="see-also"></a><span data-ttu-id="bbcd8-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbcd8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbcd8-151">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="bbcd8-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

