---
title: Attribut PLAYERAPPLICATION. hasDisplay
description: L’attribut hasDisplay récupère une valeur indiquant si la vidéo peut s’afficher via le contrôle du lecteur Windows Media distant.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- Lecteur Windows Media PLAYERAPPLICATION. hasDisplay
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533030"
---
# <a name="playerapplicationhasdisplay"></a>PLAYERAPPLICATION.hasDisplay

L’attribut **hasDisplay** récupère une valeur indiquant si la vidéo peut s’afficher via le contrôle du lecteur Windows Media distant.

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture seule.



| Valeur | Description               |
|-------|---------------------------|
| True  | La vidéo peut être affichée.    |
| Faux | La vidéo ne peut pas être affichée. |



 

## <a name="remarks"></a>Notes

Cet attribut est utilisé uniquement lors de la communication à distance du contrôle du lecteur Windows Media.

Plusieurs contrôles de lecteur Windows Media peuvent s’exécuter à distance en même temps, mais la vidéo ne peut s’afficher qu’à un seul emplacement à la fois, soit en mode complet du lecteur, soit dans l’un des contrôles distants. Utilisez cette propriété pour déterminer si le contrôle actuel est celui par le biais duquel la vidéo peut être affichée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYERAPPLICATION**](playerapplication-element.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





