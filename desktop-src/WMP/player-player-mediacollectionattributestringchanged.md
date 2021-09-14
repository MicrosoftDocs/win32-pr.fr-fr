---
title: Événement Player. MediaCollectionAttributeStringChanged
description: L’événement MediaCollectionAttributeStringChanged se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée. | Événement Player. MediaCollectionAttributeStringChanged
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Lecteur Windows Media d’événements MediaCollectionAttributeStringChanged
- Lecteur Windows Media d’événements MediaCollectionAttributeStringChanged, classe Player
- Lecteur Windows Media de classe Player, événement MediaCollectionAttributeStringChanged
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010976"
---
# <a name="playermediacollectionattributestringchanged-event"></a>Événement Player. MediaCollectionAttributeStringChanged

L’événement **MediaCollectionAttributeStringChanged** se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée.

## <a name="syntax"></a>Syntaxe


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Chaîne** spécifiant le nom de l’attribut. pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md)Lecteur Windows Media.

</dd> <dt>

*bstrOldAttribVal* 
</dt> <dd>

**Chaîne** spécifiant l’ancienne valeur de l’attribut.

</dd> <dt>

*bstrNewAttribVal* 
</dt> <dd>

**Chaîne** spécifiant la nouvelle valeur de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Quand un utilisateur modifie des métadonnées de bibliothèque, l’objet **MediaCollection** est mis à jour et cet événement se déclenche pour chaque attribut modifié.

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Player. mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





