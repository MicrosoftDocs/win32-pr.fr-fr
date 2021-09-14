---
title: Événement Player. ModeChange
description: l’événement ModeChange se produit lorsqu’un mode de Lecteur Windows Media est modifié. | Événement Player. ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Lecteur Windows Media d’événements ModeChange
- Lecteur Windows Media d’événements ModeChange, classe Player
- Lecteur Windows Media de classe Player, événement ModeChange
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010965"
---
# <a name="playermodechange-event"></a>Événement Player. ModeChange

l’événement **ModeChange** se produit lorsqu’un mode de Lecteur Windows Media est modifié.

## <a name="syntax"></a>Syntaxe


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ModeName* 
</dt> <dd>

**Chaîne** indiquant le mode qui a été modifié. Contient l'une des valeurs suivantes :



| Valeur   | Description                                         |
|---------|-----------------------------------------------------|
| lecture aléatoire | Les pistes sont lues dans un ordre aléatoire.                  |
| loop    | L’intégralité de la séquence de pistes est lue à plusieurs reprises. |



 

</dd> <dt>

*NewValue* 
</dt> <dd>

**Valeur booléenne** indiquant le nouvel État du mode spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Paramètres. getMode**](settings-getmode.md)
</dt> <dt>

[**Paramètres. setMode**](settings-setmode.md)
</dt> </dl>

 

 





