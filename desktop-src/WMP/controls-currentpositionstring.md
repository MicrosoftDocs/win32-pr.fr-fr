---
title: Controls. currentPositionString
description: La propriété currentPositionString récupère la position actuelle dans l’élément multimédia sous la forme d’une chaîne au format HH MM SS (heures, minutes et secondes).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- controls. currentPositionString Lecteur Windows Media
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 640f0f97e3fa4c4054df17ea92304ad7721c770d9cb9b56436dcf810b9c083ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651989"
---
# <a name="controlscurrentpositionstring"></a>Controls. currentPositionString

La propriété **currentPositionString** récupère la position actuelle dans l’élément multimédia sous la forme d’une **chaîne** au format hh : mm : SS (heures, minutes et secondes).

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="remarks"></a>Remarques

Si l’élément multimédia a une valeur inférieure à une heure, la partie HH : n’est pas incluse.

> [!Note]  
> Vous devez inclure du code pour arrêter la minuterie lorsque l’élément multimédia est arrêté ou suspendu.

 

## <a name="examples"></a>Exemples

l’exemple de JScript suivant démarre une minuterie HTML qui affiche la position actuelle du fichier multimédia à intervalles d’une seconde. Un élément de texte HTML nommé MyText a été créé pour afficher la position actuelle. L’objet **Player** a été créé avec ID = "Player".


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> </dl>

 

 





