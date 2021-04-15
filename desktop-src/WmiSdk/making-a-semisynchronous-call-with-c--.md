---
description: 'Les appels semi-synchrones sont les moyens recommandés pour appeler des méthodes WMI, telles que IWbemServices :: ExecMethod et des méthodes de fournisseur, telles que la méthode CHKDSK de la \_ classe disque logique Win32.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Appel semi-synchrone avec C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529614"
---
# <a name="making-a-semisynchronous-call-with-c"></a><span data-ttu-id="8784d-103">Appel semi-synchrone avec C++</span><span class="sxs-lookup"><span data-stu-id="8784d-103">Making a Semisynchronous Call with C++</span></span>

<span data-ttu-id="8784d-104">Les appels semi-synchrones sont les moyens recommandés pour appeler des méthodes WMI, telles que [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) et des méthodes de fournisseur, telles que la [**méthode CHKDSK de la \_ classe disque logique Win32**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="8784d-104">Semisynchronous calls are the recommended means to call WMI methods, such as [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) and provider methods, such as the [**Chkdsk Method of the Win32\_LogicalDisk Class**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span></span>

<span data-ttu-id="8784d-105">L’un des inconvénients du traitement synchrone est que le thread appelant est bloqué jusqu’à ce que l’appel se termine.</span><span class="sxs-lookup"><span data-stu-id="8784d-105">One disadvantage of synchronous processing is that the caller thread is blocked until the call completes.</span></span> <span data-ttu-id="8784d-106">Le blocage peut entraîner un retard dans le temps de traitement.</span><span class="sxs-lookup"><span data-stu-id="8784d-106">The blockage can cause a delay in processing time.</span></span> <span data-ttu-id="8784d-107">En revanche, un appel asynchrone doit implémenter [**SWbemSink**](swbemsink.md) dans le script.</span><span class="sxs-lookup"><span data-stu-id="8784d-107">In contrast, an asynchronous call must implement [**SWbemSink**](swbemsink.md) in script.</span></span> <span data-ttu-id="8784d-108">En C++, le code asynchrone doit implémenter l’interface [**IWbemObjectSink**](iwbemobjectsink.md) , utiliser plusieurs threads et contrôler le flux d’informations vers l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8784d-108">In C++, asynchronous code must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface, use multiple threads, and control the flow of information back to the caller.</span></span> <span data-ttu-id="8784d-109">Les jeux de résultats volumineux des requêtes, par exemple, peuvent prendre beaucoup de temps pour remettre et obliger l’appelant à consacrer des ressources système significatives pour gérer la remise.</span><span class="sxs-lookup"><span data-stu-id="8784d-109">Large result sets from queries, for example, can take a considerable amount of time to deliver and forces the caller to spend significant system resources to handle the delivery.</span></span>

<span data-ttu-id="8784d-110">Le traitement semi-synchrone résout les problèmes de blocage de thread et de remise non contrôlée en interrogeant un objet d’état spécial qui implémente l’interface [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) .</span><span class="sxs-lookup"><span data-stu-id="8784d-110">Semisynchronous processing solves both the thread blockage and uncontrolled delivery problems by polling a special status object that implements the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) interface.</span></span> <span data-ttu-id="8784d-111">Grâce à **IWbemCallResult**, vous pouvez améliorer la vitesse et l’efficacité des requêtes, des énumérations et des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="8784d-111">Through **IWbemCallResult**, you can improve the speed and efficiency of queries, enumerations, and event notifications.</span></span>

<span data-ttu-id="8784d-112">La procédure suivante décrit comment effectuer un appel semi-synchrone avec l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="8784d-112">The following procedure describes how to make a semisynchronous call with the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="8784d-113">**Pour effectuer un appel semi-synchrone avec l’interface IWbemServices**</span><span class="sxs-lookup"><span data-stu-id="8784d-113">**To make a semisynchronous call with the IWbemServices interface**</span></span>

1.  <span data-ttu-id="8784d-114">Transformez votre appel en mode normal, mais avec l' **\_ indicateur WBEM \_ retourner \_ immédiatement** l’indicateur défini dans le paramètre *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="8784d-114">Make your call as normal, but with the **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag set in the *IFlags* parameter.</span></span>

    <span data-ttu-id="8784d-115">Vous pouvez combiner **\_ immédiatement l’indicateur WBEM \_ Return \_** avec d’autres indicateurs qui sont valides pour la méthode spécifique.</span><span class="sxs-lookup"><span data-stu-id="8784d-115">You can combine **WBEM\_FLAG\_RETURN\_IMMEDIATELY** with other flags that are valid for the specific method.</span></span> <span data-ttu-id="8784d-116">Par exemple, utilisez l' **indicateur \_ WBEM \_ Forward \_ only uniquement** pour tous les appels qui retournent des énumérateurs.</span><span class="sxs-lookup"><span data-stu-id="8784d-116">For example, use the **WBEM\_FLAG\_FORWARD\_ONLY** flag for all calls that return enumerators.</span></span> <span data-ttu-id="8784d-117">La définition de ces indicateurs en combinaison permet de gagner du temps et de l’espace et d’améliorer la réactivité.</span><span class="sxs-lookup"><span data-stu-id="8784d-117">Setting these flags in combination saves time and space, and improves responsiveness.</span></span>

2.  <span data-ttu-id="8784d-118">Interrogez vos résultats.</span><span class="sxs-lookup"><span data-stu-id="8784d-118">Poll for your results.</span></span>

    <span data-ttu-id="8784d-119">Si vous appelez une méthode qui retourne un énumérateur, tel que [**IWbemServices :: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) ou [**IWbemServices :: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), vous pouvez interroger les énumérateurs avec les méthodes [**IEnumWbemClassObject :: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) ou [**IEnumWbemClassObject :: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) .</span><span class="sxs-lookup"><span data-stu-id="8784d-119">If you call a method that returns an enumerator, such as [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) or [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), you can poll the enumerators with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) methods.</span></span> <span data-ttu-id="8784d-120">L’appel de **IEnumWbemClassObject :: NextAsync** est non bloquant et est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="8784d-120">The **IEnumWbemClassObject::NextAsync** call is nonblocking and returns immediately.</span></span> <span data-ttu-id="8784d-121">En arrière-plan, WMI commence à remettre le nombre demandé d’objets en appelant [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="8784d-121">In the background, WMI begins to deliver the requested number of objects by calling [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span> <span data-ttu-id="8784d-122">WMI s’arrête et attend un autre appel **NextAsync** .</span><span class="sxs-lookup"><span data-stu-id="8784d-122">WMI then stops and waits for another **NextAsync** call.</span></span>

    <span data-ttu-id="8784d-123">Si vous appelez une méthode qui ne retourne pas d’énumérateur, telle que [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), vous devez définir le paramètre *ppCallResult* sur un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="8784d-123">If you call a method that does not return an enumerator, such as [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), you must set the *ppCallResult* parameter to a valid pointer.</span></span> <span data-ttu-id="8784d-124">Utilisez [**IWbemCallResult :: GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) sur le pointeur retourné pour récupérer les **\_ S non \_ - \_ erreur WBEM**.</span><span class="sxs-lookup"><span data-stu-id="8784d-124">Use the [**IWbemCallResult::GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) on the returned pointer to retrieve **WBEM\_S\_NO\_ERROR**.</span></span>

3.  <span data-ttu-id="8784d-125">Terminez votre appel.</span><span class="sxs-lookup"><span data-stu-id="8784d-125">Finish your call.</span></span>

    <span data-ttu-id="8784d-126">Pour un appel qui retourne un énumérateur, WMI appelle [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) pour signaler la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="8784d-126">For a call that returns an enumerator, WMI calls [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to report the completion of the operation.</span></span> <span data-ttu-id="8784d-127">Si vous n’avez pas besoin de la totalité du résultat, Libérez l’énumérateur en appelant la méthode [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="8784d-127">If you do not need the entire result, release the enumerator by calling the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="8784d-128">L’appel des résultats de la **mise** en service dans WMI annule la remise de tous les objets restants.</span><span class="sxs-lookup"><span data-stu-id="8784d-128">Calling **Release** results in WMI canceling the delivery of all objects that remain.</span></span>

    <span data-ttu-id="8784d-129">Pour un appel qui n’utilise pas d’énumérateur, récupérez l’objet [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) via le paramètre *plStatus* de votre méthode.</span><span class="sxs-lookup"><span data-stu-id="8784d-129">For a call that does not use an enumerator, retrieve the [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) object through the *plStatus* parameter of your method.</span></span>

<span data-ttu-id="8784d-130">L’exemple de code C++ dans cette rubrique requiert que les \# instructions include suivantes soient compilées correctement.</span><span class="sxs-lookup"><span data-stu-id="8784d-130">The C++ code example in this topic requires the following \#include statements to compile correctly.</span></span>


```C++
#include <comdef.h>
#include <wbemidl.h>
```



<span data-ttu-id="8784d-131">L’exemple de code suivant montre comment effectuer un appel semi-synchrone à [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="8784d-131">The following code example shows how to make a semisynchronous call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a><span data-ttu-id="8784d-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8784d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8784d-133">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="8784d-133">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
