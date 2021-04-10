---
title: Valeurs d’attribut pour le contenu TV
description: Valeurs d’attribut pour le contenu TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Lecteur Windows Media, attributs des éléments multimédias
- Modèle objet du lecteur Windows Media, attributs des éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Windows Media Player Mobile, attributs pour les éléments multimédias
- Contrôle ActiveX du lecteur Windows Media, attributs des éléments multimédias
- Contrôle ActiveX Windows Media Player Mobile, attributs des éléments multimédias
- Contrôle ActiveX, attributs pour les éléments multimédias
- Bibliothèque du lecteur Windows Media, attributs pour les éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, contenu TV
- Valeurs d’attribut de contenu TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029847"
---
# <a name="attribute-values-for-tv-content"></a>Valeurs d’attribut pour le contenu TV

Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Le lecteur Windows Media 10 ou une version ultérieure peut organiser le contenu TV dans la bibliothèque. Le lecteur Windows Media traite le contenu TV comme une sous-catégorie de contenu vidéo. Pour que le contenu vidéo apparaisse dans les nœuds TV de la bibliothèque, définissez les attributs **WM/MediaClassPrimaryID** et **WM/MediaClassSecondaryID** sur les valeurs du tableau suivant à l’aide du *média*. méthode **setItemInfo** :



| Attribut                    | Valeur                                |
|------------------------------|--------------------------------------|
| **WM/MediaClassPrimaryID**   | DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B |
| **WM/MediaClassSecondaryID** | BA7F258A-62F7-47A9-B21F-4651C42A000E |



 

Vous pouvez également utiliser ces valeurs pour déterminer si un élément multimédia numérique particulier contient du contenu TV à l’aide du *média*. **getItemInfo** ou *Media*. méthodes **getItemInfoByType** .

N’oubliez pas d’utiliser les valeurs **GUID** comme valeurs de **chaîne** lors de la spécification ou de la récupération de ces valeurs.

L’exemple de code C# suivant définit les attributs de classe de média pour qu’un élément multimédia soit identifié comme contenu TV.


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



Pour plus d’informations sur les valeurs possibles pour les attributs de classe de média, consultez les [instructions d’utilisation des métadonnées Windows Media](/previous-versions/ms867702(v=msdn.10)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs d’élément multimédia**](media-item-attributes.md)
</dt> <dt>

[**Accès à la bibliothèque**](library-access.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> </dl>

 

 




