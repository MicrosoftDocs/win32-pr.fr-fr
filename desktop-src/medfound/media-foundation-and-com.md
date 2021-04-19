---
description: Microsoft Media Foundation utilise une combinaison de constructions COM, mais n’est pas une API entièrement basée sur COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation et COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106529535"
---
# <a name="media-foundation-and-com"></a>Media Foundation et COM

Microsoft Media Foundation utilise une combinaison de constructions COM, mais n’est pas une API entièrement basée sur COM. Cette rubrique décrit l’interaction entre COM et Media Foundation. Il définit également quelques pratiques recommandées pour le développement de composants de plug-in Media Foundation. Les pratiques suivantes peuvent vous aider à éviter des erreurs de programmation courantes mais subtiles.

-   [Meilleures pratiques pour les applications](#best-practices-for-applications)
-   [Meilleures pratiques pour les composants Media Foundation](#best-practices-for-media-foundation-components)
-   [Résumé](#summary)
-   [Rubriques connexes](#related-topics)

## <a name="best-practices-for-applications"></a>Meilleures pratiques pour les applications

Dans Media Foundation, le traitement asynchrone et les rappels sont gérés par les [files d’attente de travail](work-queues.md). Les files d’attente de travail ont toujours des threads de cloisonnement multithread (MTA). par conséquent, une application aura une implémentation plus simple si elle s’exécute également sur un thread MTA. Par conséquent, il est recommandé d’appeler [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) avec l’indicateur **coinit \_ multithread** .

Media Foundation ne marshale pas les objets cloisonnés (STA) à thread unique pour les threads de file d’attente de travail. Cela ne garantit pas non plus que les invariants STA sont conservés. Par conséquent, une application STA doit veiller à ne pas passer des objets STA ou des proxies à des API Media Foundation. Les objets qui sont STA uniquement ne sont pas pris en charge dans Media Foundation.

Si vous avez un proxy STA vers un objet MTA ou un objet thread libre, l’objet peut être marshalé vers un proxy MTA à l’aide d’un rappel de file d’attente de travail. La fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) peut retourner un pointeur brut ou un proxy STA, en fonction du modèle d’objet défini dans le registre pour ce CLSID. Si un proxy STA est retourné, vous ne devez pas passer le pointeur à une API Media Foundation.

Supposons, par exemple, que vous souhaitiez passer un pointeur **IPropertyStore** à la méthode [**IMFSourceResolver :: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) . Vous pouvez appeler **PSCreateMemoryPropertyStore** pour créer le pointeur **IPropertyStore** . Si vous appelez à partir d’un STA, vous devez marshaler le pointeur avant de le passer à **BeginCreateObjectFromURL**.

Le code suivant montre comment marshaler un proxy STA vers une API Media Foundation.


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



Pour plus d’informations sur la table d’interface globale, consultez [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Si vous utilisez Media Foundation in-process, les objets retournés à partir de Media Foundation méthodes et fonctions sont des pointeurs directs vers l’objet. Pour les Media Foundation interprocessus, ces objets peuvent être des proxies MTA et doivent être marshalés dans un thread STA, le cas échéant. De même, les objets obtenus à l’intérieur d’un rappel, par exemple une topologie de l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) , sont des pointeurs directs lorsque Media Foundation est utilisé dans le processus, mais sont des proxies MTA quand Media Foundation est utilisé interprocessus.

> [!Note]  
> Le scénario le plus courant pour l’utilisation de Media Foundation interprocessus consiste à utiliser le [chemin d’accès du média protégé](protected-media-path.md) (PMP). Toutefois, ces remarques s’appliquent à toutes les situations où des API Media Foundation sont utilisées par le biais de RPC.

 

Toutes les implémentations de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) doivent être compatibles avec le MTA. Il n’est pas nécessaire que ces objets soient des objets COM. Mais s’ils sont, ils ne peuvent pas s’exécuter dans le STA. La fonction [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) sera appelée sur un thread MTA workqueue, et l’objet [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) fourni sera soit un pointeur d’objet direct, soit un proxy MTA.

## <a name="best-practices-for-media-foundation-components"></a>Meilleures pratiques pour les composants Media Foundation

Il existe deux catégories d’objets Media Foundation qui doivent se préoccuper de COM. Certains composants, tels que les transformations ou les gestionnaires de flux d’octets, sont des objets COM complets créés par CLSID. Ces objets doivent suivre les règles pour les cloisonnements COM, pour les Media Foundation interprocessus et in-process. Les autres composants de Media Foundation ne sont pas des objets COM complets, mais ils ont besoin de proxys COM pour la lecture inter-processus. Les objets de cette catégorie incluent les sources de média et l’objet d’activation. Ces objets peuvent ignorer les problèmes de cloisonnement s’ils sont utilisés uniquement pour les Media Foundation in-process.

Bien que tous les objets Media Foundation ne soient pas des objets COM, toutes les interfaces Media Foundation dérivent de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Par conséquent, tous les objets Media Foundation doivent implémenter **IUnknown** conformément aux spécifications com, y compris les règles pour le décompte de références et [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Tous les objets de référence décomptés doivent également s’assurer que [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) n’autorise pas le déchargement du module tant que les objets persistent.

Les composants Media Foundation ne peuvent pas être des objets STA. De nombreux objets Media Foundation n’ont pas besoin d’être des objets COM. Mais s’ils sont, ils ne peuvent pas s’exécuter dans le STA. Tous les composants Media Foundation doivent être thread-safe. Certains objets Media Foundation doivent également être à threads libres ou à Neutral Apartment. Le tableau suivant spécifie les conditions requises pour les implémentations d’interfaces personnalisées :



| Interface                                                          | Category            | Cloisonnement requis       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | Proxy inter-processus | Libre-thread ou neutre |
| [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | Objet COM          | MTA                      |
| [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | Proxy inter-processus | Libre-thread ou neutre |
| [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | Objet COM          | Libre-thread ou neutre |
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | Proxy inter-processus | Libre-thread ou neutre |
| [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | Objet COM          | MTA                      |
| [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | Objet COM          | Libre-thread ou neutre |
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | Objet COM          | MTA                      |



 

Il peut y avoir des exigences supplémentaires en fonction de l’implémentation. Par exemple, si un récepteur multimédia implémente une autre interface qui permet à l’application d’effectuer des appels de fonction directs au récepteur, le récepteur doit être libre de thread ou neutre, afin qu’il puisse gérer les appels inter-processus directs. Tout objet peut être libre de threads ; ce tableau spécifie la configuration minimale requise.

La méthode recommandée pour implémenter des objets à thread libre ou neutre consiste à agréger le marshaleur libre de threads. Pour plus d’informations, consultez la documentation MSDN sur [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler). Conformément à la nécessité de ne pas passer des objets STA ou des proxies à des API Media Foundation, les objets à thread libre n’ont pas besoin de se préoccuper du marshaling des pointeurs d’entrée STA dans les composants à threads libres.

Les composants qui utilisent la file d’attente de travail de longue durée (**\_ fonction de \_ \_ longue durée \_ de la file d’attente de rappel MFASYNC**) doivent faire preuve de prudence. Les threads de la fonction long workqueue créent leur propre STA. Les composants qui utilisent la fonction long workqueue pour les rappels doivent éviter de créer des objets COM sur ces threads et doivent être prudents pour marshaler les proxies vers le STA en fonction des besoins.

## <a name="summary"></a>Résumé

Les applications auront plus de temps si elles interagissent avec les Media Foundation à partir d’un thread MTA, mais il est possible d’utiliser des Media Foundation à partir d’un thread STA. Media Foundation ne gère pas les composants STA, et les applications doivent veiller à ne pas passer des objets STA à des API Media Foundation. Certains objets ont des exigences supplémentaires, en particulier les objets qui s’exécutent dans une situation inter-processus. Le respect de ces recommandations permet d’éviter les erreurs COM, les blocages et les retards inattendus dans le traitement multimédia.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de plateforme Media Foundation](media-foundation-platform-apis.md)
</dt> <dt>

[Architecture Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 
