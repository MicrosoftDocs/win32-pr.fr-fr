---
title: Utilisation du contrôle du lecteur Windows Media dans une application console
description: Utilisation du contrôle du lecteur Windows Media dans une application console
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Windows Media Player, applications console
- Windows Media Player Object Model, applications console
- modèle objet, applications console
- Windows Media Player Mobile, applications console
- Contrôle ActiveX du lecteur Windows Media, applications console
- Windows Media Player Mobile contrôle ActiveX, applications console
- Contrôle ActiveX, applications console
- incorporation d’applications console
- incorporation, applications console
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cc7701fc10848ca246d9cf100d0716e1955b5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310393"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a>Utilisation du contrôle du lecteur Windows Media dans une application console

Vous pouvez créer une instance de l’objet COM du lecteur Windows Media directement à l’aide de **CoCreateInstance**. Dans ce cas, l’objet **Player** n’affiche aucune interface utilisateur. Toutefois, l’objet est toujours utile pour les tâches qui n’ont pas besoin de l’interface utilisateur, telles que l’utilisation de la bibliothèque, la lecture de fichiers audio numériques ou l’accès aux propriétés du lecteur.

L’exemple de code suivant montre un programme de console simple qui affiche la version du lecteur Windows Media dans une boîte de message. L’exemple de code utilise ATL pour tirer parti des pointeurs intelligents et de la classe de chaîne **CComBSTR** .


```C++
#include "atlbase.h"
#include "atlwin.h"
#include "wmp.h"

int _tmain(int argc, _TCHAR* argv[])
{
    CoInitialize(NULL);

    HRESULT hr = S_OK;
    CComBSTR bstrVersionInfo; // Contains the version string.
    CComPtr<IWMPPlayer> spPlayer;  // Smart pointer to IWMPPlayer interface.

    hr = spPlayer.CoCreateInstance( __uuidof(WindowsMediaPlayer), 0, CLSCTX_INPROC_SERVER );

    if(SUCCEEDED(hr))
    {
        hr = spPlayer->get_versionInfo(&bstrVersionInfo);
    }

    if(SUCCEEDED(hr))
    {
        // Show the version in a message box.
        COLE2T pStr(bstrVersionInfo);
        MessageBox( NULL, (LPCSTR)pStr, _T("Windows Media Player Version"), MB_OK );
    }

    // Clean up.
    spPlayer.Release();
    CoUninitialize();

    return 0;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du contrôle du lecteur Windows Media dans un programme C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




