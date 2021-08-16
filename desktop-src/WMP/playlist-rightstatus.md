---
title: PLAYLIST. rightStatus
description: L’attribut rightStatus spécifie ou récupère le texte d’état affiché sur le côté droit et le bas de l’élément PLAYLIST.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- PLAYLIST. rightStatus Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29b79b0f4e3ad18ed4e044f894d63ec5059477f80999a8b96dc461d9499b29cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336562"
---
# <a name="playlistrightstatus"></a>PLAYLIST. rightStatus

L’attribut **rightStatus** spécifie ou récupère le texte d’état affiché sur le côté droit et le bas de l’élément **playlist** .

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Cet attribut peut combiner tout texte avec des mots clés spécifiques qui affichent les informations souhaitées, telles que la durée totale de la sélection. Les mots clés sont entourés par des symboles de pourcentage (%) pour les distinguer du texte ordinaire.

Les mots clés suivants peuvent être utilisés.



| Mot clé               | Description                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Nombre d’éléments dans la sélection.                                                                                                                                                                             |
| taille                  | Taille totale de la sélection.                                                                                                                                                                                  |
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

 

 





