---
title: Valeurs d’attribut pour le contenu TV
description: Valeurs d’attribut pour le contenu TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Lecteur Windows Media, attributs pour les éléments multimédias
- Lecteur Windows Media modèle objet, attributs pour les éléments multimédias
- modèle objet, attributs pour les éléments multimédias
- Lecteur Windows Media Mobile, attributs pour les éléments multimédias
- Lecteur Windows Media ActiveX contrôle, attributs pour les éléments multimédias
- Lecteur Windows Media contrôle de ActiveX Mobile, attributs pour les éléments multimédias
- contrôle ActiveX, attributs pour les éléments multimédias
- bibliothèque de Lecteur Windows Media, attributs des éléments multimédias
- bibliothèque, attributs pour les éléments multimédias
- attributs, contenu TV
- Valeurs d’attribut de contenu TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa96f855d90fe0b65c4e9483dcb2ba4ae3ff7be049f1346f1038097789b2126c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583030"
---
# <a name="attribute-values-for-tv-content"></a>Valeurs d’attribut pour le contenu TV

Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Lecteur Windows Media 10 ou une version ultérieure peut organiser le contenu TV dans la bibliothèque. Lecteur Windows Media traite le contenu TV comme une sous-catégorie de contenu vidéo. Pour que le contenu vidéo apparaisse dans les nœuds TV de la bibliothèque, définissez les attributs **WM/MediaClassPrimaryID** et **WM/MediaClassSecondaryID** sur les valeurs du tableau suivant à l’aide du *média*. méthode **setItemInfo** :



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



pour plus d’informations sur les valeurs possibles pour les attributs de classe de média, consultez les [instructions d’utilisation des métadonnées de média Windows](/previous-versions/ms867702(v=msdn.10)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs d’élément multimédia**](media-item-attributes.md)
</dt> <dt>

[**Accès à la bibliothèque**](library-access.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> </dl>

 

 




