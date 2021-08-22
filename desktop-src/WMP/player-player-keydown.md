---
title: Player. KeyOut, événement
description: L’événement KeyOut se produit lorsqu’une touche est enfoncée. | Player. KeyOut, événement
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Lecteur Windows Media d’événements keyout
- événement keyout Lecteur Windows Media, classe Player
- classe Player Lecteur Windows Media, keyout, événement
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a067e0125bea6bcabec591d6c1f3ec6fc5a2ee1b0d649a02009690c89d68952e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134772"
---
# <a name="playerkeydown-event"></a>Player. KeyOut, événement

L’événement KeyOut se produit lorsqu’une touche est **enfoncée** .

## <a name="syntax"></a>Syntaxe


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nKeyCode* 
</dt> <dd>

**Nombre** (**int**) spécifiant la touche physique qui est enfoncée. Pour connaître les valeurs possibles, consultez la section Notes.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Nombre** (**int**) spécifiant un champ de bits avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche Ctrl (bit 1) et la touche Alt (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. L’argument Shift indique l’état de ces clés. Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

L’argument *nKeyCode* spécifie une clé physique. Les tableaux suivants indiquent les valeurs possibles pour les clés principales sur un clavier standard.

Valeurs pour les clés principales.



| Clé                     | Valeur   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ÉCHAP                     | 27      |
| Tab                     | 9       |
| VERR. MAJ               | 20      |
| SHIFT (gauche ou droite)   | 16      |
| CTRL (gauche ou droite)    | 17      |
| ALT (gauche ou droite)     | 18      |
| SPACE                   | 32      |
| Ret.arr               | 8       |
| ENTRÉE                   | 13      |
| touche Windows du logo, à gauche  | 91      |
| touche Windows du logo, droite | 92      |
| Clé de l'application         | 93      |



 

Valeurs des touches du pavé numérique.



| Clé               | Valeur  |
|-------------------|--------|
| 0-9               | 96-105 |
| VERR. NUM          | 144    |
| Division (/)        | 111    |
| MULTIPLIER ( \* )     | 106    |
| SOUSTRAIre (-)      | 109    |
| AJOUTER (+)           | 107    |
| SÉPARATEUR (entrée) | 108    |
| DÉCIMAL (.)       | 110    |



 

Valeurs des touches de navigation.



| Clé         | Valeur |
|-------------|-------|
| INSERT      | 45    |
| Suppression      | 46    |
| Origine        | 36    |
| FIN         | 35    |
| Pg. préc     | 33    |
| Pg. suiv   | 34    |
| Flèche haut    | 38    |
| Bas  | 40    |
| Gauche  | 37    |
| Flèche droite | 39    |



 

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

 

 





