---
description: Comment configurer le localisateur de proxy
ms.assetid: ddc28add-ebf5-4a68-bdf4-dc5f33ab74da
title: Comment configurer le localisateur de proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6b383dda9ac78b2c62aa8481a09cc5c0d7b3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527772"
---
# <a name="how-to-configure-the-proxy-locator"></a>Comment configurer le localisateur de proxy

L’application peut modifier la configuration par défaut du localisateur de proxy en affectant à la propriété [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) l’objet de fabrique du localisateur de proxy implémenté par l’application. Lorsque l’application appelle des méthodes de résolution de source pour créer la source réseau, Media Foundation appelle la fabrique de recherche de proxy. Cet objet crée le localisateur de proxy avec une configuration personnalisée.

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a>Pour modifier le paramètre de configuration par défaut du localisateur de proxy

1.  Implémentez l’interface [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .
2.  Dans la méthode [**IMFNetProxyLocatorFactory :: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) , procédez comme suit :
    1.  Créer une banque de propriétés.
    2.  Définissez les paramètres de configuration pour le localisateur de proxy. Pour plus d’informations sur ces paramètres, consultez [paramètres de configuration du localisateur de proxy](proxy-locator-configuration-settings.md).
    3.  Appelez la fonction [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . Transmettez la Banque de propriétés et le protocole. Le protocole est spécifié dans le paramètre *pszProtocol* de [**CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator).
3.  Créez une instance de votre classe de fabrique du localisateur proxy et récupérez un pointeur vers son interface [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .
4.  Créez une autre banque de propriétés et définissez la valeur de la propriété [**MFNETSOURCE \_ PROXYLOCATORFACTORY**](mfnetsource-proxylocatorfactory-property.md) sur le pointeur [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) de l’étape 3.
5.  Lorsque vous créez la source réseau, transmettez la Banque de propriétés dans le paramètre *pProps* des méthodes de programme de résolution source, telles que [**IMFSourceResolver :: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).

## <a name="example"></a>Exemple

L’exemple de code suivant implémente l’interface [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) . La méthode [**IMFNetProxyLocatorFactory :: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) crée une instance du localisateur de proxy par défaut et la configure pour fonctionner en mode de détection automatique.


```C++
class CProxyLocatorFactory : public IMFNetProxyLocatorFactory 
{
    LONG m_cRef;

public:

    CProxyLocatorFactory() : m_cRef(1)
    {
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CProxyLocatorFactory, IMFNetProxyLocatorFactory),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP CreateProxyLocator(
        LPCWSTR pszProtocol, 
        IMFNetProxyLocator **ppProxyLocator
        )
    {
        *ppProxyLocator = NULL;

        //Create the property store object
        IPropertyStore *pProp = NULL;

        HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pProp));

        if(SUCCEEDED(hr))
        {
            // Property key for proxy settings.
            PROPERTYKEY key;
            key.fmtid = MFNETSOURCE_PROXYSETTINGS;        
            key.pid = 0;

            // Proxy settings
            PROPVARIANT var;
            var.vt = VT_I4;
            var.lVal = MFNET_PROXYSETTING_AUTO;

            hr = pProp->SetValue(key, var);
        }

        //Create the default proxy locator.

        if(SUCCEEDED(hr))
        {
            hr = MFCreateProxyLocator(pszProtocol, pProp, ppProxyLocator);
        }

        SafeRelease(&pProp);
        return hr;
    }
};
```



L’exemple suivant montre comment passer le pointeur [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) à la source réseau.


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set a proxy locator on the network source.

HRESULT CreateMediaSourceWithProxyLocator(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    IMFNetProxyLocatorFactory *pFactory = new (std::nothrow) CProxyLocatorFactory();

    if (pFactory == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_PROXYLOCATORFACTORY;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        var.punkVal = pFactory;

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge du proxy pour les sources réseau](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



