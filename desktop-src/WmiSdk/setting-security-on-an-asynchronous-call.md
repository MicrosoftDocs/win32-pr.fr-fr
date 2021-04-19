---
description: Les appels asynchrones présentent des risques sérieux pour la sécurité, car un rappel au récepteur peut ne pas être le résultat de l’appel asynchrone par l’application ou le script d’origine.
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: Définition de la sécurité sur un appel asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542010"
---
# <a name="setting-security-on-an-asynchronous-call"></a><span data-ttu-id="f28d3-103">Définition de la sécurité sur un appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="f28d3-103">Setting Security on an Asynchronous Call</span></span>

<span data-ttu-id="f28d3-104">Les appels asynchrones présentent des risques sérieux pour la sécurité, car un rappel au [*récepteur*](gloss-s.md) peut ne pas être le résultat de l’appel asynchrone par l’application ou le script d’origine.</span><span class="sxs-lookup"><span data-stu-id="f28d3-104">Asynchronous calls present serious security risks because a callback to the [*sink*](gloss-s.md) may not be a result of the asynchronous call by the original application or script.</span></span> <span data-ttu-id="f28d3-105">La sécurité des connexions à distance est basée sur le chiffrement de la communication entre le client et le fournisseur sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="f28d3-105">Security in remote connections is based on encryption of the communication between the client and the provider on the remote computer.</span></span> <span data-ttu-id="f28d3-106">En C++, vous pouvez définir le chiffrement via le paramètre de niveau d’authentification dans l’appel à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="f28d3-106">In C++ you can set encryption through the authentication level parameter in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="f28d3-107">Dans les scripts, définissez *AuthenticationLevel* dans la connexion moniker ou sur un objet [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="f28d3-107">In scripting, set the *AuthenticationLevel* in the moniker connection or on an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="f28d3-108">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="f28d3-108">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="f28d3-109">Il existe des risques de sécurité pour les appels asynchrones, car WMI réduit le niveau d’authentification sur un rappel jusqu’à ce que le rappel aboutisse.</span><span class="sxs-lookup"><span data-stu-id="f28d3-109">The security risks for asynchronous calls exist because WMI lowers the authentication level on a callback until the callback succeeds.</span></span> <span data-ttu-id="f28d3-110">Sur un appel asynchrone sortant, le client peut définir le niveau d’authentification de la connexion à WMI.</span><span class="sxs-lookup"><span data-stu-id="f28d3-110">On an outgoing asynchronous call, the client can set the authentication level on the connection to WMI.</span></span> <span data-ttu-id="f28d3-111">WMI récupère les paramètres de sécurité de l’appel client et tente d’effectuer un rappel avec le même niveau d’authentification.</span><span class="sxs-lookup"><span data-stu-id="f28d3-111">WMI retrieves the security settings on the client call and attempts to call back with the same authentication level.</span></span> <span data-ttu-id="f28d3-112">Le rappel est toujours initié au niveau de confidentialité de l' **\_ authentification au niveau d' \_ authentification \_ \_ \_ RPC C** .</span><span class="sxs-lookup"><span data-stu-id="f28d3-112">The callback is always initiated at the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** level.</span></span> <span data-ttu-id="f28d3-113">Si le rappel échoue, WMI réduit le niveau d’authentification à un niveau où le rappel peut être réussi, le cas échéant, au niveau d’authentification **RPC \_ C \_ \_ \_** sans.</span><span class="sxs-lookup"><span data-stu-id="f28d3-113">If the callback fails, WMI lowers the authentication level to a level where the callback can succeed, if necessary, to **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span> <span data-ttu-id="f28d3-114">Dans le contexte des appels au sein du système local où le service d’authentification n’est pas Kerberos, le rappel est toujours retourné au **\_ niveau d’authentification RPC C- \_ \_ \_ None**.</span><span class="sxs-lookup"><span data-stu-id="f28d3-114">In the context of calls within the local system where the authentication service is not Kerberos, the callback is always returned at **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span>

<span data-ttu-id="f28d3-115">Le niveau d’authentification minimal est **RPC \_ C \_ Authn \_ niveau \_** (**wbemAuthenticationLevelPkt** pour les scripts).</span><span class="sxs-lookup"><span data-stu-id="f28d3-115">The minimum authentication level is **RPC\_C\_AUTHN\_LEVEL\_PKT** (**wbemAuthenticationLevelPkt** for scripting).</span></span> <span data-ttu-id="f28d3-116">Toutefois, vous pouvez spécifier un niveau plus élevé, tel que laconfidentialité de l' **\_ \_ authentification \_ au niveau \_ \_** de l’authentification (wbemAuthenticationLevelPktPrivacy) RPC C.</span><span class="sxs-lookup"><span data-stu-id="f28d3-116">However, you can specify a higher level, such as **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="f28d3-117">Il est recommandé que les applications clientes ou les scripts définissent le niveau d’authentification à la valeur **\_ \_ \_ \_ par défaut du niveau d’authentification RPC C** (**wbemAuthenticationLevelDefault**), ce qui permet de négocier le niveau d’authentification au niveau spécifié par le serveur.</span><span class="sxs-lookup"><span data-stu-id="f28d3-117">It is recommended that client applications or scripts set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** (**wbemAuthenticationLevelDefault**) which allows the authentication level to be negotiated to the level specified by the server.</span></span>

<span data-ttu-id="f28d3-118">La valeur de Registre **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** contrôle si WMI vérifie la présence d’un niveau d’authentification acceptable dans les rappels.</span><span class="sxs-lookup"><span data-stu-id="f28d3-118">The **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault** registry value controls whether WMI checks for an acceptable authentication level in callbacks.</span></span> <span data-ttu-id="f28d3-119">Il s’agit du seul mécanisme de protection de la sécurité du récepteur pour les appels asynchrones effectués dans des scripts ou des Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f28d3-119">This is the only mechanism for protecting sink security for asynchronous calls made in scripting or Visual Basic.</span></span> <span data-ttu-id="f28d3-120">Par défaut, cette clé de Registre est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="f28d3-120">By default, this registry key is set to zero.</span></span> <span data-ttu-id="f28d3-121">Si la clé de Registre est égale à zéro, WMI ne vérifie pas les niveaux d’authentification.</span><span class="sxs-lookup"><span data-stu-id="f28d3-121">If the registry key is zero then WMI does not verify authentication levels.</span></span> <span data-ttu-id="f28d3-122">Pour sécuriser les appels asynchrones dans les scripts, affectez la valeur 1 à la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="f28d3-122">To secure asynchronous calls in scripting, set the registry key to 1.</span></span> <span data-ttu-id="f28d3-123">Les clients C++ peuvent appeler [**IWbemUnsecuredApartment :: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) pour contrôler l’accès au récepteur.</span><span class="sxs-lookup"><span data-stu-id="f28d3-123">C++ clients can call [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) to control access to the sink.</span></span> <span data-ttu-id="f28d3-124">La valeur est créée n’importe où par défaut.</span><span class="sxs-lookup"><span data-stu-id="f28d3-124">The value is created anywhere by default.</span></span>

<span data-ttu-id="f28d3-125">Les rubriques suivantes fournissent des exemples de définition de la sécurité des appels asynchrones :</span><span class="sxs-lookup"><span data-stu-id="f28d3-125">The following topics provide examples of setting asynchronous call security:</span></span>

-   [<span data-ttu-id="f28d3-126">Définition de la sécurité sur un appel asynchrone dans VBScript</span><span class="sxs-lookup"><span data-stu-id="f28d3-126">Setting Security on an Asynchronous Call in VBScript</span></span>](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   <span data-ttu-id="f28d3-127">Définition de la sécurité des appels asynchrones en C++</span><span class="sxs-lookup"><span data-stu-id="f28d3-127">Setting Asynchronous Call Security in C++</span></span>

## <a name="setting-asynchronous-call-security-in-c"></a><span data-ttu-id="f28d3-128">Définition de la sécurité des appels asynchrones en C++</span><span class="sxs-lookup"><span data-stu-id="f28d3-128">Setting Asynchronous Call Security in C++</span></span>

<span data-ttu-id="f28d3-129">La méthode [**IWbemUnsecuredApartment :: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) est semblable à la méthode [**IUnsecuredApartment :: CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) et crée un récepteur dans un processus séparé, Unsecapp.exe, pour recevoir des rappels.</span><span class="sxs-lookup"><span data-stu-id="f28d3-129">The [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) method is similar to [**IUnsecuredApartment::CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) method and creates a sink in a separate process, Unsecapp.exe, to receive callbacks.</span></span> <span data-ttu-id="f28d3-130">Toutefois, la méthode **CreateSinkStub** a un paramètre *dwFlag* qui spécifie comment le processus distinct gère le contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="f28d3-130">However, the **CreateSinkStub** method has a *dwFlag* parameter that specifies how the separate process handles access control.</span></span>

<span data-ttu-id="f28d3-131">Le paramètre *dwFlag* spécifie l’une des actions suivantes pour Unsecapp.exe :</span><span class="sxs-lookup"><span data-stu-id="f28d3-131">The *dwFlag* parameter specifies one of the following actions for Unsecapp.exe:</span></span>

-   <span data-ttu-id="f28d3-132">Utilisez le paramètre de clé de Registre pour déterminer s’il faut ou non vérifier l’accès.</span><span class="sxs-lookup"><span data-stu-id="f28d3-132">Use the registry key setting to determine whether or not to check access.</span></span>
-   <span data-ttu-id="f28d3-133">Ignorez la clé de Registre et vérifiez toujours l’accès.</span><span class="sxs-lookup"><span data-stu-id="f28d3-133">Ignore the registry key and always check access.</span></span>
-   <span data-ttu-id="f28d3-134">Ignorer la clé de Registre et ne jamais vérifier l’accès.</span><span class="sxs-lookup"><span data-stu-id="f28d3-134">Ignore the registry key and never check access.</span></span>

<span data-ttu-id="f28d3-135">L’exemple de code de cette rubrique requiert l' \# instruction include suivante pour compiler correctement.</span><span class="sxs-lookup"><span data-stu-id="f28d3-135">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="f28d3-136">La procédure suivante décrit comment effectuer un appel asynchrone avec [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span><span class="sxs-lookup"><span data-stu-id="f28d3-136">The following procedure describes how to perform an asynchronous call with [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span></span>

<span data-ttu-id="f28d3-137">**Pour effectuer un appel asynchrone avec IWbemUnsecuredApartment**</span><span class="sxs-lookup"><span data-stu-id="f28d3-137">**To perform an asynchronous call with IWbemUnsecuredApartment**</span></span>

1.  <span data-ttu-id="f28d3-138">Créez un processus dédié avec un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="f28d3-138">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="f28d3-139">L’exemple de code suivant appelle [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un processus dédié.</span><span class="sxs-lookup"><span data-stu-id="f28d3-139">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
                     (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="f28d3-140">Instanciez l’objet récepteur.</span><span class="sxs-lookup"><span data-stu-id="f28d3-140">Instantiate the sink object.</span></span>

    <span data-ttu-id="f28d3-141">L’exemple de code suivant crée un nouvel objet récepteur.</span><span class="sxs-lookup"><span data-stu-id="f28d3-141">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="f28d3-142">Créez un stub pour le récepteur.</span><span class="sxs-lookup"><span data-stu-id="f28d3-142">Create a stub for the sink.</span></span>

    <span data-ttu-id="f28d3-143">Un stub est une fonction wrapper produite à partir du récepteur.</span><span class="sxs-lookup"><span data-stu-id="f28d3-143">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="f28d3-144">L’exemple de code suivant crée un stub pour le récepteur.</span><span class="sxs-lookup"><span data-stu-id="f28d3-144">The following code example creates a stub for the sink.</span></span>

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  <span data-ttu-id="f28d3-145">Libère le pointeur d’objet récepteur.</span><span class="sxs-lookup"><span data-stu-id="f28d3-145">Release the sink object pointer.</span></span>

    <span data-ttu-id="f28d3-146">Vous pouvez libérer le pointeur d’objet, car le stub est désormais propriétaire du pointeur.</span><span class="sxs-lookup"><span data-stu-id="f28d3-146">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="f28d3-147">L’exemple de code suivant libère le pointeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="f28d3-147">The following code example releases the object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

5.  <span data-ttu-id="f28d3-148">Utilisez le stub dans n’importe quel appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f28d3-148">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="f28d3-149">Lorsque vous avez terminé avec l’appel, libérez le nombre de références locales.</span><span class="sxs-lookup"><span data-stu-id="f28d3-149">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="f28d3-150">L’exemple de code suivant utilise le stub dans un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f28d3-150">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="f28d3-151">Parfois, vous devrez peut-être annuler un appel asynchrone après avoir effectué l’appel.</span><span class="sxs-lookup"><span data-stu-id="f28d3-151">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="f28d3-152">Si vous devez annuler l’appel, annulez l’appel avec le même pointeur que celui qui a initialement effectué l’appel.</span><span class="sxs-lookup"><span data-stu-id="f28d3-152">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="f28d3-153">L’exemple de code suivant décrit comment annuler un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f28d3-153">The following code example describes how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  <span data-ttu-id="f28d3-154">Libérez le nombre de références locales lorsque vous avez fini d’utiliser l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f28d3-154">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="f28d3-155">Veillez à libérer le pointeur *pStubSink* uniquement après avoir vérifié que l’appel asynchrone ne doit pas être annulé.</span><span class="sxs-lookup"><span data-stu-id="f28d3-155">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not must be canceled.</span></span> <span data-ttu-id="f28d3-156">En outre, ne libérez pas *pStubSink* après la libération du pointeur du récepteur *pSink* par WMI.</span><span class="sxs-lookup"><span data-stu-id="f28d3-156">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="f28d3-157">La libération de *pStubSink* après *pSink* crée un nombre de références circulaires dans lequel le récepteur et le stub restent en mémoire indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="f28d3-157">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="f28d3-158">Au lieu de cela, un emplacement possible pour libérer le pointeur se trouve dans l’appel [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , créé par WMI pour signaler que l’appel asynchrone d’origine est terminé.</span><span class="sxs-lookup"><span data-stu-id="f28d3-158">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

7.  <span data-ttu-id="f28d3-159">Lorsque vous avez terminé, désinitialisez COM à l’aide d’un appel à [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="f28d3-159">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="f28d3-160">L’exemple de code suivant montre comment appeler [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur *pUnsecApp* .</span><span class="sxs-lookup"><span data-stu-id="f28d3-160">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

<span data-ttu-id="f28d3-161">Pour plus d’informations sur la fonction [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) et les paramètres, consultez la documentation [com](../cossdk/component-services-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f28d3-161">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation.</span></span>

 

 
