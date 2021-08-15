---
title: Récupération de l’état du lecteur et du disque
description: Récupération de l’état du lecteur et du disque
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Lecteur Windows Media, gravage de CD
- modèle d’objet Lecteur Windows Media, gravage de CD
- modèle d’objet, gravage de CD
- contrôle de ActiveX Lecteur Windows Media, gravure de CD
- contrôle de ActiveX, gravure de CD
- Lecteur Windows Media contrôle de ActiveX Mobile, gravage de CD
- Lecteur Windows Media Mobile, gravage de CD
- Gravage de CD, récupération de l’état du lecteur et du disque
- gravure de CD, récupération de l’état du lecteur et du disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664315972158b4cf68e7f766f98be095a27d7fa8496f983305cc6baaafe784d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746271"
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

 

 




