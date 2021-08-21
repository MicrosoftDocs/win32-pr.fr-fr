---
title: Objet PlayerApplication
description: l’objet PlayerApplication offre un moyen de coordonner le basculement entre un contrôle de Lecteur Windows Media à distance et le mode complet de Lecteur Windows Media.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- objet PlayerApplication Lecteur Windows Media
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46ac009ead54fc4d32b1a302f9228f84484ba6911b353ebb5443653378d9ce61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571830"
---
# <a name="playerapplication-object"></a>Objet PlayerApplication

l’objet **PlayerApplication** offre un moyen de coordonner le basculement entre un contrôle de Lecteur Windows Media à distance et le mode complet de Lecteur Windows Media. Cet objet est utilisé uniquement avec les programmes C++ qui implémentent l’interface **IWMPRemoteMediaServices** et incorporent le contrôle Player en mode distant. les fichiers d’apparence utilisés comme interfaces personnalisées pour le contrôle de Lecteur Windows Media distant accèdent à cet objet dans le code de script via l’attribut global **playerApplication** .

L’objet **PlayerApplication** prend en charge les propriétés suivantes.



| Propriété                                           | Description                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasDisplay](playerapplication-hasdisplay.md)     | récupère une valeur indiquant si la vidéo peut s’afficher par le biais du contrôle de Lecteur Windows Media distant. |
| [playerDocked](playerapplication-playerdocked.md) | récupère une valeur indiquant si Lecteur Windows Media est dans un état ancré.                          |



 

L’objet **PlayerApplication** prend en charge les méthodes suivantes.



| Méthode                                                                       | Description                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [switchToControl](playerapplication-switchtocontrol.md)                     | bascule un contrôle de Lecteur Windows Media distant à l’état d’ancrage.            |
| [switchToPlayerApplication](playerapplication-switchtoplayerapplication.md) | bascule un contrôle de Lecteur Windows Media distant vers le mode complet du lecteur. |



 

L’objet **PlayerApplication** est accessible par le biais de la propriété suivante.



| Object                      | Propriété                                          |
|-----------------------------|---------------------------------------------------|
| [Lecteur](player-object.md) | [playerApplication](player-playerapplication.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




