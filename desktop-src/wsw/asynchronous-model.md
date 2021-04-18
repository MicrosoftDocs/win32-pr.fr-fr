---
title: Modèle asynchrone
description: La plupart des opérations dans l’API des services Web Windows peuvent être effectuées de façon synchrone ou asynchrone.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Services Web de modèle asynchrone pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509392"
---
# <a name="asynchronous-model"></a><span data-ttu-id="b36a6-106">Modèle asynchrone</span><span class="sxs-lookup"><span data-stu-id="b36a6-106">Asynchronous Model</span></span>

<span data-ttu-id="b36a6-107">La plupart des opérations dans l’API des services Web Windows peuvent être effectuées de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b36a6-107">Most operations in Windows Web Services API can be performed synchronously or asynchronously.</span></span> <span data-ttu-id="b36a6-108">Pour appeler une fonction de façon synchrone, transmettez une valeur null pour la structure de [**\_ \_ contexte WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="b36a6-108">To call a function synchronously, pass a null value for the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="b36a6-109">Pour spécifier qu’une fonction peut être exécutée de façon asynchrone, transmettez un **\_ \_ contexte WS Async** non null à la fonction.</span><span class="sxs-lookup"><span data-stu-id="b36a6-109">To specify that a function may be performed asynchronously, pass a non-null **WS\_ASYNC\_CONTEXT** to the function.</span></span>

<span data-ttu-id="b36a6-110">Lorsqu’elle est appelée de façon asynchrone, une fonction peut néanmoins se terminer de façon synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b36a6-110">When called asynchronously, a function can nevertheless complete synchronously or asynchronously.</span></span> <span data-ttu-id="b36a6-111">Si la fonction se termine de façon synchrone, elle retourne une valeur qui indique le succès ou l’erreur final, et cette valeur est toujours autre chose que **WS \_ S \_ Async** (voir les [valeurs de retour des services Web Windows](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="b36a6-111">If the function completes synchronously, it returns a value that indicates the final success or error, and this value is always something other than **WS\_S\_ASYNC** (See [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span> <span data-ttu-id="b36a6-112">Une valeur de retour de **WS \_ S \_ Async**, toutefois, indique que la fonction se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b36a6-112">A return value of **WS\_S\_ASYNC**, however, indicates that the function will complete asynchronously.</span></span> <span data-ttu-id="b36a6-113">Lorsque la fonction se termine de façon asynchrone, un rappel est appelé pour signaler la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b36a6-113">When the function completes asynchronously, a callback is invoked to signal completion of the operation.</span></span> <span data-ttu-id="b36a6-114">Ce rappel indique la valeur finale de réussite ou d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b36a6-114">This callback indicates the final success or error value.</span></span> <span data-ttu-id="b36a6-115">Le rappel n’est pas appelé si l’opération se termine de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="b36a6-115">The callback is not called if the operation completes synchronously.</span></span>

<span data-ttu-id="b36a6-116">Pour créer un contexte asynchrone, initialisez les champs **callback** et **callbackState** de la structure de [**\_ \_ contexte WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="b36a6-116">To create an asynchronous context, initialize the **callback** and **callbackState** fields of the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="b36a6-117">Le champ **callbackState** est utilisé pour spécifier un pointeur vers les données définies par l’utilisateur qui sont passées à la fonction de [**\_ \_ rappel WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .</span><span class="sxs-lookup"><span data-stu-id="b36a6-117">The **callbackState** field is used to specify a pointer to user-defined data which is passed to the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) function.</span></span>

<span data-ttu-id="b36a6-118">L’exemple suivant illustre l’appel d’une fonction de manière asynchrone en passant un pointeur vers une structure de [**\_ \_ contexte WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) qui contient le rappel et un pointeur vers les données d’État.</span><span class="sxs-lookup"><span data-stu-id="b36a6-118">The following example shows calling a function asynchronously by passing a pointer to a [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure that contains the callback and a pointer to the state data.</span></span>

``` syntax
HRESULT ExampleAsyncFunction(WS_ASYNC_CONTEXT* asyncContext);
void ExampleAsyncFunction()
{
    // Set up the WS_ASYNC_CONTEXT structure.
    MyState* myState = ...;  \\ Declare a pointer to user-defined data.
    WS_ASYNC_CONTEXT asyncContext;
    asyncContext.callback = MyCallback;  \\ Set the callback.
    asyncContext.callbackState = myState; \\ Set the pointer to the user-defined data.

    // Start the asynchronous operation
    HRESULT hr = SomeFunction(&asyncContext);

    if (hr == WS_S_ASYNC)
    {
        // The operation is completing asynchronously.  The callback is called 
        // when the operation is complete.
    }
    else
    {
        // The operation completed synchronously.  The callback is not called.
    }
}
void CALLBACK MyCallback(HRESULT hr, WS_CALLBACK_MODEL callbackModel, void* callbackState)
{
    MyState* myState = (MyState*)callbackState;

    // The operation completed asynchronously.
}
```

<span data-ttu-id="b36a6-119">La structure de [**\_ \_ contexte WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) est utilisée par la fonction asynchrone uniquement pendant la durée de l’appel de fonction (pas pendant la durée de l’opération asynchrone), afin que vous puissiez la déclarer en toute sécurité sur la pile.</span><span class="sxs-lookup"><span data-stu-id="b36a6-119">The [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure is used by the asynchronous function only for the duration of the function call (not for the duration of the asynchronous operation), so you can safely declare it on the stack.</span></span>

<span data-ttu-id="b36a6-120">Si d’autres paramètres, en plus de la structure de [**\_ \_ contexte WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) , sont passés à une fonction asynchrone en tant que pointeurs et que la fonction se termine de façon asynchrone, il incombe à l’appelant de conserver les valeurs vers lesquelles ces paramètres sont actifs (non libérés) jusqu’à ce que le rappel asynchrone soit appelé.</span><span class="sxs-lookup"><span data-stu-id="b36a6-120">If any other parameters, besides the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure, are passed to an asynchronous function as pointers and the function completes asynchronously, it is the responsibility of the caller to keep the values pointed to by these parameters alive (not freed) until the asynchronous callback is invoked.</span></span>

<span data-ttu-id="b36a6-121">Il existe des limitations sur les opérations qu’un rappel peut effectuer.</span><span class="sxs-lookup"><span data-stu-id="b36a6-121">There are limitations on what operations a callback may perform.</span></span> <span data-ttu-id="b36a6-122">Pour plus d’informations sur les opérations possibles, consultez le [**\_ \_ modèle de rappel WS**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span><span class="sxs-lookup"><span data-stu-id="b36a6-122">For more information on possible operations , see the [**WS\_CALLBACK\_MODEL**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span></span>

<span data-ttu-id="b36a6-123">Quand vous implémentez une fonction asynchrone, n’appelez pas le rappel sur le thread qui a appelé la fonction asynchrone avant que la fonction asynchrone soit retournée à l’appelant, ce qui interrompt le modèle asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b36a6-123">When you implement an asynchronous function, do not invoke the callback on the same thread that called the asynchronous function before the asynchronous function has returned to the caller, as this disrupts the asynchronous model.</span></span>

<span data-ttu-id="b36a6-124">Lors de l’implémentation d’une fonction qui doit exécuter une série d’opérations asynchrones, envisagez d’utiliser la fonction d’assistance [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) .</span><span class="sxs-lookup"><span data-stu-id="b36a6-124">When implementing a function that needs to execute a series of asynchronous operations, consider using the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) helper function.</span></span>

<span data-ttu-id="b36a6-125">L' [exemple de fonction asynchrone](asyncmodelexample.md) montre comment implémenter et utiliser des fonctions qui suivent le modèle asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b36a6-125">The [Asynchronous Function Example](asyncmodelexample.md) shows how to implement and consume functions that follow the asynchronous model.</span></span>

<span data-ttu-id="b36a6-126">Le démarrage d’une opération d’e/s asynchrone consomme des ressources système.</span><span class="sxs-lookup"><span data-stu-id="b36a6-126">Starting an asynchronous IO operation consumes system resources.</span></span> <span data-ttu-id="b36a6-127">Si un nombre suffisant d’opérations d’e/s est démarré, le système peut cesser de répondre.</span><span class="sxs-lookup"><span data-stu-id="b36a6-127">If enough IO operations are started, the system can become unresponsive.</span></span> <span data-ttu-id="b36a6-128">Pour éviter cela, une application doit limiter le nombre d’opérations asynchrones qu’elle démarre.</span><span class="sxs-lookup"><span data-stu-id="b36a6-128">To prevent this, an application needs to limit the number of asynchronous operations that it starts.</span></span>

<span data-ttu-id="b36a6-129">Le modèle asynchrone utilise les éléments d’API suivants.</span><span class="sxs-lookup"><span data-stu-id="b36a6-129">The asynchronous model uses the following API elements.</span></span>

| <span data-ttu-id="b36a6-130">Rappel</span><span class="sxs-lookup"><span data-stu-id="b36a6-130">Callback</span></span>                                         | <span data-ttu-id="b36a6-131">Description</span><span class="sxs-lookup"><span data-stu-id="b36a6-131">Description</span></span>                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b36a6-132">**\_rappel WS asynchrone \_**</span><span class="sxs-lookup"><span data-stu-id="b36a6-132">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | <span data-ttu-id="b36a6-133">Paramètre de fonction de rappel utilisé avec le modèle asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b36a6-133">The callback function parameter used with the asynchronous model.</span></span>                                                                     |
| [<span data-ttu-id="b36a6-134">**WS \_ Async, \_ fonction**</span><span class="sxs-lookup"><span data-stu-id="b36a6-134">**WS\_ASYNC\_FUNCTION**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | <span data-ttu-id="b36a6-135">Utilisé avec [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) pour spécifier la fonction suivante à appeler dans une série d’opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="b36a6-135">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |



 



| <span data-ttu-id="b36a6-136">Énumération</span><span class="sxs-lookup"><span data-stu-id="b36a6-136">Enumeration</span></span>                                      | <span data-ttu-id="b36a6-137">Description</span><span class="sxs-lookup"><span data-stu-id="b36a6-137">Description</span></span>                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b36a6-138">**\_modèle de rappel WS \_**</span><span class="sxs-lookup"><span data-stu-id="b36a6-138">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | <span data-ttu-id="b36a6-139">Spécifie le comportement de thread d’un rappel (par exemple, [**un \_ \_ rappel WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span><span class="sxs-lookup"><span data-stu-id="b36a6-139">Specifies the threading behavior of a callback (for example, a [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span></span> |



 



| <span data-ttu-id="b36a6-140">Fonction</span><span class="sxs-lookup"><span data-stu-id="b36a6-140">Function</span></span>                                 | <span data-ttu-id="b36a6-141">Description</span><span class="sxs-lookup"><span data-stu-id="b36a6-141">Description</span></span>                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b36a6-142">**WsAsyncExecute**</span><span class="sxs-lookup"><span data-stu-id="b36a6-142">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | <span data-ttu-id="b36a6-143">Appelle un rappel défini par l’utilisateur qui peut lancer une opération asynchrone et indiquer une fonction qui doit être appelée lorsque l’opération asynchrone est terminée.</span><span class="sxs-lookup"><span data-stu-id="b36a6-143">Invokes a user-defined callback which can initiate an asynchronous operation and indicate a function that should be called when the asynchronous operation has been completed.</span></span> |



 



| <span data-ttu-id="b36a6-144">Structure</span><span class="sxs-lookup"><span data-stu-id="b36a6-144">Structure</span></span>                                          | <span data-ttu-id="b36a6-145">Description</span><span class="sxs-lookup"><span data-stu-id="b36a6-145">Description</span></span>                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b36a6-146">**\_contexte WS Async \_**</span><span class="sxs-lookup"><span data-stu-id="b36a6-146">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | <span data-ttu-id="b36a6-147">Spécifie le rappel asynchrone et un pointeur vers les données définies par l’utilisateur, qui seront passées au rappel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b36a6-147">Specifies the asynchronous callback and a pointer to user-defined data, which will be passed to the asynchronous callback.</span></span>            |
| [<span data-ttu-id="b36a6-148">**fonctionnement de WS \_ Async \_**</span><span class="sxs-lookup"><span data-stu-id="b36a6-148">**WS\_ASYNC\_OPERATION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | <span data-ttu-id="b36a6-149">Utilisé avec [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) pour spécifier la fonction suivante à appeler dans une série d’opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="b36a6-149">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |
| [<span data-ttu-id="b36a6-150">**\_État WS Async \_**</span><span class="sxs-lookup"><span data-stu-id="b36a6-150">**WS\_ASYNC\_STATE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | <span data-ttu-id="b36a6-151">Utilisé par [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) pour gérer l’état d’une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b36a6-151">Used by [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to manage the state of an asynchronous operation.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="b36a6-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b36a6-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b36a6-153">Exemple de fonction asynchrone</span><span class="sxs-lookup"><span data-stu-id="b36a6-153">Asynchronous Function Example</span></span>](asyncmodelexample.md)
</dt> <dt>

[<span data-ttu-id="b36a6-154">**\_rappel WS asynchrone \_**</span><span class="sxs-lookup"><span data-stu-id="b36a6-154">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[<span data-ttu-id="b36a6-155">**\_contexte WS Async \_**</span><span class="sxs-lookup"><span data-stu-id="b36a6-155">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[<span data-ttu-id="b36a6-156">**\_modèle de rappel WS \_**</span><span class="sxs-lookup"><span data-stu-id="b36a6-156">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[<span data-ttu-id="b36a6-157">**WsAsyncExecute**</span><span class="sxs-lookup"><span data-stu-id="b36a6-157">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




