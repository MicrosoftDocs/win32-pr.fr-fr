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
ms.openlocfilehash: e4a1102d49064c602d04915f77eda7ecfa1c748d4aea000cef1271679da1ec62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054357"
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

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

## <a name="requirements"></a>Configuration requise



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

 

 





