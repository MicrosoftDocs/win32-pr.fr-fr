---
title: Extraction à l’aide de l’interface IWMPCdromRip
description: Extraction à l’aide de l’interface IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, interface IWMPCdromRip
- extraction de CDs, interface IWMPCdromRip
- Interface IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841909"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Extraction à l’aide de l’interface IWMPCdromRip

Cette section décrit comment utiliser l’interface [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) pour extraire de la musique à partir d’un CD.

L’extraction d’un CD à l’aide de l’interface **IWMPCdromRip** a le même effet que l’extraction de musique à l’aide de l’interface utilisateur du lecteur Windows Media. Le contenu extrait est automatiquement ajouté à la bibliothèque en fonction des préférences de l’utilisateur. Pour plus d’informations sur l’extraction de CD, consultez « extraction de musique à partir de CD » dans l’aide du lecteur Windows Media.

Les exemples de code de cette section utilisent des classes Active Template Library (ATL), telles que **CComPtr**.

## <a name="included-headers"></a>En-têtes inclus

Pour utiliser le code de cette section, incluez les en-têtes suivants :


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a>Pointeurs d’interface

Les interfaces pour le lecteur Windows Media sont stockées dans les variables de membre suivantes.


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



Les sections suivantes décrivent l’utilisation de l’interface IWMPCdromRip

-   [Récupération de l’interface d’extraction](retrieving-the-ripping-interface.md)
-   [Démarrage du processus RIP](starting-the-rip-process.md)
-   [Récupération de l’État RIP](retrieving-the-rip-status.md)
-   [Sélection d’éléments pour l’extraction](selecting-items-for-ripping.md)

 

 




