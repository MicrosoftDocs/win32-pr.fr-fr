---
title: StringCollection. getAttributeCountByType, méthode
description: La méthode getAttributeCountByType récupère le nombre d’attributs associés à l’index d’élément StringCollection, le nom d’attribut et la langue spécifiés.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- Lecteur Windows Media de la méthode getAttributeCountByType
- getAttributeCountByType, méthode Lecteur Windows Media, StringCollection, classe
- StringCollection, classe Lecteur Windows Media, méthode getAttributeCountByType
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520937"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>StringCollection. getAttributeCountByType, méthode

La méthode **getAttributeCountByType** récupère le nombre d’attributs associés à l’index d’élément **StringCollection** , le nom d’attribut et la langue spécifiés.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
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

</dd> <dt>

*langue* \[ dans\]
</dt> <dd>

**Chaîne** contenant le langage. Si la valeur est définie sur null ou sur la chaîne vide (""), la chaîne de paramètres régionaux active est utilisée. Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un **nombre** (**long**).

## <a name="remarks"></a>Notes

Cette méthode est utilisée pour déterminer le nombre d’attributs correspondant à un nom d’attribut particulier pour un élément **StringCollection** particulier. Les numéros d’index peuvent ensuite être passés au quatrième paramètre de la méthode **StringCollection. getItemInfoByType** .

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**StringCollection, objet**](stringcollection-object.md)
</dt> </dl>

 

 





