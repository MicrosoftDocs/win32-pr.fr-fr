---
title: Récupération de l’état du lecteur et du disque
description: Récupération de l’état du lecteur et du disque
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Lecteur Windows Media, gravure de CD
- Windows Media Player Object Model, gravage de CD
- modèle d’objet, gravage de CD
- Contrôle ActiveX du lecteur Windows Media, gravure de CD
- Contrôle ActiveX, gravage de CD
- Windows Media Player Mobile contrôle ActiveX, gravure de CD
- Lecteur Windows Media Mobile, gravure de CD
- Gravage de CD, récupération de l’état du lecteur et du disque
- gravure de CD, récupération de l’état du lecteur et du disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841910"
---
# <a name="retrieving-the-drive-and-disc-status"></a>Récupération de l’état du lecteur et du disque

Avant de lancer une opération de gravure de CD, vous devez vous assurer que le lecteur de CD-ROM sélectionné prend en charge l’opération que vous souhaitez effectuer. Par exemple, vous devez vérifier qu’un CD peut être effacé avant d’appeler [IWMPCdromBurn :: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase). Le code suivant montre un exemple d’utilisation de [IWMPCdromBurn :: isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) pour déterminer si une opération est prise en charge :


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gravure d’un CD**](burning-a-cd.md)
</dt> <dt>

[**Récupération de l’interface de gravure de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Démarrage du processus de gravure**](starting-the-burn-process.md)
</dt> <dt>

[**Effacement d’un CD réinscriptible**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Récupération de l’état d’avancement**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




