---
title: StringCollection. getItemInfoByType, méthode
description: La méthode getItemInfoByType récupère la valeur correspondant à l’index, au nom, à la langue et à l’index d’attribut de StringCollection spécifiés.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- Lecteur Windows Media de la méthode getItemInfoByType
- getItemInfoByType, méthode Lecteur Windows Media, StringCollection, classe
- StringCollection, classe Lecteur Windows Media, méthode getItemInfoByType
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520932"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>StringCollection. getItemInfoByType, méthode

La méthode **getItemInfoByType** récupère la valeur correspondant à l’index, au nom, à la langue et à l’index d’attribut de **StringCollection** spécifiés.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
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

</dd> <dt>

*attributeIndex* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’index de base zéro de la valeur à récupérer de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un **nombre**, une **chaîne**, un objet **MetadataPicture** ou un objet **MetadataText** comme indiqué dans le tableau suivant.



| Attribut                   | Valeur de retour                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Number** (**unsigned long**) |
| **Synchronisation des WM et des paroles \_** | Objet **MetadataText**        |
| **WM/image**              | Objet **MetadataPicture**     |
| **WM/UserWebURL**           | Objet **MetadataText**        |
| Tous les autres attributs        | String                         |



 

Pour les attributs dont la valeur sous-jacente est **booléenne**, cette méthode retourne la chaîne « true » ou « false ».

## <a name="remarks"></a>Notes

Cette méthode prend en charge des attributs avec plusieurs valeurs et des attributs avec des valeurs complexes. La méthode **getItemInfo** ne prend pas en charge les attributs avec plusieurs valeurs ou des valeurs complexes.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Objet MetadataText**](metadatatext-object.md)
</dt> <dt>

[**StringCollection. getItemInfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**StringCollection, objet**](stringcollection-object.md)
</dt> </dl>

 

 





