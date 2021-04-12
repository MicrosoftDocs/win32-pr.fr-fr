---
title: Écriture d’un substitut personnalisé
description: Écriture d’un substitut personnalisé
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0899702f6626d586f8a819e8fee2c2e67b7c80
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316512"
---
# <a name="writing-a-custom-surrogate"></a><span data-ttu-id="636bf-103">Écriture d’un substitut personnalisé</span><span class="sxs-lookup"><span data-stu-id="636bf-103">Writing a Custom Surrogate</span></span>

<span data-ttu-id="636bf-104">Bien que le substitut fourni par le système soit plus que suffisant pour la plupart des situations, il existe des cas où l’écriture d’un substitut personnalisé peut être utile.</span><span class="sxs-lookup"><span data-stu-id="636bf-104">While the system-supplied surrogate will be more than adequate for most situations, there are some cases where writing a custom surrogate could be worthwhile.</span></span> <span data-ttu-id="636bf-105">En voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="636bf-105">Following are some examples:</span></span>

-   <span data-ttu-id="636bf-106">Un substitut personnalisé peut fournir des optimisations ou une sémantique qui ne figure pas dans le substitut système.</span><span class="sxs-lookup"><span data-stu-id="636bf-106">A custom surrogate could provide some optimizations or semantics not present in the system surrogate.</span></span>
-   <span data-ttu-id="636bf-107">Si une DLL in-process contient du code qui dépend du même processus que le client, le serveur DLL ne fonctionnera pas correctement s’il s’exécute dans le substitut système.</span><span class="sxs-lookup"><span data-stu-id="636bf-107">If an in-process DLL contains code that depends on being in the same process as the client, the DLL server will not function correctly if it is running in the system surrogate.</span></span> <span data-ttu-id="636bf-108">Un substitut personnalisé peut être adapté à une DLL spécifique pour gérer ce problème.</span><span class="sxs-lookup"><span data-stu-id="636bf-108">A custom surrogate could be tailored to a specific DLL to deal with this.</span></span>
-   <span data-ttu-id="636bf-109">Le substitut système prend en charge un modèle de thread mixte afin qu’il puisse charger des dll de modèle libre et cloisonné.</span><span class="sxs-lookup"><span data-stu-id="636bf-109">The system surrogate supports a mixed-threading model so that it can load both free and apartment model DLLs.</span></span> <span data-ttu-id="636bf-110">Un substitut personnalisé peut être adapté pour charger uniquement des dll cloisonnées pour des raisons d’efficacité ou pour accepter un argument de ligne de commande pour le type de DLL qu’il est autorisé à charger.</span><span class="sxs-lookup"><span data-stu-id="636bf-110">A custom surrogate might be tailored to load only apartment DLLs for reasons of efficiency or to accept a command-line argument for the type of DLL it is allowed to load.</span></span>
-   <span data-ttu-id="636bf-111">Un substitut personnalisé peut accepter des paramètres de ligne de commande supplémentaires que le substitut système ne fait pas.</span><span class="sxs-lookup"><span data-stu-id="636bf-111">A custom surrogate could take extra command-line parameters that the system surrogate does not.</span></span>
-   <span data-ttu-id="636bf-112">Le substitut système appelle [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) et lui indique d’utiliser les paramètres de sécurité existants qui se trouvent sous la clé [AppID](appid-key.md) dans le registre.</span><span class="sxs-lookup"><span data-stu-id="636bf-112">The system surrogate calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and tells it to use any existing security settings found under the [AppID](appid-key.md) key in the registry.</span></span> <span data-ttu-id="636bf-113">Un substitut personnalisé peut utiliser un autre contexte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="636bf-113">A custom surrogate could use another security context.</span></span>
-   <span data-ttu-id="636bf-114">Les interfaces qui ne sont pas accessibles à distance (telles que celles pour les ocx récents) ne fonctionnent pas avec le substitut système.</span><span class="sxs-lookup"><span data-stu-id="636bf-114">Interfaces that aren't remotable (such as those for recent OCXs) will not work with the system surrogate.</span></span> <span data-ttu-id="636bf-115">Un substitut personnalisé peut encapsuler les interfaces de la DLL avec sa propre implémentation et utiliser des dll proxy/stub avec une définition IDL accessible à distance qui permettrait à l’interface d’être distante.</span><span class="sxs-lookup"><span data-stu-id="636bf-115">A custom surrogate could wrap the DLL's interfaces with its own implementation and use proxy/stub DLLs with a remotable IDL definition that would allow the interface to be remoted.</span></span>

<span data-ttu-id="636bf-116">Le thread de substitution principal doit généralement effectuer les étapes de configuration suivantes :</span><span class="sxs-lookup"><span data-stu-id="636bf-116">The main surrogate thread should typically perform the following setup steps:</span></span>

1.  <span data-ttu-id="636bf-117">Appelez [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser le thread et définir le modèle de thread.</span><span class="sxs-lookup"><span data-stu-id="636bf-117">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the thread and set the threading model.</span></span>
2.  <span data-ttu-id="636bf-118">Si vous souhaitez que les serveurs DLL s’exécutent sur le serveur pour pouvoir utiliser les paramètres de sécurité de la clé de Registre **AppID** , appelez [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) avec la \_ fonctionnalité EOAC AppID.</span><span class="sxs-lookup"><span data-stu-id="636bf-118">If you want the DLL servers that are to run in the server to be able to use the security settings in the **AppID** registry key, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) with the EOAC\_APPID capability.</span></span> <span data-ttu-id="636bf-119">Dans le cas contraire, les paramètres de sécurité hérités seront utilisés.</span><span class="sxs-lookup"><span data-stu-id="636bf-119">Otherwise, legacy security settings will be used.</span></span>
3.  <span data-ttu-id="636bf-120">Appelez [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) pour inscrire l’interface de substitution à com.</span><span class="sxs-lookup"><span data-stu-id="636bf-120">Call [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) to register the surrogate interface to COM.</span></span>
4.  <span data-ttu-id="636bf-121">Appelez [**ISurrogate :: LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) pour le CLSID demandé.</span><span class="sxs-lookup"><span data-stu-id="636bf-121">Call [**ISurrogate::LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) for the requested CLSID.</span></span>
5.  <span data-ttu-id="636bf-122">Placez le thread principal dans une boucle pour appeler régulièrement [**coFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) .</span><span class="sxs-lookup"><span data-stu-id="636bf-122">Put main thread in a loop to call [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periodically.</span></span>
6.  <span data-ttu-id="636bf-123">Lorsque COM appelle [**ISurrogate :: FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), révoquez toutes les fabriques de classes et quittez.</span><span class="sxs-lookup"><span data-stu-id="636bf-123">When COM calls [**ISurrogate::FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revoke all class factories and exit.</span></span>

<span data-ttu-id="636bf-124">Un processus de substitution doit implémenter l’interface [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) .</span><span class="sxs-lookup"><span data-stu-id="636bf-124">A surrogate process must implement the [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) interface.</span></span> <span data-ttu-id="636bf-125">Cette interface doit être inscrite lorsqu’un nouveau substitut est démarré et après l’appel de [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="636bf-125">This interface should be registered when a new surrogate is started and after calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span> <span data-ttu-id="636bf-126">Comme indiqué dans les étapes précédentes, l’interface **ISurrogate** a deux méthodes appelées par com : [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), pour charger dynamiquement de nouveaux serveurs dll dans des substituts existants. et [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), pour libérer le substitut.</span><span class="sxs-lookup"><span data-stu-id="636bf-126">As indicated in the preceding steps, the **ISurrogate** interface has two methods that COM calls: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), to dynamically load new DLL servers into existing surrogates; and [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), to free the surrogate.</span></span>

<span data-ttu-id="636bf-127">L’implémentation de [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), que com appelle avec une demande de chargement, doit tout d’abord créer un objet de fabrique de classe qui prend en charge [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)et [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), puis appeler [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) pour inscrire l’objet en tant que fabrique de classe pour le CLSID demandé.</span><span class="sxs-lookup"><span data-stu-id="636bf-127">The implementation of [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), which COM calls with a load request, must first create a class factory object that supports [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), and then call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) to register the object as the class factory for the requested CLSID.</span></span>

<span data-ttu-id="636bf-128">La fabrique de classe inscrite par le processus de substitution n’est pas la fabrique de classe réelle implémentée par le serveur DLL, mais est une fabrique de classe générique implémentée par le processus de substitution qui prend en charge [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) et [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span><span class="sxs-lookup"><span data-stu-id="636bf-128">The class factory registered by the surrogate process is not the actual class factory implemented by the DLL server but is a generic class factory implemented by the surrogate process that supports [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span></span> <span data-ttu-id="636bf-129">Étant donné qu’il s’agit de la fabrique de classes du substitut, au lieu de celle du serveur DLL en cours d’inscription, la fabrique de classes du substitut doit utiliser la fabrique de classes réelle pour créer une instance de l’objet pour le CLSID inscrit.</span><span class="sxs-lookup"><span data-stu-id="636bf-129">Because it is the surrogate's class factory, rather than that of the DLL server that is being registered, the surrogate's class factory will need to use the real class factory to create an instance of the object for the registered CLSID.</span></span> <span data-ttu-id="636bf-130">La valeur [**IClassFactory :: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) du substitut doit ressembler à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="636bf-130">The surrogate's [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) should look something like the following example:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::CreateInstance(
  IUnknown* pUnkOuter, 
  REFIID iid, 
  void** ppv)
{
    void* pcf;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, IID_IClassFactory, &pcf);
    if ( FAILED(hr) )
        return hr;
    hr = ((IClassFactory*)pcf)->CreateInstance(pUnkOuter, iid, ppv);
    ((IClassFactory*)pcf)->Release();
    return hr;
}
 
```



<span data-ttu-id="636bf-131">La fabrique de classe de substitution doit également prendre en charge [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , car un appel à [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) peut demander toute interface à partir de la fabrique de classe inscrite, pas seulement [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="636bf-131">The surrogate's class factory must also support [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) because a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) can request any interface from the registered class factory, not just [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="636bf-132">En outre, étant donné que la fabrique de classe générique ne prend en charge que [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) et **IClassFactory**, les demandes d’autres interfaces doivent être dirigées vers l’objet réel.</span><span class="sxs-lookup"><span data-stu-id="636bf-132">Further, since the generic class factory supports only [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and **IClassFactory**, requests for other interfaces must be directed to the real object.</span></span> <span data-ttu-id="636bf-133">Par conséquent, il doit y avoir une méthode [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) qui doit ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="636bf-133">Thus, there should be a [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) method which should be similar to the following:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::MarshalInterface(
  IStream *pStm,  
  REFIID riid, void *pv, 
  WORD dwDestContext, 
  void *pvDestContext, 
  DWORD mshlflags )
{   
    void * pCF = NULL;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, riid, &pCF);
    if ( FAILED(hr) )
        return hr;   
    hr = CoMarshalInterface(pStm, riid, (IUnknown*)pCF, dwDestContext, pvDestContext,  mshlflags);
    ((IUnknown*)pCF)->Release();
    return S_OK;
 
```



<span data-ttu-id="636bf-134">Le substitut qui héberge un serveur DLL doit publier les objets de classe du serveur DLL avec un appel à [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span><span class="sxs-lookup"><span data-stu-id="636bf-134">The surrogate that houses a DLL server must publish the DLL server's class object(s) with a call to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span></span> <span data-ttu-id="636bf-135">Toutes les fabriques de classes pour les substituts de DLL doivent être inscrites en tant que \_ substitut REGCLS.</span><span class="sxs-lookup"><span data-stu-id="636bf-135">All class factories for DLL surrogates should be registered as REGCLS\_SURROGATE.</span></span> <span data-ttu-id="636bf-136">REGCLS \_ SINGLUSE et REGCLS \_ MULTIPLEUSE ne doivent pas être utilisés pour les serveurs dll chargés dans les substituts.</span><span class="sxs-lookup"><span data-stu-id="636bf-136">REGCLS\_SINGLUSE and REGCLS\_MULTIPLEUSE should not be used for DLL servers loaded into surrogates.</span></span>

<span data-ttu-id="636bf-137">Suivez ces instructions pour créer un processus de substitution quand cela est nécessaire pour garantir un comportement correct.</span><span class="sxs-lookup"><span data-stu-id="636bf-137">Following these guidelines for creating a surrogate process when it is necessary to do so should ensure proper behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="636bf-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="636bf-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="636bf-139">Substituts de DLL</span><span class="sxs-lookup"><span data-stu-id="636bf-139">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 