---
title: Écriture d’un substitut personnalisé
description: Écriture d’un substitut personnalisé
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0899702f6626d586f8a819e8fee2c2e67b7c80
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363576"
---
# <a name="writing-a-custom-surrogate"></a>Écriture d’un substitut personnalisé

Bien que le substitut fourni par le système soit plus que suffisant pour la plupart des situations, il existe des cas où l’écriture d’un substitut personnalisé peut être utile. En voici quelques exemples :

-   Un substitut personnalisé peut fournir des optimisations ou une sémantique qui ne figure pas dans le substitut système.
-   Si une DLL in-process contient du code qui dépend du même processus que le client, le serveur DLL ne fonctionnera pas correctement s’il s’exécute dans le substitut système. Un substitut personnalisé peut être adapté à une DLL spécifique pour gérer ce problème.
-   Le substitut système prend en charge un modèle de thread mixte afin qu’il puisse charger des dll de modèle libre et cloisonné. Un substitut personnalisé peut être adapté pour charger uniquement des dll cloisonnées pour des raisons d’efficacité ou pour accepter un argument de ligne de commande pour le type de DLL qu’il est autorisé à charger.
-   Un substitut personnalisé peut accepter des paramètres de ligne de commande supplémentaires que le substitut système ne fait pas.
-   Le substitut système appelle [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) et lui indique d’utiliser les paramètres de sécurité existants qui se trouvent sous la clé [AppID](appid-key.md) dans le registre. Un substitut personnalisé peut utiliser un autre contexte de sécurité.
-   Les interfaces qui ne sont pas accessibles à distance (telles que celles pour les ocx récents) ne fonctionnent pas avec le substitut système. Un substitut personnalisé peut encapsuler les interfaces de la DLL avec sa propre implémentation et utiliser des dll proxy/stub avec une définition IDL accessible à distance qui permettrait à l’interface d’être distante.

Le thread de substitution principal doit généralement effectuer les étapes de configuration suivantes :

1.  Appelez [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser le thread et définir le modèle de thread.
2.  Si vous souhaitez que les serveurs DLL s’exécutent sur le serveur pour pouvoir utiliser les paramètres de sécurité de la clé de Registre **AppID** , appelez [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) avec la \_ fonctionnalité EOAC AppID. Dans le cas contraire, les paramètres de sécurité hérités seront utilisés.
3.  Appelez [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) pour inscrire l’interface de substitution à com.
4.  Appelez [**ISurrogate :: LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) pour le CLSID demandé.
5.  Placez le thread principal dans une boucle pour appeler régulièrement [**coFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) .
6.  Lorsque COM appelle [**ISurrogate :: FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), révoquez toutes les fabriques de classes et quittez.

Un processus de substitution doit implémenter l’interface [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) . Cette interface doit être inscrite lorsqu’un nouveau substitut est démarré et après l’appel de [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Comme indiqué dans les étapes précédentes, l’interface **ISurrogate** a deux méthodes appelées par com : [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), pour charger dynamiquement de nouveaux serveurs dll dans des substituts existants. et [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), pour libérer le substitut.

L’implémentation de [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), que com appelle avec une demande de chargement, doit tout d’abord créer un objet de fabrique de classe qui prend en charge [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)et [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), puis appeler [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) pour inscrire l’objet en tant que fabrique de classe pour le CLSID demandé.

La fabrique de classe inscrite par le processus de substitution n’est pas la fabrique de classe réelle implémentée par le serveur DLL, mais est une fabrique de classe générique implémentée par le processus de substitution qui prend en charge [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) et [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). Étant donné qu’il s’agit de la fabrique de classes du substitut, au lieu de celle du serveur DLL en cours d’inscription, la fabrique de classes du substitut doit utiliser la fabrique de classes réelle pour créer une instance de l’objet pour le CLSID inscrit. La valeur [**IClassFactory :: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) du substitut doit ressembler à l’exemple suivant :


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



La fabrique de classe de substitution doit également prendre en charge [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , car un appel à [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) peut demander toute interface à partir de la fabrique de classe inscrite, pas seulement [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). En outre, étant donné que la fabrique de classe générique ne prend en charge que [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) et **IClassFactory**, les demandes d’autres interfaces doivent être dirigées vers l’objet réel. Par conséquent, il doit y avoir une méthode [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) qui doit ressembler à ce qui suit :


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



Le substitut qui héberge un serveur DLL doit publier les objets de classe du serveur DLL avec un appel à [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject). Toutes les fabriques de classes pour les substituts de DLL doivent être inscrites en tant que \_ substitut REGCLS. REGCLS \_ SINGLUSE et REGCLS \_ MULTIPLEUSE ne doivent pas être utilisés pour les serveurs dll chargés dans les substituts.

Suivez ces instructions pour créer un processus de substitution quand cela est nécessaire pour garantir un comportement correct.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Substituts de DLL](dll-surrogates.md)
</dt> </dl>

 

 