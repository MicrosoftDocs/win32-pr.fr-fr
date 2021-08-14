---
title: Contextes asynchrones
description: Vue d’ensemble des contextes asynchrones et de l’en-tête SSPI asynchrone.
ms.topic: article
ms.keywords: SSPI, Asynchronous Contexts, async contexts, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e83dbab8c20dd9f9cfe13ec579db304aabd491cba92ab0cd6a9c8afcf4e4af8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917228"
---
# <a name="asynchronous-contexts"></a>Contextes asynchrones

Les contextes de sécurité SSPI asynchrones permettent aux appelants de continuer sans bloquer et recevoir des notifications une fois l’appel terminé. Les contextes asynchrones sont actuellement pris en charge uniquement pour les serveurs et les clients TLS en mode noyau. Les fonctions SSPI asynchrones suivantes fonctionnent sur les contextes de sécurité asynchrones :

## <a name="async-context-management-types"></a>Types de gestion de contexte Async

| Nom d’objet | Description |
|-------------|--------------|
| [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | Rappel utilisé pour notifier l’achèvement d’un appel SSPI asynchrone. |


## <a name="async-context-management-functions"></a>Fonctions de gestion de contexte Async

| Nom de l’API | Description |
|-------------|--------------|
| [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | Crée une instance de SspiAsyncContext qui est utilisée pour effectuer le suivi de l’appel asynchrone. |
| [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | Marque un contexte Async pour la réutilisation. |
| [SspiSetAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | Inscrit un rappel qui est notifié de la fin de l’appel asynchrone. |
| [SspiAsyncContextRequiresNotify](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | Détermine si un contexte asynchrone donné requiert une notification à la fin de l’appel. |
| [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | Obtient l’état actuel d’un appel asynchrone associé au contexte fourni.  |
| [SspiFreeAsyncContext](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | Libère un contexte créé dans l’appel à la fonction SspiCreateAsyncContext. |

## <a name="async-sspi-functions"></a>Fonctions SSPI Async

Les fonctions suivantes acceptent un contexte asynchrone en plus de tous les mêmes paramètres que leur équivalent synchrone.

| Nom de l’API | Description |
|-------------|--------------|
| [SspiAcquireCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | Acquiert de manière asynchrone un handle pour les informations d’identification préexistantes d’un principal de sécurité. |
| [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | Permet au composant serveur d’une application de transport d’établir de façon asynchrone un contexte de sécurité entre le serveur et un client distant. |
| [SspiInitializeSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | Initialise un contexte de sécurité Async. |
| [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | Supprime les structures de données locales associées au contexte de sécurité spécifié initié par un appel précédent à la fonction SspiInitializeSecurityContextAsync ou à la fonction SspiAcceptSecurityContextAsync. |
| [SspiFreeCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | Libère un handle d’informations d’identification. |

## <a name="api-sample"></a>Exemple d’API

Un workflow d’appel classique fonctionne comme suit :
1) Créer un contexte SspiAsyncContext pour suivre l’appel à l’aide de [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)
2) Inscrire un [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) pour le contexte
3) Effectuer l’appel asynchrone à l’aide de [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)
4) Sur le rappel, récupérez le résultat à l’aide de [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)
5) Supprimez SspiAsyncContext à l’aide de [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync). Si vous réutilisez le contexte avec [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), revenez à l’étape 2.

L’exemple ci-dessous illustre un appel de SspiAcceptSecurityContextAsync. L’exemple attend la fin de l’appel et récupère le résultat.

Dans une négociation SSPI complète, SspiAcceptSecurityContextAsync et SspiInitializeSecurityContextAsync sont appelées plusieurs fois jusqu’à ce que SEC_E_OK soit retourné. SspiReinitAsyncContext a été fourni pour une facilité d’utilisation et pour faciliter les performances dans ce cas.

Les assertions sont utilisées pour mettre en évidence ce que nous attendons dans le cas d’une réussite.

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

## <a name="see-also"></a>Voir aussi

[en-tête SSPI. h](/windows/win32/api/sspi/)

[Fonctions SSPI](/windows/win32/api/sspi/#functions)

[Structures SSPI](/windows/win32/api/sspi/#structures)


