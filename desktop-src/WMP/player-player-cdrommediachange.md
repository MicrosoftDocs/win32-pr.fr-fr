---
title: Événement Player. CdromMediaChange
description: L’événement CdromMediaChange se produit lorsqu’un CD ou un DVD est inséré ou éjecté d’un lecteur de CD ou DVD. | Événement Player. CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Lecteur Windows Media d’événements CdromMediaChange
- Lecteur Windows Media d’événements CdromMediaChange, classe Player
- Lecteur Windows Media de classe Player, événement CdromMediaChange
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5e7301c1fb697f4dbbceea2d4dc46af1d884fe4b3e06166b5c24aa43502a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747385"
---
# <a name="playercdrommediachange-event"></a>Événement Player. CdromMediaChange

L’événement **CdromMediaChange** se produit lorsqu’un CD ou un DVD est inséré ou éjecté d’un lecteur de CD ou DVD.

## <a name="syntax"></a>Syntaxe


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CdromNum* 
</dt> <dd>

**Nombre** (**long**) spécifiant l’index du lecteur de CD ou de DVD.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

L’index du lecteur de CD correspond à l’index d’un objet **cdrom** dans le **CdromCollection**.

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet cdrom**](cdrom-object.md)
</dt> <dt>

[**Objet CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





