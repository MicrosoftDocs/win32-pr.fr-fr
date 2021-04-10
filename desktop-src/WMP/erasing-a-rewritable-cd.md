---
title: Effacement d’un CD réinscriptible
description: Effacement d’un CD réinscriptible
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Lecteur Windows Media, gravure de CD
- Windows Media Player Object Model, gravage de CD
- modèle d’objet, gravage de CD
- Contrôle ActiveX du lecteur Windows Media, gravure de CD
- Contrôle ActiveX, gravage de CD
- Windows Media Player Mobile contrôle ActiveX, gravure de CD
- Lecteur Windows Media Mobile, gravure de CD
- Gravage de CD, effacement des CD réinscriptibles
- gravure de CD, effacement des CD réinscriptibles
- effacement des CD réinscriptibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030804"
---
# <a name="erasing-a-rewritable-cd"></a>Effacement d’un CD réinscriptible

L’interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) fournit une méthode d’effacement des disques CD-RW. Avant d’effacer un CD-ROM, vous devez d’abord vous assurer que l’opération est prise en charge. Pour plus d’informations, consultez [récupération de l’état du lecteur et du disque](retrieving-the-drive-and-disc-status.md).

Pour commencer à effacer le contenu d’un CD réinscriptible, appelez [IWMPCdromBurn :: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gravure d’un CD**](burning-a-cd.md)
</dt> <dt>

[**Récupération de l’interface de gravure de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Démarrage du processus de gravure**](starting-the-burn-process.md)
</dt> <dt>

[**Récupération de l’état du lecteur et du disque**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Récupération de l’état d’avancement**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




