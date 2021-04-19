---
description: L’interface IWbemObjectSink crée une interface de récepteur qui peut recevoir tous les types de notifications dans le modèle de programmation WMI.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Interface IWbemObjectSink (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527826"
---
# <a name="iwbemobjectsink-interface"></a><span data-ttu-id="0b6e2-103">Interface IWbemObjectSink</span><span class="sxs-lookup"><span data-stu-id="0b6e2-103">IWbemObjectSink interface</span></span>

<span data-ttu-id="0b6e2-104">L’interface **IWbemObjectSink** crée une interface de récepteur qui peut recevoir tous les types de notifications dans le modèle de programmation WMI.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-104">The **IWbemObjectSink** interface creates a sink interface that can receive all types of notifications within the WMI programming model.</span></span> <span data-ttu-id="0b6e2-105">Les clients doivent implémenter cette interface pour recevoir les résultats des [méthodes asynchrones](making-an-asynchronous-call-with-c--.md) de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)et des types spécifiques de notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-105">Clients must implement this interface to receive both the results of the [asynchronous methods](making-an-asynchronous-call-with-c--.md) of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), and specific types of event notifications.</span></span> <span data-ttu-id="0b6e2-106">Les fournisseurs utilisent, mais n’implémentent pas cette interface pour fournir des événements et des objets à WMI.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-106">Providers use, but do not implement this interface to provide events and objects to WMI.</span></span>

<span data-ttu-id="0b6e2-107">En règle générale, les fournisseurs appellent une implémentation qui leur est fournie par WMI.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-107">Typically, providers call an implementation provided to them by WMI.</span></span> <span data-ttu-id="0b6e2-108">Dans ce cas, Call [**indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) pour fournir des objets au service WMI.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-108">In these cases, call [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to provide objects to the WMI service.</span></span> <span data-ttu-id="0b6e2-109">Après cela, appelez [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) pour indiquer la fin de la séquence de notification.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-109">After that, call [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to indicate the end of the notification sequence.</span></span> <span data-ttu-id="0b6e2-110">Vous pouvez également appeler **SetStatus** pour indiquer des erreurs lorsque le récepteur n’a aucun objet.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-110">You can also call **SetStatus** to indicate errors when the sink does not have any objects.</span></span>

<span data-ttu-id="0b6e2-111">Lors de la programmation de clients asynchrones de WMI, l’utilisateur fournit l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-111">When programming asynchronous clients of WMI, the user provides the implementation.</span></span> <span data-ttu-id="0b6e2-112">WMI appelle les méthodes pour remettre des objets et définir l’état du résultat.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-112">WMI calls the methods to deliver objects and set the status of the result.</span></span>

> [!Note]  
> <span data-ttu-id="0b6e2-113">Si une application cliente passe la même interface de récepteur dans deux appels asynchrones différents qui se chevauchent, WMI ne garantit pas l’ordre du rappel.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-113">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="0b6e2-114">Les applications clientes qui effectuent des appels asynchrones qui se chevauchent doivent passer différents objets récepteur ou sérialiser leurs appels.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-114">Client applications that make overlapping asynchronous calls should either pass different sink objects, or serialize their calls.</span></span>

 

> [!Note]  
> <span data-ttu-id="0b6e2-115">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser la fonction semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-115">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="0b6e2-116">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0b6e2-116">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="0b6e2-117">Membres</span><span class="sxs-lookup"><span data-stu-id="0b6e2-117">Members</span></span>

<span data-ttu-id="0b6e2-118">L’interface **IWbemObjectSink** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0b6e2-118">The **IWbemObjectSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="0b6e2-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0b6e2-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0b6e2-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0b6e2-120">Methods</span></span>

<span data-ttu-id="0b6e2-121">L’interface **IWbemObjectSink** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-121">The **IWbemObjectSink** interface has these methods.</span></span>



| <span data-ttu-id="0b6e2-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="0b6e2-122">Method</span></span>                                         | <span data-ttu-id="0b6e2-123">Description</span><span class="sxs-lookup"><span data-stu-id="0b6e2-123">Description</span></span>                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b6e2-124">**Indiquer**</span><span class="sxs-lookup"><span data-stu-id="0b6e2-124">**Indicate**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | <span data-ttu-id="0b6e2-125">Reçoit des objets de notification.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-125">Receives notification objects.</span></span><br/>                                                                               |
| [<span data-ttu-id="0b6e2-126">**SetStatus**</span><span class="sxs-lookup"><span data-stu-id="0b6e2-126">**SetStatus**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | <span data-ttu-id="0b6e2-127">Appelée par les sources pour indiquer la fin d’une séquence de notification, ou pour envoyer d’autres codes d’État au récepteur.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-127">Called by sources to indicate the end of a notification sequence, or to send other status codes to the sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b6e2-128">Notes</span><span class="sxs-lookup"><span data-stu-id="0b6e2-128">Remarks</span></span>

<span data-ttu-id="0b6e2-129">Lors de l’implémentation d’un récepteur d’abonnement aux événements (**IWbemObjectSink** ou [**IWbemEventSink**](iwbemeventsink.md)), n’appelez pas WMI à partir des méthodes d' [**indication**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) ou [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) sur l’objet récepteur.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-129">When implementing an event subscription sink (**IWbemObjectSink** or [**IWbemEventSink**](iwbemeventsink.md)), do not call into WMI from within the [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) or [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) methods on the sink object.</span></span> <span data-ttu-id="0b6e2-130">Par exemple, l’appel de [**IWbemServices :: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) pour annuler le récepteur à partir d’une implémentation de [**indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) qu’il peut interférer avec l’État WMI.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-130">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) can interfere with the WMI state.</span></span> <span data-ttu-id="0b6e2-131">Pour annuler un abonnement à un événement, définissez un indicateur et appelez **IWbemServices :: CancelAsyncCall** à partir d’un autre thread ou objet.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-131">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="0b6e2-132">Pour les implémentations qui ne sont pas liées à un récepteur d’événements, telles que les récupérations d’objets, d’enum et de requêtes, vous pouvez rappeler dans WMI.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-132">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="0b6e2-133">Les implémentations de récepteur doivent traiter la notification d’événement dans un délai de 100 ms car le thread WMI qui remet la notification d’événement ne peut pas effectuer d’autres tâches tant que le traitement de l’objet récepteur n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-133">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="0b6e2-134">Si la notification nécessite une grande quantité de traitement, le récepteur peut utiliser une file d’attente interne pour qu’un autre thread gère le traitement.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-134">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="examples"></a><span data-ttu-id="0b6e2-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="0b6e2-135">Examples</span></span>

<span data-ttu-id="0b6e2-136">L’exemple de code suivant est une implémentation simple d’un récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="0b6e2-136">The following code example is a simple implementation of an object sink.</span></span> <span data-ttu-id="0b6e2-137">Cet exemple peut être utilisé avec [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) ou [**IWbemServices :: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) pour recevoir les instances retournées :</span><span class="sxs-lookup"><span data-stu-id="0b6e2-137">This sample can be used with [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) to receive the returned instances:</span></span>


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a><span data-ttu-id="0b6e2-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b6e2-138">Requirements</span></span>



| <span data-ttu-id="0b6e2-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b6e2-139">Requirement</span></span> | <span data-ttu-id="0b6e2-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b6e2-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6e2-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b6e2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0b6e2-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b6e2-142">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="0b6e2-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b6e2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0b6e2-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b6e2-144">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="0b6e2-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b6e2-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b6e2-146"><dt>Wbemcli. h (inclure Wbemidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b6e2-146"><dt>Wbemcli.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="0b6e2-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b6e2-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b6e2-148"><dt>Wbemuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b6e2-148"><dt>Wbemuuid.lib</dt></span></span> </dl>                  |
| <span data-ttu-id="0b6e2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="0b6e2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b6e2-150"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b6e2-150"><dt>Fastprox.dll</dt></span></span> </dl>                  |



## <a name="see-also"></a><span data-ttu-id="0b6e2-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b6e2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6e2-152">API COM pour WMI</span><span class="sxs-lookup"><span data-stu-id="0b6e2-152">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="0b6e2-153">Exécution d’un appel asynchrone avec C++</span><span class="sxs-lookup"><span data-stu-id="0b6e2-153">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[<span data-ttu-id="0b6e2-154">Définition de la sécurité sur un appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="0b6e2-154">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="0b6e2-155">Réception d’événements pendant la durée de votre application</span><span class="sxs-lookup"><span data-stu-id="0b6e2-155">Receiving Events for the Duration of your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




