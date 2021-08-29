---
title: Player. KeyUp (événement)
description: L’événement KeyUp se produit lorsqu’une touche est relâchée. | Player. KeyUp (événement)
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- événement KeyUp Lecteur Windows Media
- événement KeyUp Lecteur Windows Media, classe Player
- Lecteur Windows Media de classe Player, événement KeyUp
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46134b675f06e0d9febcfa29ec31f8939aac606028342cd829e92e757465c49a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134783"
---
# <a name="playerkeyup-event"></a>Player. KeyUp (événement)

L’événement **KeyUp** se produit lorsqu’une touche est relâchée.

## <a name="syntax"></a>Syntaxe


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nKeyCode* 
</dt> <dd>

**Nombre** (**int**) spécifiant la touche physique qui est enfoncée. Pour connaître les valeurs possibles, consultez [événement Player.](player-player-keydown.md)KeyOut.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Nombre** (**int**) spécifiant un champ de bits avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche Ctrl (bit 1) et la touche Alt (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. L’argument Shift indique l’état de ces clés. Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





