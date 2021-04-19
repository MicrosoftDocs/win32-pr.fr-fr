---
title: Méthode Media. getAttributeName
description: La méthode getAttributeName récupère le nom de l’attribut correspondant à l’index spécifié.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- méthode getAttributeName lecteur Windows Media
- méthode getAttributeName lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode getAttributeName
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523528"
---
# <a name="mediagetattributename-method"></a>Méthode Media. getAttributeName

La méthode **getAttributeName** récupère le nom de l’attribut correspondant à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’index de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une **chaîne** spécifiant le nom de l’attribut.

## <a name="remarks"></a>Notes

Le nom d’attribut retourné peut être utilisé conjointement avec **getItemInfo** pour récupérer la valeur d’un attribut nommé spécifique.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.

**Lecteur Windows Media 10 Mobile :** Les attributs d’un élément multimédia sont disponibles uniquement lors de la lecture, sauf s’ils sont récupérés à partir de l’élément via la collection de supports.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise un *média*. **getAttributeName** pour remplir une zone de texte html nommée myText avec l’index et le nom de chaque attribut de l’élément multimédia en cours. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





