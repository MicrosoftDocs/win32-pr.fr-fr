---
title: Gravure d’un CD
description: Gravure d’un CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Lecteur Windows Media, gravure de CD
- Windows Media Player Object Model, gravage de CD
- modèle d’objet, gravage de CD
- Contrôle ActiveX du lecteur Windows Media, gravure de CD
- Contrôle ActiveX, gravage de CD
- Windows Media Player Mobile contrôle ActiveX, gravure de CD
- Lecteur Windows Media Mobile, gravure de CD
- Gravage de CD, à propos de
- gravure de CD, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101273"
---
# <a name="burning-a-cd"></a>Gravure d’un CD

Cette section décrit comment utiliser l’interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) pour graver de la musique sur un CD. L’interface **IWMPCdromBurn** fournit des fonctionnalités permettant de graver des playlists sur des CD comme des pistes audio ou des données, ainsi que d’effacer CD-RWS.

Utilisation du code

Les exemples de code de cette section utilisent des classes Active Template Library (ATL), telles que **CComPtr**.

En-têtes inclus

Pour utiliser le code de cette section, incluez les en-têtes suivants :


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



Pointeurs d’interface

Les interfaces pour le lecteur Windows Media sont stockées dans les variables membres suivantes :


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



Les rubriques suivantes décrivent comment utiliser l’API de gravage de CD.

-   [Récupération de l’interface de gravure de CD](retrieving-the-cd-burning-interface.md)
-   [Démarrage du processus de gravure](starting-the-burn-process.md)
-   [Effacement d’un CD réinscriptible](erasing-a-rewritable-cd.md)
-   [Récupération de l’état du lecteur et du disque](retrieving-the-drive-and-disc-status.md)
-   [Récupération de l’état d’avancement](retrieving-the-burn-status.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de contrôle du lecteur**](player-control-guide.md)
</dt> </dl>

 

 




