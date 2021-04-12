---
title: Hébergement du contrôle du lecteur Windows Media dans une application Windows
description: Hébergement du contrôle du lecteur Windows Media dans une application Windows
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Windows Media Player, programmes Windows
- Windows Media Player Object Model, programmes Windows
- modèle objet, programmes Windows
- Windows Media Player Mobile, programmes Windows
- Windows Media Player ActiveX Control, programmes Windows
- Windows Media Player Mobile contrôle ActiveX, programmes Windows
- Contrôle ActiveX, programmes Windows
- Incorporation de programmes basés sur Windows
- incorporation, programmes Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310766"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>Hébergement du contrôle du lecteur Windows Media dans une application Windows

Pour utiliser le contrôle ActiveX du lecteur Windows Media (y compris l’interface utilisateur) dans un programme Windows, vous devez fournir un conteneur de contrôles ActiveX. ATL fournit la classe **CAxWindow** pour fournir les fonctionnalités de la fenêtre hôte ActiveX.

Pour héberger le contrôle du lecteur Windows Media à l’aide de la classe **CAxWindow** , procédez comme suit :

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

    

3.  Lorsque votre fenêtre d’application est créée, appelez **AtlAxWinInit**, qui est requis lors de l’utilisation de la fenêtre hôte ActiveX ATL.
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

    

7.  Créez le contrôle du lecteur Windows Media dans la fenêtre hôte à l’aide de l’ID de classe :
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Récupérez le pointeur d’interface **IWMPPlayer** :
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

Lorsque vous écrivez votre propre code, veillez à vérifier les erreurs dans chaque code de retour **HRESULT** .

Pour obtenir un exemple complet illustrant comment héberger le contrôle Windows Media Player ActiveX à l’aide de la classe **CAxWindow** , consultez l’exemple WMPHost.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>Hébergement du contrôle mobile du lecteur Windows Media 10 dans Windows CE

Microsoft eMbedded Visual C++ 4,0 et le kit de développement logiciel (SDK) Pocket PC 2003 ou le kit de développement logiciel (SDK) Smartphone 2003 doivent être installés lors du développement d’applications basées sur Windows CE qui hébergent un contrôle mobile Windows Media Player 10. En outre, contrairement à ATL pour Windows, ATL pour Windows CE ne prend pas en charge le modèle de thread cloisonné. Par conséquent, vous devez rechercher toutes les instances de cloisonnement Threading dans votre projet ATL et les modifier pour utiliser le Threading libre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples**](samples.md)
</dt> <dt>

[**Utilisation du contrôle du lecteur Windows Media dans un programme C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




