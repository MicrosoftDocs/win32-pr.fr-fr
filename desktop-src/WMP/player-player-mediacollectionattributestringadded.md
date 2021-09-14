---
title: Événement Player. MediaCollectionAttributeStringAdded
description: L’événement MediaCollectionAttributeStringAdded se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque. | Événement Player. MediaCollectionAttributeStringAdded
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Lecteur Windows Media d’événements MediaCollectionAttributeStringAdded
- Lecteur Windows Media d’événements MediaCollectionAttributeStringAdded, classe Player
- Lecteur Windows Media de classe Player, événement MediaCollectionAttributeStringAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010977"
---
# <a name="playermediacollectionattributestringadded-event"></a>Événement Player. MediaCollectionAttributeStringAdded

L’événement **MediaCollectionAttributeStringAdded** se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque.

## <a name="syntax"></a>Syntaxe


```JScript
Player.MediaCollectionAttributeStringAdded(
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

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Lorsqu’un élément multimédia est ajouté à la bibliothèque, ses métadonnées sont ajoutées à l’objet **MediaCollection** et cet événement est déclenché pour chaque attribut ajouté.

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Spécifications



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

 

 





