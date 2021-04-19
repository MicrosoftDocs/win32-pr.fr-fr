---
title: Événement Player. MediaCollectionAttributeStringRemoved
description: L’événement MediaCollectionAttributeStringRemoved se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque. | Événement Player. MediaCollectionAttributeStringRemoved
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Événement MediaCollectionAttributeStringRemoved lecteur Windows Media
- Événement MediaCollectionAttributeStringRemoved lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaCollectionAttributeStringRemoved
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
ms.openlocfilehash: b1b85dfd566c507f6ae5557134ac95544e42d688
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527979"
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

**Chaîne** spécifiant le nom de l’attribut. Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Chaîne** spécifiant la valeur de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Lorsqu’un élément multimédia est supprimé de la bibliothèque, ses métadonnées sont supprimées de l’objet **MediaCollection** et cet événement est déclenché pour chaque attribut supprimé.

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

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

 

 





