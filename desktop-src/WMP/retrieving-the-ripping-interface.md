---
title: Récupération de l’interface d’extraction
description: Récupération de l’interface d’extraction
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Lecteur Windows Media, extraction de CD
- modèle d’objet Lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- contrôle de ActiveX Lecteur Windows Media, extraction de CD
- contrôle de ActiveX, extraction de CD
- Lecteur Windows Media contrôle de ActiveX Mobile, extraction de CD
- Lecteur Windows Media Mobile, extraction de CD
- Extraction de CD, interface IWMPCdromRip
- extraction de CDs, interface IWMPCdromRip
- Interface IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2179e4f38eee121d7b8fefc028adf232eb724264362396c8cacedfcc55b162d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002549"
---
# <a name="retrieving-the-ripping-interface"></a>Récupération de l’interface d’extraction

Pour énumérer les lecteurs de CD sur l’ordinateur de l’utilisateur, utilisez l’interface **IWMPCdromCollection** . Récupérez un pointeur vers cette interface en appelant [IWMPCore :: obtenir \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

En utilisant les méthodes d' [extraction de \_ nombre](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) et d' [élément](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) , vous pouvez effectuer une itération de la collection pour récupérer une interface [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) pour chaque lecteur de CD sur l’ordinateur de l’utilisateur.

L’interface **IWMPCdrom** représente un lecteur de CD individuel. Avant de commencer l’extraction d’un CD, vous devez d’abord appeler **QueryInterface** à l’aide d’un pointeur **IWMPCdrom** pour récupérer l’interface [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) .

L’exemple de code suivant montre comment récupérer une interface pour extraire un CD d’un lecteur spécifique :


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extraction d’un CD**](ripping-a-cd.md)
</dt> <dt>

[**Démarrage du processus RIP**](starting-the-rip-process.md)
</dt> <dt>

[**Récupération de l’État RIP**](retrieving-the-rip-status.md)
</dt> <dt>

[**Sélection d’éléments pour l’extraction**](selecting-items-for-ripping.md)
</dt> <dt>

[**Interface IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




