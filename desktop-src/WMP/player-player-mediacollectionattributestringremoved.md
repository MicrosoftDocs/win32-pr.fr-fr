---
title: Événement Player. MediaCollectionAttributeStringRemoved
description: L’événement MediaCollectionAttributeStringRemoved se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque. | Événement Player. MediaCollectionAttributeStringRemoved
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Lecteur Windows Media d’événements MediaCollectionAttributeStringRemoved
- Lecteur Windows Media d’événements MediaCollectionAttributeStringRemoved, classe Player
- Lecteur Windows Media de classe Player, événement MediaCollectionAttributeStringRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b89e46d4dbe86f185fb636b5c8de453e2addbf83c92d1231b5f067ce0b3b1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747405"
---
# <a name="playermediacollectionattributestringremoved-event"></a>Événement Player. MediaCollectionAttributeStringRemoved

L’événement **MediaCollectionAttributeStringRemoved** se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque.

## <a name="syntax"></a>Syntaxe


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Chaîne** spécifiant le nom de l’attribut. pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md)Lecteur Windows Media.

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Chaîne** spécifiant la valeur de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Lorsqu’un élément multimédia est supprimé de la bibliothèque, ses métadonnées sont supprimées de l’objet **MediaCollection** et cet événement est déclenché pour chaque attribut supprimé.

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Player. mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





