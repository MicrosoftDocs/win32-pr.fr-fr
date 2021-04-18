---
title: StringCollection. getItemInfo, méthode
description: La méthode getItemInfo récupère la chaîne correspondant au nom et à l’index d’élément StringCollection spécifiés.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo Player Windows Media, StringCollection Class
- StringCollection, classe Windows Media Player, méthode getItemInfo
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533301"
---
# <a name="stringcollectiongetiteminfo-method"></a>StringCollection. getItemInfo, méthode

La méthode **getItemInfo** récupère la chaîne correspondant au nom et à l’index d’élément **StringCollection** spécifiés.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Number** (**long**) spécifiant l’index de base zéro de l’élément **StringCollection** à partir duquel l’attribut doit être obtenu.

</dd> <dt>

*nom* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une **chaîne** représentant la valeur de l’attribut spécifié. Pour les attributs dont la valeur sous-jacente est **booléenne**, elle retourne la chaîne « true » ou « false ».

## <a name="remarks"></a>Notes

Pour récupérer des attributs avec plusieurs valeurs et attributs avec des valeurs complexes, utilisez la méthode **getItemInfoByType** .

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**StringCollection. getItemInfoByType**](stringcollection-getiteminfobytype.md)
</dt> <dt>

[**StringCollection, objet**](stringcollection-object.md)
</dt> </dl>

 

 





