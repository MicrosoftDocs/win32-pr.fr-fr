---
description: Les applications WMI écrites en C++ peuvent effectuer des appels asynchrones à l’aide de nombreuses méthodes de l’interface COM IWbemServices.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Exécution d’un appel asynchrone avec C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522438"
---
# <a name="making-an-asynchronous-call-with-c"></a><span data-ttu-id="33991-103">Exécution d’un appel asynchrone avec C++</span><span class="sxs-lookup"><span data-stu-id="33991-103">Making an Asynchronous Call with C++</span></span>

<span data-ttu-id="33991-104">Les applications WMI écrites en C++ peuvent effectuer des appels asynchrones à l’aide de nombreuses méthodes de l’interface com [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="33991-104">WMI applications written in C++ can make asynchronous calls by using many of the methods of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) COM interface.</span></span> <span data-ttu-id="33991-105">Toutefois, la procédure recommandée pour appeler une [*méthode WMI*](gloss-w.md) ou un [*fournisseur*](gloss-p.md) consiste à utiliser des appels semi-synchrones, car les appels semi-synchrones sont plus sûrs que les appels asynchrones.</span><span class="sxs-lookup"><span data-stu-id="33991-105">However, the recommended procedure for calling a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) is by using semisynchronous calls because semisynchronous calls are more secure than asynchronous calls.</span></span> <span data-ttu-id="33991-106">Pour plus d’informations, consultez [création d’un appel semi-synchrone avec C++](making-a-semisynchronous-call-with-c--.md) et [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="33991-106">For more information, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="33991-107">La procédure suivante décrit comment effectuer un appel asynchrone à l’aide du récepteur dans votre processus.</span><span class="sxs-lookup"><span data-stu-id="33991-107">The following procedure describes how to make an asynchronous call by using the sink in your process.</span></span>

<span data-ttu-id="33991-108">**Pour effectuer un appel asynchrone à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="33991-108">**To make an asynchronous call using C++**</span></span>

1.  <span data-ttu-id="33991-109">Implémentez l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="33991-109">Implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="33991-110">Toutes les applications qui effectuent des appels asynchrones doivent implémenter [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="33991-110">All applications that make asynchronous calls must implement [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="33991-111">Les consommateurs d’événements temporaires implémentent également **IWbemObjectSink** pour recevoir des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="33991-111">Temporary event consumers also implement **IWbemObjectSink** to receive notification of events.</span></span>

2.  <span data-ttu-id="33991-112">Connectez-vous à l’espace de noms WMI cible.</span><span class="sxs-lookup"><span data-stu-id="33991-112">Log on to the target WMI namespace.</span></span>

    <span data-ttu-id="33991-113">Les applications doivent toujours appeler la fonction COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) lors de la phase d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="33991-113">Applications always have to call the COM function [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) during the initialization phase.</span></span> <span data-ttu-id="33991-114">Si ce n’est pas le cas avant d’effectuer un appel asynchrone, WMI libère le récepteur d’application sans terminer l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="33991-114">If they do not do so before making an asynchronous call, WMI releases the application sink without completing the asynchronous call.</span></span> <span data-ttu-id="33991-115">Pour plus d’informations, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="33991-115">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

3.  <span data-ttu-id="33991-116">Définissez la sécurité de votre récepteur.</span><span class="sxs-lookup"><span data-stu-id="33991-116">Set the security for your sink.</span></span>

    <span data-ttu-id="33991-117">Les appels asynchrones créent un grand nombre de problèmes de sécurité que vous devrez peut-être gérer, par exemple, en autorisant l’accès WMI à votre application.</span><span class="sxs-lookup"><span data-stu-id="33991-117">Asynchronous calls create a variety of security issues that you may have to deal with, for example, allowing WMI access to your application.</span></span> <span data-ttu-id="33991-118">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="33991-118">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

4.  <span data-ttu-id="33991-119">Effectuez l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="33991-119">Make the asynchronous call.</span></span>

    <span data-ttu-id="33991-120">La méthode est retournée immédiatement avec l’absence de code de réussite des **\_ \_ \_ Erreurs WBEM** .</span><span class="sxs-lookup"><span data-stu-id="33991-120">The method returns immediately with the **WBEM\_S\_NO\_ERROR** success code.</span></span> <span data-ttu-id="33991-121">L’application peut effectuer d’autres tâches en attendant que l’opération se termine.</span><span class="sxs-lookup"><span data-stu-id="33991-121">The application can proceed with other tasks while waiting for the operation to complete.</span></span> <span data-ttu-id="33991-122">WMI renvoie à l’application en appelant des méthodes dans l’implémentation [**IWbemObjectSink**](iwbemobjectsink.md) de votre application.</span><span class="sxs-lookup"><span data-stu-id="33991-122">WMI reports back to the application by calling methods in the [**IWbemObjectSink**](iwbemobjectsink.md) implementation of your application.</span></span>

5.  <span data-ttu-id="33991-123">Si nécessaire, vérifiez régulièrement votre mise en œuvre des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="33991-123">If necessary, check your implementation periodically for updates.</span></span>

    <span data-ttu-id="33991-124">Les applications peuvent recevoir une notification d’état intermédiaire en définissant le paramètre *lFlags* dans l’appel asynchrone de l’état d’envoi de l' **\_ indicateur \_ \_ WBEM**.</span><span class="sxs-lookup"><span data-stu-id="33991-124">Applications can receive notification of intermediate status by setting the *lFlags* parameter in the asynchronous call to **WBEM\_FLAG\_SEND\_STATUS**.</span></span> <span data-ttu-id="33991-125">WMI signale l’état de votre appel en définissant le paramètre *lFlags* de [**IWbemObjectSink**](iwbemobjectsink.md) sur **WBEM \_ Status \_ Progress**.</span><span class="sxs-lookup"><span data-stu-id="33991-125">WMI reports the status of your call by setting the *lFlags* parameter of [**IWbemObjectSink**](iwbemobjectsink.md) to **WBEM\_STATUS\_PROGRESS**.</span></span>

6.  <span data-ttu-id="33991-126">Si nécessaire, vous pouvez annuler l’appel avant que WMI termine le traitement en appelant la méthode [**IWbemServices :: CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .</span><span class="sxs-lookup"><span data-stu-id="33991-126">If necessary, you can cancel the call before WMI finishes processing by calling the [**IWbemServices::CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method.</span></span>

    <span data-ttu-id="33991-127">La méthode [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) annule le traitement asynchrone en libérant immédiatement le pointeur vers l’interface [**IWbemObjectSink**](iwbemobjectsink.md) et garantit que le pointeur est libéré avant que **CancelAsyncCall** retourne.</span><span class="sxs-lookup"><span data-stu-id="33991-127">The [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method cancels asynchronous processing by immediately releasing the pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface and guarantees that the pointer is released before **CancelAsyncCall** returns.</span></span>

    <span data-ttu-id="33991-128">Si vous utilisez un objet wrapper qui implémente l’interface **IUnsecured** pour héberger des [**IWbemObjectSink**](iwbemobjectsink.md), vous risquez de rencontrer des complications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="33991-128">If you are using a wrapper object implementing the **IUnsecured** interface to host [**IWbemObjectSink**](iwbemobjectsink.md), you may find some additional complications.</span></span> <span data-ttu-id="33991-129">Étant donné que l’application doit passer le même pointeur à [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) qui a été passé dans l’appel asynchrone d’origine, l’application doit conserver l’objet de wrapper jusqu’à ce qu’il soit clair que l’annulation n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="33991-129">Because the application must pass the same pointer to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) that was passed in the original asynchronous call, the application must hold on to the wrapper object until it becomes clear that cancellation is not required.</span></span> <span data-ttu-id="33991-130">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="33991-130">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

7.  <span data-ttu-id="33991-131">Lorsque vous avez terminé, nettoyez les pointeurs et arrêtez l’application.</span><span class="sxs-lookup"><span data-stu-id="33991-131">When finished, clean up pointers and shut down the application.</span></span>

    <span data-ttu-id="33991-132">WMI fournit l’appel d’état final par le biais de la méthode [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) .</span><span class="sxs-lookup"><span data-stu-id="33991-132">WMI provides the final status call through the [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="33991-133">Après l’envoi de la dernière mise à jour d’État, WMI libère le récepteur d’objets en appelant la méthode **Release** pour la classe qui implémente l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="33991-133">After sending the final status update, WMI releases the object sink by calling the **Release** method for the class that implements the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span> <span data-ttu-id="33991-134">Dans l’exemple précédent, il s’agit de la méthode **QuerySink :: Release** .</span><span class="sxs-lookup"><span data-stu-id="33991-134">In the previous example, this is the **QuerySink::Release** method.</span></span> <span data-ttu-id="33991-135">Si vous souhaitez contrôler la durée de vie de l’objet récepteur, vous pouvez implémenter le récepteur avec un nombre de références initial de un (1).</span><span class="sxs-lookup"><span data-stu-id="33991-135">If you want to have control over the lifetime of the sink object, you can implement the sink with an initial reference count of one (1).</span></span>

     

    <span data-ttu-id="33991-136">Si une application cliente passe la même interface de récepteur dans deux appels asynchrones différents qui se chevauchent, WMI ne garantit pas l’ordre du rappel.</span><span class="sxs-lookup"><span data-stu-id="33991-136">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="33991-137">Une application cliente qui effectue des appels asynchrones qui se chevauchent doit passer différents objets récepteur ou sérialiser les appels.</span><span class="sxs-lookup"><span data-stu-id="33991-137">A client application making overlapping asynchronous calls should either pass different sink objects or serialize the calls.</span></span>

<span data-ttu-id="33991-138">L’exemple suivant requiert la référence et les \# instructions include suivantes.</span><span class="sxs-lookup"><span data-stu-id="33991-138">The following example requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



<span data-ttu-id="33991-139">L’exemple suivant décrit comment créer une requête asynchrone à l’aide de la méthode [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) , mais ne crée pas de paramètres de sécurité ou ne libère pas l’objet [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="33991-139">The following example describes how to make an asynchronous query using the [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, but does not create security settings or release the [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span> <span data-ttu-id="33991-140">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="33991-140">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> <span data-ttu-id="33991-141">Le code ci-dessus ne se compile pas sans erreur, car la classe **QuerySink** n’a pas été définie.</span><span class="sxs-lookup"><span data-stu-id="33991-141">The code above does not compile without error because the **QuerySink** class has not been defined.</span></span> <span data-ttu-id="33991-142">Pour plus d’informations sur **QuerySink**, consultez [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="33991-142">For more information about **QuerySink**, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="33991-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33991-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33991-144">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="33991-144">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
