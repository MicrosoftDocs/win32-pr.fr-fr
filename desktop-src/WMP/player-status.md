---
title: Player. Status
description: La propriété Status récupère une valeur indiquant l’état du lecteur Windows Media.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Lecteur Windows Media Player. Status
topic_type:
- apiref
api_name:
- Player.status
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d54c71e6ab8ece61fb97960bd2956393b1ae584
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539556"
---
# <a name="playerstatus"></a>Player. Status

La propriété **Status** récupère une valeur indiquant l’état du lecteur Windows Media.

## <a name="syntax"></a>Syntaxe

*lecteur* . **État**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une chaîne en lecture seule.

## <a name="remarks"></a>Notes

Les valeurs contenues dans cette propriété sont sujettes à modification à tout moment et doivent être utilisées à des fins d’affichage uniquement.

L’événement **statuschange** est déclenché à chaque modification de la valeur de cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 7,0 ou version ultérieure.<br/>                                      |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Événement Player. StatusChange**](player-player-statuschange.md)
</dt> </dl>

 

 





