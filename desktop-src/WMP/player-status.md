---
title: Player. Status
description: la propriété status récupère une valeur indiquant l’état de Lecteur Windows Media.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Player. status Lecteur Windows Media
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
ms.openlocfilehash: a03ef010bfcb5ee936183724331e97fac5d6f5912d87c5281a55106519c104e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572048"
---
# <a name="playerstatus"></a>Player. Status

la propriété **status** récupère une valeur indiquant l’état de Lecteur Windows Media.

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

 

 





