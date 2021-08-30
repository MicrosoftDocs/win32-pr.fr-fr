---
title: Démarrage du processus RIP
description: Démarrage du processus RIP
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Lecteur Windows Media, extraction de CD
- modèle d’objet Lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- contrôle de ActiveX Lecteur Windows Media, extraction de CD
- contrôle de ActiveX, extraction de CD
- Lecteur Windows Media contrôle de ActiveX Mobile, extraction de CD
- Lecteur Windows Media Mobile, extraction de CD
- Extraction de CD, démarrage du processus RIP
- extraction de CD, démarrage du processus RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d6d4e7bac4de9fc82f26d7231020e002570553ecdd6447c55f981601e5830a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002159"
---
# <a name="starting-the-rip-process"></a>Démarrage du processus RIP

Après avoir récupéré l’interface d’extraction comme expliqué dans la section précédente, démarrez le processus d’extraction en appelant [IWMPCdromRip :: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



Vous pouvez arrêter l’opération d’extraction en appelant [IWMPCdromRip :: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extraction d’un CD**](ripping-a-cd.md)
</dt> <dt>

[**Récupération de l’interface d’extraction**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Récupération de l’État RIP**](retrieving-the-rip-status.md)
</dt> <dt>

[**Sélection d’éléments pour l’extraction**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




