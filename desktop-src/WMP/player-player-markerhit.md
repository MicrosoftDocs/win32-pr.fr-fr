---
title: Événement Player. MarkerHit
description: L’événement MarkerHit se produit lorsqu’un marqueur est atteint. | Événement Player. MarkerHit
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Événement MarkerHit lecteur Windows Media
- Événement MarkerHit lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MarkerHit
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532212"
---
# <a name="playermarkerhit-event"></a>Événement Player. MarkerHit

L’événement **MarkerHit** se produit lorsqu’un marqueur est atteint.

## <a name="syntax"></a>Syntaxe


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MarkerNum* 
</dt> <dd>

**Nombre** (**long**) indiquant le numéro du marqueur qui a été atteint.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





