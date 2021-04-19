---
description: Windows Management Instrumentation (WMI) peut créer le récepteur pour recevoir des rappels asynchrones pour une application cliente dans un processus séparé.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Diminution de la sécurité d’un récepteur dans un processus distinct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521828"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a><span data-ttu-id="131b3-103">Diminution de la sécurité d’un récepteur dans un processus distinct</span><span class="sxs-lookup"><span data-stu-id="131b3-103">Lowering the Security for a Sink in a Separate Process</span></span>

<span data-ttu-id="131b3-104">Windows Management Instrumentation (WMI) peut créer le récepteur pour recevoir des rappels asynchrones pour une application cliente dans un processus séparé.</span><span class="sxs-lookup"><span data-stu-id="131b3-104">Windows Management Instrumentation (WMI) can create the sink to receive asynchronous callbacks for a client application in a separate process.</span></span> <span data-ttu-id="131b3-105">Le processus distinct est Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="131b3-105">The separate process is Unsecapp.exe.</span></span> <span data-ttu-id="131b3-106">Utilisez l’interface [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) .</span><span class="sxs-lookup"><span data-stu-id="131b3-106">Use the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface.</span></span> <span data-ttu-id="131b3-107">**IWbemUnsecuredApartment** vous permet de contrôler si Unsecapp.exe authentifie les rappels sur le récepteur.</span><span class="sxs-lookup"><span data-stu-id="131b3-107">**IWbemUnsecuredApartment** allows you to control whether Unsecapp.exe authenticates callbacks to the sink.</span></span> <span data-ttu-id="131b3-108">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="131b3-108">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="131b3-109">Vous pouvez ensuite réduire la sécurité sur ce processus et WMI peut accéder au récepteur sans restriction.</span><span class="sxs-lookup"><span data-stu-id="131b3-109">You can then lower the security on that process and WMI can access the sink without restriction.</span></span> <span data-ttu-id="131b3-110">Pour faciliter cette technique, WMI fournit le processus de Unsecapp.exe pour fonctionner en tant que processus distinct.</span><span class="sxs-lookup"><span data-stu-id="131b3-110">To assist with this technique WMI provides the Unsecapp.exe process to function as the separate process.</span></span> <span data-ttu-id="131b3-111">Vous pouvez héberger des Unsecapp.exe à l’aide d’un appel à l’interface [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) .</span><span class="sxs-lookup"><span data-stu-id="131b3-111">You can host Unsecapp.exe with a call to the [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface.</span></span>

<span data-ttu-id="131b3-112">L’interface [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) permet à une application cliente de créer un processus dédié distinct exécutant Unsecapp.exe pour héberger une implémentation [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="131b3-112">The [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface allows a client application to create a separate dedicated process running Unsecapp.exe for hosting a [**IWbemObjectSink**](iwbemobjectsink.md) implementation.</span></span> <span data-ttu-id="131b3-113">Le processus dédié peut appeler [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour accorder l’accès WMI au processus dédié sans compromettre la sécurité du processus principal.</span><span class="sxs-lookup"><span data-stu-id="131b3-113">The dedicated process can call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to grant WMI access to the dedicated process without compromising the security of the main process.</span></span> <span data-ttu-id="131b3-114">Après l’initialisation, le processus dédié agit comme un intermédiaire entre le processus principal et WMI.</span><span class="sxs-lookup"><span data-stu-id="131b3-114">After initialization, the dedicated process acts as an intermediary between the main process and WMI.</span></span>

<span data-ttu-id="131b3-115">La procédure suivante décrit comment effectuer un appel asynchrone avec [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span><span class="sxs-lookup"><span data-stu-id="131b3-115">The following procedure describes how to perform an asynchronous call with [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span></span>

<span data-ttu-id="131b3-116">**Pour effectuer un appel asynchrone avec IUnsecuredApartment**</span><span class="sxs-lookup"><span data-stu-id="131b3-116">**To perform an asynchronous call with IUnsecuredApartment**</span></span>

1.  <span data-ttu-id="131b3-117">Créez un processus dédié avec un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="131b3-117">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="131b3-118">L’exemple de code suivant appelle [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un processus dédié.</span><span class="sxs-lookup"><span data-stu-id="131b3-118">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="131b3-119">Instanciez l’objet récepteur.</span><span class="sxs-lookup"><span data-stu-id="131b3-119">Instantiate the sink object.</span></span>

    <span data-ttu-id="131b3-120">L’exemple de code suivant crée un nouvel objet récepteur.</span><span class="sxs-lookup"><span data-stu-id="131b3-120">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="131b3-121">Créez un stub pour le récepteur.</span><span class="sxs-lookup"><span data-stu-id="131b3-121">Create a stub for the sink.</span></span>

    <span data-ttu-id="131b3-122">Un stub est une fonction wrapper produite à partir du récepteur.</span><span class="sxs-lookup"><span data-stu-id="131b3-122">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="131b3-123">L’exemple de code suivant appelle [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) pour créer un stub pour le récepteur.</span><span class="sxs-lookup"><span data-stu-id="131b3-123">The following code example calls [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) to create a stub for the sink.</span></span>

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  <span data-ttu-id="131b3-124">Appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour le wrapper et demandez un pointeur vers l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="131b3-124">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the wrapper, and request a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="131b3-125">L’exemple de code suivant appelle [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) et demande un pointeur vers l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="131b3-125">The following code example calls [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) and requests a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  <span data-ttu-id="131b3-126">Libère le pointeur d’objet récepteur.</span><span class="sxs-lookup"><span data-stu-id="131b3-126">Release the sink object pointer.</span></span>

    <span data-ttu-id="131b3-127">Vous pouvez libérer le pointeur d’objet, car le stub est désormais propriétaire du pointeur.</span><span class="sxs-lookup"><span data-stu-id="131b3-127">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="131b3-128">L’exemple de code suivant libère le pointeur d’objet récepteur.</span><span class="sxs-lookup"><span data-stu-id="131b3-128">The following code example releases the sink object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

6.  <span data-ttu-id="131b3-129">Utilisez le stub dans n’importe quel appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="131b3-129">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="131b3-130">Lorsque vous avez terminé avec l’appel, libérez le nombre de références locales.</span><span class="sxs-lookup"><span data-stu-id="131b3-130">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="131b3-131">L’exemple de code suivant utilise le stub dans un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="131b3-131">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="131b3-132">Parfois, vous devrez peut-être annuler un appel asynchrone après avoir effectué l’appel.</span><span class="sxs-lookup"><span data-stu-id="131b3-132">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="131b3-133">Si vous devez annuler l’appel, annulez l’appel avec le même pointeur que celui qui a initialement effectué l’appel.</span><span class="sxs-lookup"><span data-stu-id="131b3-133">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="131b3-134">L’exemple de code suivant montre comment annuler un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="131b3-134">The following code example shows how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  <span data-ttu-id="131b3-135">Libérez le nombre de références locales lorsque vous avez fini d’utiliser l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="131b3-135">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="131b3-136">Veillez à libérer le pointeur *pStubSink* uniquement après avoir confirmé que l’appel asynchrone n’a pas besoin d’être annulé.</span><span class="sxs-lookup"><span data-stu-id="131b3-136">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not need to be canceled.</span></span> <span data-ttu-id="131b3-137">En outre, ne libérez pas *pStubSink* après la libération du pointeur du récepteur *pSink* par WMI.</span><span class="sxs-lookup"><span data-stu-id="131b3-137">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="131b3-138">La libération de *pStubSink* après *pSink* crée un nombre de références circulaires dans lequel le récepteur et le stub restent en mémoire indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="131b3-138">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="131b3-139">Au lieu de cela, un emplacement possible pour libérer le pointeur se trouve dans l’appel [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , créé par WMI pour signaler que l’appel asynchrone d’origine est terminé.</span><span class="sxs-lookup"><span data-stu-id="131b3-139">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

8.  <span data-ttu-id="131b3-140">Lorsque vous avez terminé, désinitialisez COM à l’aide d’un appel à [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="131b3-140">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="131b3-141">L’exemple de code suivant montre comment appeler [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur *pUnsecApp* .</span><span class="sxs-lookup"><span data-stu-id="131b3-141">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

    <span data-ttu-id="131b3-142">Les exemples de code de cette rubrique requièrent la référence suivante et l' \# instruction include pour compiler correctement.</span><span class="sxs-lookup"><span data-stu-id="131b3-142">The code examples in this topic require the following reference and \#include statement to correctly compile.</span></span>

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

<span data-ttu-id="131b3-143">Pour plus d’informations sur la fonction [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) et les paramètres, consultez la documentation [com](../cossdk/component-services-portal.md) dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="131b3-143">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation in the Platform Software Development Kit (SDK).</span></span>

 

 
