---
title: Controls. currentPositionTimecode
description: La propriété currentPositionTimecode spécifie ou récupère la position actuelle dans l’élément multimédia actuel à l’aide d’un format de code d’heure. Cette propriété prend actuellement en charge le code de temps SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Controls. currentPositionTimecode Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528779"
---
# <a name="controlscurrentpositiontimecode"></a>Controls. currentPositionTimecode

La propriété **currentPositionTimecode** spécifie ou récupère la position actuelle dans l’élément multimédia actuel à l’aide d’un format de code d’heure. Cette propriété prend actuellement en charge le code de temps SMPTE.

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Le code temporel SMPTE offre un moyen standard d’identifier une image vidéo individuelle, ce qui est utile pour synchroniser la lecture. Si un fichier multimédia numérique prend en charge le code temporel SMPTE, le lecteur Windows Media peut récupérer les informations de position du code en temps courant ou rechercher une image vidéo identifiée par une **chaîne** de code d’heure particulière.

Le code temporel SMPTE identifie une trame particulière en fonction du nombre d’heures, de minutes, de secondes et de frames qui le séparent d’une trame de référence particulière. En règle générale, la trame de temps zéro est le début du fichier et une valeur de code temporel SMPTE particulière représente le temps écoulé depuis le début du fichier.

La **chaîne** de code d’heure est au \[ *format* \] *hh*:*mm*:*SS*.*FF* où \[ *Range* \] représente la plage, *hh* représente les heures, *mm* représente les minutes, *SS* représente les secondes et *FF* représente les images. Lorsque vous spécifiez une valeur à l’aide de **currentPositionTimecode**, vous devez inclure les huit chiffres en utilisant des zéros comme espaces réservés.

Le \[  \] spécificateur de plage correspond au membre **wRange** de la structure de données d' **\_ extension du \_ \_ code temporel WMT** Windows Media format. Pour plus d’informations sur les plages de codes de temps, consultez le kit de développement logiciel (SDK) Windows Media format.

La spécification et la récupération de **currentPositionTimecode** sont prises en charge uniquement pour les fichiers qui contiennent des informations de code de temps SMPTE.

## <a name="examples"></a>Exemples

L’exemple de code suivant spécifie **currentPositionTimecode** comme 1 heure, zéro minute, 30 secondes et 5 frames. L’objet **Player** a été créé avec ID = "Player".


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> </dl>

 

 





