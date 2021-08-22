---
title: Attribut PLAYERAPPLICATION. hasDisplay
description: l’attribut hasDisplay récupère une valeur indiquant si la vidéo peut s’afficher par le biais du contrôle Lecteur Windows Media distant.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- PLAYERAPPLICATION. hasDisplay Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac144f7e9f96db707944cbb016028578d2446be43a0f06cd0293cb5d56f84c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571942"
---
# <a name="playerapplicationhasdisplay"></a>PLAYERAPPLICATION.hasDisplay

l’attribut **hasDisplay** récupère une valeur indiquant si la vidéo peut s’afficher par le biais du contrôle Lecteur Windows Media distant.

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture seule.



| Valeur | Description               |
|-------|---------------------------|
| True  | La vidéo peut être affichée.    |
| False | La vidéo ne peut pas être affichée. |



 

## <a name="remarks"></a>Notes

cet attribut est utilisé uniquement lors de la communication à distance du contrôle Lecteur Windows Media.

plusieurs contrôles de Lecteur Windows Media peuvent s’exécuter à distance en même temps, mais la vidéo ne peut s’afficher qu’à un seul emplacement à la fois, soit en mode complet du lecteur, soit dans l’un des contrôles distants. Utilisez cette propriété pour déterminer si le contrôle actuel est celui par le biais duquel la vidéo peut être affichée.

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

 

 





