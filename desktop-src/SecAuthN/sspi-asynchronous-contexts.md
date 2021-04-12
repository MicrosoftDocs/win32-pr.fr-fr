---
title: Contextes asynchrones
description: Vue d’ensemble des contextes asynchrones et de l’en-tête SSPI asynchrone.
ms.topic: article
ms.keywords: SSPI, Asynchronous Contexts, async contexts, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e523112d35e0ddbc38c3374c67e3d81ba74a6dce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319894"
---
# <a name="asynchronous-contexts"></a><span data-ttu-id="2b741-103">Contextes asynchrones</span><span class="sxs-lookup"><span data-stu-id="2b741-103">Asynchronous Contexts</span></span>

<span data-ttu-id="2b741-104">Les contextes de sécurité SSPI asynchrones permettent aux appelants de continuer sans bloquer et recevoir des notifications une fois l’appel terminé.</span><span class="sxs-lookup"><span data-stu-id="2b741-104">Asynchronous SSPI security contexts allow callers to proceed without blocking and receive notifications once the call completes.</span></span> <span data-ttu-id="2b741-105">Les contextes asynchrones sont actuellement pris en charge uniquement pour les serveurs et les clients TLS en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="2b741-105">Asynchronous contexts are currently only supported for kernel-mode TLS clients and servers.</span></span> <span data-ttu-id="2b741-106">Les fonctions SSPI asynchrones suivantes fonctionnent sur les contextes de sécurité asynchrones :</span><span class="sxs-lookup"><span data-stu-id="2b741-106">The following asynchronous SSPI functions operate on asynchronous security contexts:</span></span>

## <a name="async-context-management-types"></a><span data-ttu-id="2b741-107">Types de gestion de contexte Async</span><span class="sxs-lookup"><span data-stu-id="2b741-107">Async context management types</span></span>

| <span data-ttu-id="2b741-108">Nom d’objet</span><span class="sxs-lookup"><span data-stu-id="2b741-108">Object Name</span></span> | <span data-ttu-id="2b741-109">Description</span><span class="sxs-lookup"><span data-stu-id="2b741-109">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="2b741-110">SspiAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="2b741-110">SspiAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | <span data-ttu-id="2b741-111">Rappel utilisé pour notifier l’achèvement d’un appel SSPI asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2b741-111">Callback used for notifying completion of an async SSPI call.</span></span> |


## <a name="async-context-management-functions"></a><span data-ttu-id="2b741-112">Fonctions de gestion de contexte Async</span><span class="sxs-lookup"><span data-stu-id="2b741-112">Async context management functions</span></span>

| <span data-ttu-id="2b741-113">Nom de l’API</span><span class="sxs-lookup"><span data-stu-id="2b741-113">API Name</span></span> | <span data-ttu-id="2b741-114">Description</span><span class="sxs-lookup"><span data-stu-id="2b741-114">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="2b741-115">SspiCreateAsyncContext</span><span class="sxs-lookup"><span data-stu-id="2b741-115">SspiCreateAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | <span data-ttu-id="2b741-116">Crée une instance de SspiAsyncContext qui est utilisée pour effectuer le suivi de l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2b741-116">Creates an instance of SspiAsyncContext which is used to track the async call.</span></span> |
| [<span data-ttu-id="2b741-117">SspiReinitAsyncContext</span><span class="sxs-lookup"><span data-stu-id="2b741-117">SspiReinitAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | <span data-ttu-id="2b741-118">Marque un contexte Async pour la réutilisation.</span><span class="sxs-lookup"><span data-stu-id="2b741-118">Marks an async context for reuse.</span></span> |
| [<span data-ttu-id="2b741-119">SspiSetAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="2b741-119">SspiSetAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | <span data-ttu-id="2b741-120">Inscrit un rappel qui est notifié de la fin de l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2b741-120">Registers a callback that is notified on async call completion.</span></span> |
| [<span data-ttu-id="2b741-121">SspiAsyncContextRequiresNotify</span><span class="sxs-lookup"><span data-stu-id="2b741-121">SspiAsyncContextRequiresNotify</span></span>](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | <span data-ttu-id="2b741-122">Détermine si un contexte asynchrone donné requiert une notification à la fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="2b741-122">Determines whether a given async context requires notification on completion of the call.</span></span> |
| [<span data-ttu-id="2b741-123">SspiGetAsyncCallStatus</span><span class="sxs-lookup"><span data-stu-id="2b741-123">SspiGetAsyncCallStatus</span></span>](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | <span data-ttu-id="2b741-124">Obtient l’état actuel d’un appel asynchrone associé au contexte fourni.</span><span class="sxs-lookup"><span data-stu-id="2b741-124">Gets the current status of an async call associated with the provided context.</span></span>  |
| [<span data-ttu-id="2b741-125">SspiFreeAsyncContext</span><span class="sxs-lookup"><span data-stu-id="2b741-125">SspiFreeAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | <span data-ttu-id="2b741-126">Libère un contexte créé dans l’appel à la fonction SspiCreateAsyncContext.</span><span class="sxs-lookup"><span data-stu-id="2b741-126">Frees up a context created in the call to the SspiCreateAsyncContext function.</span></span> |

## <a name="async-sspi-functions"></a><span data-ttu-id="2b741-127">Fonctions SSPI Async</span><span class="sxs-lookup"><span data-stu-id="2b741-127">Async SSPI functions</span></span>

<span data-ttu-id="2b741-128">Les fonctions suivantes acceptent un contexte asynchrone en plus de tous les mêmes paramètres que leur équivalent synchrone.</span><span class="sxs-lookup"><span data-stu-id="2b741-128">The following functions accept an async context in addition to all the same parameters as their synchronous counterpart.</span></span>

| <span data-ttu-id="2b741-129">Nom de l’API</span><span class="sxs-lookup"><span data-stu-id="2b741-129">API Name</span></span> | <span data-ttu-id="2b741-130">Description</span><span class="sxs-lookup"><span data-stu-id="2b741-130">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="2b741-131">SspiAcquireCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="2b741-131">SspiAcquireCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | <span data-ttu-id="2b741-132">Acquiert de manière asynchrone un handle pour les informations d’identification préexistantes d’un principal de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2b741-132">Asynchronously acquires a handle to preexisting credentials of a security principal.</span></span> |
| [<span data-ttu-id="2b741-133">SspiAcceptSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="2b741-133">SspiAcceptSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | <span data-ttu-id="2b741-134">Permet au composant serveur d’une application de transport d’établir de façon asynchrone un contexte de sécurité entre le serveur et un client distant.</span><span class="sxs-lookup"><span data-stu-id="2b741-134">Lets the server component of a transport application asynchronously establish a security context between the server and a remote client.</span></span> |
| [<span data-ttu-id="2b741-135">SspiInitializeSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="2b741-135">SspiInitializeSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | <span data-ttu-id="2b741-136">Initialise un contexte de sécurité Async.</span><span class="sxs-lookup"><span data-stu-id="2b741-136">Initializes an async security context.</span></span> |
| [<span data-ttu-id="2b741-137">SspiDeleteSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="2b741-137">SspiDeleteSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | <span data-ttu-id="2b741-138">Supprime les structures de données locales associées au contexte de sécurité spécifié initié par un appel précédent à la fonction SspiInitializeSecurityContextAsync ou à la fonction SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="2b741-138">Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.</span></span> |
| [<span data-ttu-id="2b741-139">SspiFreeCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="2b741-139">SspiFreeCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | <span data-ttu-id="2b741-140">Libère un handle d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="2b741-140">Frees up a credential handle.</span></span> |

## <a name="api-sample"></a><span data-ttu-id="2b741-141">Exemple d’API</span><span class="sxs-lookup"><span data-stu-id="2b741-141">API Sample</span></span>

<span data-ttu-id="2b741-142">Un workflow d’appel classique fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="2b741-142">A typical call flow works as follows:</span></span>
1) <span data-ttu-id="2b741-143">Créer un contexte SspiAsyncContext pour suivre l’appel à l’aide de [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span><span class="sxs-lookup"><span data-stu-id="2b741-143">Create SspiAsyncContext context to track call using [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span></span>
2) <span data-ttu-id="2b741-144">Inscrire un [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) pour le contexte</span><span class="sxs-lookup"><span data-stu-id="2b741-144">Register an [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) for the context</span></span>
3) <span data-ttu-id="2b741-145">Effectuer l’appel asynchrone à l’aide de [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span><span class="sxs-lookup"><span data-stu-id="2b741-145">Make the async call using [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span></span>
4) <span data-ttu-id="2b741-146">Sur le rappel, récupérez le résultat à l’aide de [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span><span class="sxs-lookup"><span data-stu-id="2b741-146">On callback, retrieve the result using [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span></span>
5) <span data-ttu-id="2b741-147">Supprimez SspiAsyncContext à l’aide de [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span><span class="sxs-lookup"><span data-stu-id="2b741-147">Delete SspiAsyncContext using [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span></span> <span data-ttu-id="2b741-148">Si vous réutilisez le contexte avec [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), revenez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="2b741-148">If reusing the context with [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), go back to step 2.</span></span>

<span data-ttu-id="2b741-149">L’exemple ci-dessous illustre un appel de SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="2b741-149">The sample below demonstrates an invocation of SspiAcceptSecurityContextAsync.</span></span> <span data-ttu-id="2b741-150">L’exemple attend la fin de l’appel et récupère le résultat.</span><span class="sxs-lookup"><span data-stu-id="2b741-150">The sample waits for the call to complete and retrieves the result.</span></span>

<span data-ttu-id="2b741-151">Dans une négociation SSPI complète, SspiAcceptSecurityContextAsync et SspiInitializeSecurityContextAsync sont appelées plusieurs fois jusqu’à ce que SEC_E_OK soit retourné.</span><span class="sxs-lookup"><span data-stu-id="2b741-151">In a full SSPI handshake, SspiAcceptSecurityContextAsync and SspiInitializeSecurityContextAsync would be called multiple times until SEC_E_OK is returned.</span></span> <span data-ttu-id="2b741-152">SspiReinitAsyncContext a été fourni pour une facilité d’utilisation et pour faciliter les performances dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="2b741-152">SspiReinitAsyncContext has been provided for ease of use and to facilitate performance in this case.</span></span>

<span data-ttu-id="2b741-153">Les assertions sont utilisées pour mettre en évidence ce que nous attendons dans le cas d’une réussite.</span><span class="sxs-lookup"><span data-stu-id="2b741-153">Asserts are used to highlight what we would expect in the case of success.</span></span>

```cpp
#include <sspi.h>

void AsyncCallCompleted(
    _In_     SspiAsyncContext* AsyncContext,
    _In_opt_ PVOID pCallbackData
)
{
    // Get result.
    SECURITY_STATUS Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_E_OK == Status);

    // *Perform any needed callback actions, use pCallbackData if needed*

    // Clean up async context when done.
    SspiFreeAsyncContext(AsyncContext);
}

void DoASCCall(
    _In_opt_  PCredHandle    phCred,
    _In_opt_  PCtxtHandle    phContext,
    _In_opt_  PSecBufferDesc pInput,
    _In_opt_  PSecBufferDesc pOutput,
    _Out_     unsigned long* pfContextAttr,
    _Out_opt_ PTimeStamp     ptsExpiry
)
{
    // Create context for async call
    SspiAsyncContext* AsyncContext = SspiCreateAsyncContext();

    // Check for out of memory condition
    ASSERT(AsyncContext);

    // Register callback that continues execution upon completion.
    PVOID pCallbackData = … ; // *Setup any state needed for callback.*
    SECURITY_STATUS Status = SspiSetAsyncNotifyCallback(AsyncContext,
                                        AsyncCallCompleted,
                                        pCallbackData);
    ASSERT(SEC_E_OK == Status);

    // Queue asynchronous call.
    Status = SspiAcceptSecurityContextAsync(AsyncContext,
                                            phCred,
                                            phContext,
                                            pInput,
                                            ASC_REQ_CONNECTION,
                                            SECURITY_NATIVE_DREP,
                                            phContext,
                                            pOutput,
                                            pfContextAttr,
                                            ptsExpiry);

    // All async functions return the status of queueing the async call,
    // not the call’s result.
    ASSERT(SEC_E_OK == Status);

    // At this point, the call can be pending or complete.
    // If complete, the result or error is returned.
    // For this example, we assume if it finished, it finished with SEC_E_OK.
    Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_I_ASYNC_CALL_PENDING == Status ||
           SEC_E_OK == Status);

    // Execution will continue in the callback upon completion
}

```

## <a name="see-also"></a><span data-ttu-id="2b741-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b741-154">See Also</span></span>

[<span data-ttu-id="2b741-155">en-tête SSPI. h</span><span class="sxs-lookup"><span data-stu-id="2b741-155">sspi.h header</span></span>](/windows/win32/api/sspi/)

[<span data-ttu-id="2b741-156">Fonctions SSPI</span><span class="sxs-lookup"><span data-stu-id="2b741-156">SSPI functions</span></span>](/windows/win32/api/sspi/#functions)

[<span data-ttu-id="2b741-157">Structures SSPI</span><span class="sxs-lookup"><span data-stu-id="2b741-157">SSPI structures</span></span>](/windows/win32/api/sspi/#structures)


