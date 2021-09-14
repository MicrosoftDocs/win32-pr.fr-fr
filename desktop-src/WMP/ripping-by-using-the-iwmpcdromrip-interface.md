---
title: Extraction à l’aide de l’interface IWMPCdromRip
description: Extraction à l’aide de l’interface IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
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
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416179"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Extraction à l’aide de l’interface IWMPCdromRip

Cette section décrit comment utiliser l’interface [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) pour extraire de la musique à partir d’un CD.

l’extraction d’un CD à l’aide de l’interface **IWMPCdromRip** a le même effet que l’extraction de musique à l’aide de l’interface utilisateur Lecteur Windows Media. Le contenu extrait est automatiquement ajouté à la bibliothèque en fonction des préférences de l’utilisateur. pour plus d’informations sur l’extraction de cd, consultez « extraction de musique à partir de cd » dans l’aide de Lecteur Windows Media.

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

les interfaces pour Lecteur Windows Media sont stockées dans les variables membres suivantes.


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

 

 




