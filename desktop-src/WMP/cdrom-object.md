---
title: Objet cdrom
description: L’objet cdrom offre un moyen d’accéder à un CD ou un DVD dans son lecteur.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- objet Cdrom Lecteur Windows Media
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60c4e1081dec3e44107778e45fd911e0c4bb673d27b5e19874508ddbacb270ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342642"
---
# <a name="cdrom-object"></a>Objet cdrom

L’objet **cdrom** offre un moyen d’accéder à un CD ou un DVD dans son lecteur.

L’objet **cdrom** prend en charge les propriétés suivantes.



| Propriété                                   | Description                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | Récupère la lettre du lecteur de CD ou de DVD.                                                                                                                   |
| [playlist](cdrom-playlist.md)             | Récupère un objet de [sélection](playlist-object.md) représentant les pistes sur le CD-ROM actuellement dans le lecteur de CD ou les entrées de titre au niveau de la racine pour le DVD. |



 

L’objet **cdrom** prend en charge la méthode suivante.



| Méthode                   | Description                          |
|--------------------------|--------------------------------------|
| [émission](cdrom-eject.md) | Éjecte le CD ou DVD du lecteur. |



 

L’objet **cdrom** est accessible via la méthode suivante.



| Object                                        | Méthode                           |
|-----------------------------------------------|----------------------------------|
| [CdromCollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

À des fins d’illustration, Player. cdromCollection. Item (*index*) est utilisé dans les sections de syntaxe de référence.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




