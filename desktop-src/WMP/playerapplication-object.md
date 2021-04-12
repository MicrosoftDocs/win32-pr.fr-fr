---
title: Objet PlayerApplication
description: L’objet PlayerApplication permet de coordonner le basculement entre un contrôle du lecteur Windows Media distant et le mode complet du lecteur Windows Media.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Objet PlayerApplication lecteur Windows Media
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313243"
---
# <a name="playerapplication-object"></a>Objet PlayerApplication

L’objet **PlayerApplication** permet de coordonner le basculement entre un contrôle du lecteur Windows Media distant et le mode complet du lecteur Windows Media. Cet objet est utilisé uniquement avec les programmes C++ qui implémentent l’interface **IWMPRemoteMediaServices** et incorporent le contrôle Player en mode distant. Les fichiers d’apparence utilisés comme interfaces personnalisées pour le contrôle du lecteur Windows Media distant accèdent à cet objet dans le code de script via l’attribut global **playerApplication** .

L’objet **PlayerApplication** prend en charge les propriétés suivantes.



| Propriété                                           | Description                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasDisplay](playerapplication-hasdisplay.md)     | Récupère une valeur indiquant si la vidéo peut s’afficher via le contrôle du lecteur Windows Media distant. |
| [playerDocked](playerapplication-playerdocked.md) | Récupère une valeur indiquant si le lecteur Windows Media est dans un état d’ancrage.                          |



 

L’objet **PlayerApplication** prend en charge les méthodes suivantes.



| Méthode                                                                       | Description                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [switchToControl](playerapplication-switchtocontrol.md)                     | Bascule un contrôle du lecteur Windows Media distant vers l’état d’ancrage.            |
| [switchToPlayerApplication](playerapplication-switchtoplayerapplication.md) | Bascule un contrôle du lecteur Windows Media distant vers le mode complet du lecteur. |



 

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

 

 




