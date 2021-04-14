---
title: Objet cdrom
description: L’objet cdrom offre un moyen d’accéder à un CD ou un DVD dans son lecteur.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Objet cdrom lecteur Windows Media
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104311923"
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

 

 




