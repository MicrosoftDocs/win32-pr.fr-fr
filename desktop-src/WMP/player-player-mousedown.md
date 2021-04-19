---
title: Player. MouseDown (événement)
description: L’événement MouseDown se produit lorsque l’utilisateur appuie sur un bouton de la souris. | Player. MouseDown (événement)
ms.assetid: cc2fd2ca-c974-4683-98ca-2202c4d5b240
keywords:
- Événement MouseDown lecteur Windows Media
- Événement MouseDown lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, événement MouseDown
topic_type:
- apiref
api_name:
- Player.MouseDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29eb0c8aa5f6731f94d0e4c3b4ff967cb7819f42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523616"
---
# <a name="playermousedown-event"></a>Player. MouseDown (événement)

L’événement **MouseDown** se produit lorsque l’utilisateur appuie sur un bouton de la souris.

## <a name="syntax"></a>Syntaxe


```JScript
Player.MouseDown(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nbouton* 
</dt> <dd>

**Nombre** (**int**) spécifiant un champ de bits avec bits correspondant au bouton gauche (bit 0), bouton droit (bit 1) et bouton central (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Nombre** (**int**) spécifiant un champ de bits avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche Ctrl (bit 1) et la touche Alt (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. L’argument Shift indique l’état de ces clés. Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.

</dd> <dt>

*Rotation* 
</dt> <dd>

**Nombre** (**long**) spécifiant la coordonnée x du pointeur de la souris par rapport au coin supérieur gauche du contrôle.

</dd> <dt>

*Années* 
</dt> <dd>

**Nombre** (**long**) spécifiant la coordonnée y du pointeur de la souris par rapport au coin supérieur gauche du contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

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

 

 





