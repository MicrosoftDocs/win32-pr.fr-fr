---
title: PLAYLIST. leftStatus
description: L’attribut leftStatus spécifie ou récupère le texte d’état affiché sur le côté gauche et le bas de l’élément PLAYLIST.
ms.assetid: c83f4fd1-d0e6-4822-9208-8e968c409a78
keywords:
- Lecteur Windows Media PLAYLIST. leftStatus
topic_type:
- apiref
api_name:
- PLAYLIST.leftStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33d4c3d235a7bba67219378063cb9811601e68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540265"
---
# <a name="playlistleftstatus"></a>PLAYLIST. leftStatus

L’attribut **leftStatus** spécifie ou récupère le texte d’état affiché sur le côté gauche et le bas de l’élément **playlist** .

``` syntax
        elementID.leftStatus
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Cet attribut peut combiner tout texte avec des mots clés spécifiques qui affichent les informations souhaitées, telles que la durée totale de la sélection. Les mots clés sont entourés de symboles de pourcentage (%) pour les distinguer du texte ordinaire.

Les mots clés suivants peuvent être utilisés.



| Mot clé               | Description                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Nombre d’éléments dans la sélection.                                                                                                                                                                             |
| est                  | Taille totale de la sélection.                                                                                                                                                                                  |
| duration              | Durée totale de la sélection.                                                                                                                                                                              |
| *INCONNU*                 | Effectue un **getItemInfo** sur la playlist avec *xxx* qui est l’élément à recevoir.                                                                                                                                 |
| SelectedSize          | Taille totale des entrées sélectionnées dans la sélection.                                                                                                                                                          |
| SelectedCount         | Nombre total d’entrées sélectionnées dans la sélection.                                                                                                                                                            |
| SelectedDuration      | Durée totale des entrées sélectionnées dans la sélection.                                                                                                                                                      |
| CheckedCount          | Nombre total de pistes activées dans la sélection.                                                                                                                                                              |
| CheckedDuration       | Durée totale des pistes cochées dans la sélection.                                                                                                                                                        |
| CheckedSize           | Taille totale des pistes cochées dans la sélection.                                                                                                                                                            |
| DurationString        | Affiche du texte qui décrit la durée sous la forme « temps total » ou « temps estimé », selon que les valeurs totales sont connues ou non. Ce texte est suivi de « % Duration% ».                                       |
| CheckedDurationString | Affiche le texte qui décrit la durée de tous les éléments activés dans la liste de lecture en tant que « durée totale » ou « durée estimée », selon que les valeurs totales sont connues ou non. Ce texte est suivi de « % Duration% ». |



 

La valeur « temps total :% Duration% » pour une sélection qui contient une durée totale de sept minutes affiche « temps total : 07:00 ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





