---
title: Événement Player. Click
description: L’événement Click se produit lorsque l’utilisateur clique sur un bouton de la souris.
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- Lecteur Windows Media d’événements de clic
- Lecteur Windows Media d’événements click, classe Player
- Lecteur Windows Media de classe Player, événement click
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8389460d59018b221749719d32edbaa89943808
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292542"
---
# <a name="playerclick-event"></a>Événement Player. Click

L’événement **Click** se produit lorsque l’utilisateur clique sur un bouton de la souris.

## <a name="syntax"></a>Syntaxe


```JScript
Player.Click(
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

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





