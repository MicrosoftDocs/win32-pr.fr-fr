---
title: Démarrage du processus RIP
description: Démarrage du processus RIP
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, démarrage du processus RIP
- extraction de CD, démarrage du processus RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106512714"
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

 

 




