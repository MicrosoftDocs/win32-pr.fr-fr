---
title: Player. PositionChange (événement)
description: L’événement PositionChange se produit lorsque la position actuelle de l’élément multimédia a été modifiée.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Lecteur Windows Media d’événements PositionChange
- Lecteur Windows Media d’événements PositionChange, classe Player
- Player, classe Lecteur Windows Media, événement PositionChange
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008361"
---
# <a name="playerpositionchange-event"></a>Player. PositionChange (événement)

L’événement **PositionChange** se produit lorsque la position actuelle de l’élément multimédia a été modifiée.

## <a name="syntax"></a>Syntaxe


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*oldPosition* 
</dt> <dd>

Nombre (**double**) spécifiant l’ancienne position.

</dd> <dt>

*newPosition* 
</dt> <dd>

**Nombre** (**double**) spécifiant la nouvelle position.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cet événement n’est pas déclenché régulièrement pendant la lecture. Il se produit uniquement quand un élément change activement la position actuelle de l’élément multimédia en cours d’exécution, par exemple l’utilisateur qui déplace la poignée de recherche ou le code en spécifiant une valeur pour les *contrôles*. **CurrentPosition**.

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





