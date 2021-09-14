---
title: Récupération de l’interface de gravure de CD
description: Récupération de l’interface de gravure de CD
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Lecteur Windows Media, gravage de CD
- modèle d’objet Lecteur Windows Media, gravage de CD
- modèle d’objet, gravage de CD
- contrôle de ActiveX Lecteur Windows Media, gravure de CD
- contrôle de ActiveX, gravure de CD
- Lecteur Windows Media contrôle de ActiveX Mobile, gravage de CD
- Lecteur Windows Media Mobile, gravage de CD
- Gravage de CD, récupération de l’interface IWMPCdromCollection
- gravure de CD, récupération de l’interface IWMPCdromCollection
- Interface IWMPCdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416188"
---
# <a name="retrieving-the-cd-burning-interface"></a>Récupération de l’interface de gravure de CD

Pour énumérer les lecteurs de CD sur l’ordinateur de l’utilisateur, utilisez l’interface **IWMPCdromCollection** . Vous récupérez un pointeur vers cette interface en appelant [IWMPCore :: obtenir \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

En utilisant les méthodes d' **extraction de \_ nombre** et d' **élément** , vous pouvez effectuer une itération de la collection pour récupérer un pointeur d’interface [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) pour chaque lecteur de CD sur l’ordinateur de l’utilisateur.

L’interface **IWMPCdrom** représente un lecteur de CD individuel. Avant de commencer à graver un CD, vous devez d’abord appeler **QueryInterface** à l’aide d’un pointeur **IWMPCdrom** pour récupérer un pointeur vers l’interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) .

L’exemple de code suivant montre comment récupérer une interface pour la gravure d’un CD sur un lecteur spécifique :


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gravure d’un CD**](burning-a-cd.md)
</dt> <dt>

[**Démarrage du processus de gravure**](starting-the-burn-process.md)
</dt> <dt>

[**Effacement d’un CD réinscriptible**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Récupération de l’état du lecteur et du disque**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Récupération de l’état d’avancement**](retrieving-the-burn-status.md)
</dt> <dt>

[**Interface IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




