---
title: Démarrage du processus de gravure
description: Démarrage du processus de gravure
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Lecteur Windows Media, gravure de CD
- Windows Media Player Object Model, gravage de CD
- modèle d’objet, gravage de CD
- Contrôle ActiveX du lecteur Windows Media, gravure de CD
- Contrôle ActiveX, gravage de CD
- Windows Media Player Mobile contrôle ActiveX, gravure de CD
- Lecteur Windows Media Mobile, gravure de CD
- Gravage de CD, démarrage du processus de gravure
- gravure de CD, démarrage du processus de gravure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940696"
---
# <a name="starting-the-burn-process"></a>Démarrage du processus de gravure

Avant de pouvoir procéder à la gravure, vous devez affecter une sélection à graver. Utilisez [IWMPCdromBurn ::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) pour spécifier une sélection pour la gravure.


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



Pour plus d’informations sur l’utilisation des sélections, consultez [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).

Pour démarrer l’opération de gravure, appelez [IWMPCdromBurn :: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



Vous pouvez arrêter l’opération de gravure en appelant [IWMPCdromBurn :: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gravure d’un CD**](burning-a-cd.md)
</dt> <dt>

[**Récupération de l’interface de gravure de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Effacement d’un CD réinscriptible**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Récupération de l’état du lecteur et du disque**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Récupération de l’état d’avancement**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




