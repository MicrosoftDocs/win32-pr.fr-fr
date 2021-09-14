---
title: Gestion des événements en C++
description: Gestion des événements en C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Lecteur Windows Media, C++
- Lecteur Windows Media modèle objet, C++
- modèle objet, C++
- Lecteur Windows Media Mobile, C++
- Lecteur Windows Media ActiveX contrôle, C++
- Lecteur Windows Media contrôle Mobile ActiveX, C++
- contrôle ActiveX, C++
- Incorporation de programmes C++
- incorporation, programmes C++
- contrôle de ActiveX Lecteur Windows Media, gestion des événements
- Lecteur Windows Media contrôle Mobile ActiveX, gestion des événements
- contrôle de ActiveX, gestion des événements
- événements, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416250"
---
# <a name="handling-events-in-c"></a>Gestion des événements en C++

vous pouvez recevoir des événements de Lecteur Windows Media de deux manières.

-   Via **IDispatch** à l’aide de l’interface **\_ WMPOCXEvents** . Il s’agit de l’interface à utiliser pour la plupart des scénarios d’incorporation.
-   Via l’interface **IWMPEvents** . cette interface est disponible lorsque votre code est connecté au lecteur en mode complet, par exemple lors de la communication à distance du contrôle Lecteur Windows Media ou dans un plug-in d’interface utilisateur.

Dans chaque scénario, vous commencez à écouter des événements à l’aide de points de connexion COM.

L’exemple de code suivant utilise trois variables membres :


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



Pour récupérer un point de connexion, vous commencez par **QueryInterface** pour le conteneur de point de connexion.


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



Ensuite, demandez le point de connexion de l’interface d’événement que vous souhaitez utiliser. L’exemple de code suivant tente d’abord d’utiliser **IWMPEvents**. Si cette interface n’est pas disponible, elle utilise **\_ WMPOCXEvents**.


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



Enfin, appelez **IConnectionPoint :: Advise** pour demander des événements.


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



Dans l’exemple précédent, le premier paramètre suppose que la classe appelante implémente à la fois **IWMPEvents** et **\_ WMPOCXEvents**. Le deuxième paramètre est une valeur de retour que vous utilisez pour arrêter d’écouter des événements, par exemple lorsque votre programme s’arrête, à l’aide d’un code similaire à ce qui suit :


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



L’implémentation des gestionnaires d’événements pour **IWMPEvents** et **\_ WMPOCXEvents** diffère. Pour **IWMPEvents**, vous devez implémenter une fonction pour gérer chaque événement défini par l’interface, même si vous n’envisagez pas d’utiliser l’événement.


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



Pour implémenter des gestionnaires **\_ WMPOCXEvents** , vous devez utiliser **IDispatch :: Invoke**, qui est une implémentation de gestionnaire d’événements unique pour tous les événements qui se produisent sur l’interface **IDispatch** . Cela signifie que vous pouvez choisir de gérer uniquement certains événements et d’en ignorer d’autres. L’exemple de code suivant montre un gestionnaire **\_ WMPOCXEvents** , à l’aide de **Invoke**, qui gère uniquement les événements **OpenStateChange** et **PlayStateChange** :


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



Dans l’exemple de code précédent, chaque cas appelle simplement via le gestionnaire **IWMPEvents** pour l’événement correspondant. Si votre code gère uniquement **\_ WMPOCXEvents**, vous pouvez simplement appeler une fonction personnalisée ou gérer l’événement Inline après l’instruction **case** .

## <a name="receiving-events-from-windows-media-player-10-mobile"></a>réception d’événements de Lecteur Windows Media 10 Mobile

le contrôle Mobile Lecteur Windows Media 10 prend uniquement en charge la réception de certains événements via **\_ WMPOCXEvents** et **IWMPEvents**. Pour plus d’informations, consultez la documentation de **IWMPEvents**.

## <a name="samples"></a>Exemples

le package d’installation Lecteur Windows Media installe un exemple qui illustre la gestion des événements. Pour plus d’informations, consultez l’exemple WMPHost.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples**](samples.md)
</dt> <dt>

[**utilisation du contrôle Lecteur Windows Media dans un programme C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




