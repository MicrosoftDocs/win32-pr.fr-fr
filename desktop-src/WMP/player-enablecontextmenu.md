---
title: Player. enableContextMenu
description: La propriété enableContextMenu spécifie ou récupère une valeur indiquant s’il faut activer le menu contextuel qui apparaît lorsque l’utilisateur clique sur le bouton droit de la souris.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Lecteur Windows Media Player. enableContextMenu
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192700"
---
# <a name="playerenablecontextmenu"></a>Player. enableContextMenu

La propriété **enableContextMenu** spécifie ou récupère une valeur indiquant s’il faut activer le menu contextuel qui apparaît lorsque l’utilisateur clique sur le bouton droit de la souris.

## <a name="syntax"></a>Syntaxe

*lecteur*. **enableContextMenu**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une valeur booléenne en lecture/écriture.



| Valeur | Description                       |
|-------|-----------------------------------|
| true  | Par défaut. Activez le menu contextuel. |
| false | N’activez pas le menu contextuel.   |



 

## <a name="remarks"></a>Notes

pendant la lecture en plein écran, Lecteur Windows Media masque le curseur de la souris quand **enableContextMenu** est égal à false et **uiMode** est égal à « none ».

**Lecteur Windows Media 10 Mobile :** Cette propriété n’est pas prise en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





