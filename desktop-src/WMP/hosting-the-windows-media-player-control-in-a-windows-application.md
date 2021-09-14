---
title: hébergement du contrôle Lecteur Windows Media dans une Application Windows
description: hébergement du contrôle Lecteur Windows Media dans une Application Windows
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet, incorporation ActiveX contrôle
- Lecteur Windows Media Mobile, incorporation ActiveX contrôle
- contrôle de ActiveX Lecteur Windows Media, incorporation
- Lecteur Windows Media contrôle de ActiveX Mobile, incorporation
- contrôle de ActiveX, incorporation
- Lecteur Windows Media, programmes basés sur Windows
- Lecteur Windows Media modèle objet, programmes basés sur des Windows
- modèle objet, programmes basés sur des Windows
- Lecteur Windows Media programmes mobiles, à base de Windows
- Lecteur Windows Media contrôle ActiveX, programmes basés sur Windows
- Lecteur Windows Media contrôle de ActiveX Mobile, programmes basés sur des Windows
- contrôle de ActiveX, programmes basés sur Windows
- incorporation de programmes basés sur Windows
- incorporation, programmes basés sur des Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416240"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>hébergement du contrôle Lecteur Windows Media dans une Application Windows

pour utiliser le contrôle ActiveX Lecteur Windows Media (y compris l’interface utilisateur) dans un programme basé sur Windows, vous devez fournir un conteneur de contrôle ActiveX. ATL fournit la classe **CAxWindow** pour fournir ActiveX fonctionnalité de fenêtre hôte.

pour héberger le contrôle Lecteur Windows Media à l’aide de la classe **CAxWindow** , procédez comme suit :

1.  Incluez les en-têtes suivants :
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  Déclarez les variables membres, comme suit :
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  lorsque votre fenêtre d’application est créée, appelez **AtlAxWinInit**, qui est requis lors de l’utilisation de la fenêtre hôte ATL ActiveX.
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  Déclarez les variables locales pour les codes de retour et pour contenir le pointeur vers l’interface de la fenêtre hôte :
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  Créez la fenêtre hôte :
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  Récupérez le pointeur d’interface de la fenêtre hôte :
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  créez le contrôle Lecteur Windows Media dans la fenêtre hôte à l’aide de l’ID de classe :
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Récupérez le pointeur d’interface **IWMPPlayer** :
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

Lorsque vous écrivez votre propre code, veillez à vérifier les erreurs dans chaque code de retour **HRESULT** .

pour obtenir un exemple complet qui illustre comment héberger le contrôle Lecteur Windows Media ActiveX à l’aide de la classe **CAxWindow** , consultez l’exemple WMPHost.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>hébergement du contrôle Mobile Lecteur Windows Media 10 dans Windows CE

Microsoft embedded Visual C++ 4,0 et le kit de développement logiciel (sdk) Pocket PC 2003 ou le kit de développement logiciel (sdk) Smartphone 2003 doivent être installés lors du développement d’applications basées sur Windows CE qui hébergent un contrôle Mobile Lecteur Windows Media 10. en outre, contrairement à atl pour Windows, atl pour Windows CE ne prend pas en charge le modèle de thread cloisonné. Par conséquent, vous devez rechercher toutes les instances de cloisonnement Threading dans votre projet ATL et les modifier pour utiliser le Threading libre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples**](samples.md)
</dt> <dt>

[**utilisation du contrôle Lecteur Windows Media dans un programme C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




