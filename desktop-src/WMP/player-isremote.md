---
title: Player. isRemote
description: La propriété isRemote récupère une valeur indiquant si le contrôle du lecteur Windows Media s’exécute en mode distant.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Lecteur Windows Media Player. isRemote
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c8d97ba212e032db16b43299d2a3a8a836f9b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526010"
---
# <a name="playerisremote"></a>Player. isRemote

La propriété **isRemote** récupère une valeur indiquant si le contrôle du lecteur Windows Media s’exécute en mode distant.

## <a name="syntax"></a>Syntaxe

*lecteur* . **isRemote**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture seule.



| Valeur | Description                                   |
|-------|-----------------------------------------------|
| true  | Le contrôle du lecteur s’exécute en mode distant. |
| false | Le contrôle du lecteur s’exécute en mode local.  |



 

## <a name="remarks"></a>Notes

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





