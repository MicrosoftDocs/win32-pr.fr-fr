---
title: Objet Media
description: L’objet Media offre un moyen de spécifier ou de récupérer les propriétés d’un élément multimédia, à l’aide des propriétés et méthodes suivantes.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Objet multimédia Windows Media Player
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88eff6ee0a97e63df6a0c073ef18425cbb576e85
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106533550"
---
# <a name="media-object"></a>Objet Media

L’objet **Media** offre un moyen de spécifier ou de récupérer les propriétés d’un élément multimédia, à l’aide des propriétés et méthodes suivantes.

L’objet **multimédia** prend en charge les propriétés suivantes.



| Propriété                                         | Description                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [attributeCount](media-attributecount.md)       | Récupère le nombre d’attributs qui peuvent être interrogés et/ou définis pour l’élément multimédia.              |
| [duration](media-duration.md)                   | Récupère la durée en secondes de l’élément multimédia actuel.                                       |
| [durationString](media-durationstring.md)       | Récupère une valeur de **chaîne** indiquant la durée de l’élément multimédia actuel au format hh : mm : SS. |
| [error](media-error.md)                         | Récupère un objet [ErrorItem](erroritem-object.md) si l’élément multimédia a une condition d’erreur.    |
| [imageSourceHeight](media-imagesourceheight.md) | Récupère, en pixels, la hauteur de l’élément multimédia actuel.                                          |
| [imageSourceWidth](media-imagesourcewidth.md)   | Récupère la largeur de l’élément multimédia actuel en pixels.                                           |
| [markerCount](media-markercount.md)             | Récupère le nombre de marqueurs dans l’élément multimédia.                                                 |
| [name](media-name.md)                           | Spécifie ou récupère le nom de l’élément multimédia.                                                 |
| [sourceURL](media-sourceurl.md)                 | Récupère l’URL de l’élément multimédia.                                                               |



 

L’objet **multimédia** prend en charge les méthodes suivantes.



| Méthode                                                       | Description                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](media-getattributecountbytype.md) | Récupère le nombre d’attributs associés au nom et à la langue de l’attribut spécifiés.            |
| [getAttributeName](media-getattributename.md)               | Récupère le nom de l’attribut correspondant à l’index spécifié.                                |
| [getItemInfo](media-getiteminfo.md)                         | Récupère la valeur de l’attribut spécifié pour l’élément multimédia.                                       |
| [getItemInfoByAtom](media-getiteminfobyatom.md)             | Récupère la valeur de l’attribut avec le numéro d’index spécifié.                                    |
| [getItemInfoByType](media-getiteminfobytype.md)             | Récupère la valeur de l’attribut correspondant au nom de l’attribut, à la langue et à l’index spécifiés. |
| [getMarkerName](media-getmarkername.md)                     | Récupère le nom du marqueur à l’index spécifié.                                                 |
| [getMarkerTime](media-getmarkertime.md)                     | Récupère l’heure du marqueur à l’index spécifié.                                                 |
| [isIdentical](media-isidentical.md)                         | Récupère une valeur indiquant si l’objet fourni est identique à l’objet actuel.                 |
| [isMemberOf](media-ismemberof.md)                           | Récupère une valeur indiquant si l’élément multimédia spécifié est membre de la sélection spécifiée.     |
| [isReadOnlyItem](media-isreadonlyitem.md)                   | Récupère une valeur indiquant si les attributs de l’élément multimédia spécifié peuvent être modifiés.           |
| [setItemInfo](media-setiteminfo.md)                         | Définit la valeur de l’attribut spécifié pour l’élément multimédia.                                            |



 

L’accès à l’objet **multimédia** s’effectue par le biais des propriétés et méthodes suivantes.



| Object                          | Propriété ou méthode                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [Contrôles](controls-object.md) | [currentItem](controls-currentitem.md)                                  |
| [Lecteur](player-object.md)     | [currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md) |
| [Playlist](playlist-object.md) | [item](playlist-item.md)                                                |



 

Parce qu’il s’agit de la méthode d’accès la plus courante, *Player*. **currentMedia** est utilisé à des fins d’illustration dans les sections de syntaxe de référence.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




