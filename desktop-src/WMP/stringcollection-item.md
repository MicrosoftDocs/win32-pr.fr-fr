---
title: StringCollection. Item, méthode
description: La méthode Item récupère la chaîne à l’index spécifié.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- méthode item Lecteur Windows Media
- item, méthode Lecteur Windows Media, StringCollection, classe
- StringCollection, classe Lecteur Windows Media, méthode item
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a7ab868a1b8814b3ea67d0c37988e492ed2576758d7e8e68a7dbfa997c16b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832312"
---
# <a name="stringcollectionitem-method"></a>StringCollection. Item, méthode

La méthode **Item** récupère la chaîne à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’index.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une **chaîne**.

## <a name="remarks"></a>Remarques

L’objet **StringCollection** est utilisé pour récupérer l’ensemble de valeurs disponibles pour un attribut. Par exemple, *MediaCollection*. la méthode **getAttributeStringCollection** peut être utilisée pour récupérer un objet **StringCollection** représentant toutes les valeurs de l’attribut genre dans le type de média audio. La propriété **Item** peut ensuite être utilisée pour itérer au sein de toutes les valeurs possibles de l’attribut genre.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MediaCollection.getAttributeStringCollection**](mediacollection-getattributestringcollection.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection, objet**](stringcollection-object.md)
</dt> </dl>

 

 





