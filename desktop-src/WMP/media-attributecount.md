---
title: Media. attributeCount
description: La propriété attributeCount récupère le nombre d’attributs qui peuvent être interrogés et/ou définis pour l’élément multimédia.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media. attributeCount Lecteur Windows Media
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d02e120570140aa7c39a4acc7ce0eb096fffd7bccfc51a6c82d53a7ab5f3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934340"
---
# <a name="mediaattributecount"></a>Media. attributeCount

La propriété **attributeCount** récupère le nombre d’attributs qui peuvent être interrogés et/ou définis pour l’élément multimédia.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. **attributeCount**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Remarques

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md)Lecteur Windows Media.

**Lecteur Windows Media 10 Mobile :** Les attributs d’un élément multimédia sont disponibles uniquement lors de la lecture, sauf s’ils sont récupérés à partir de l’élément via la collection de supports.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un *média*. **attributeCount** pour déterminer le nombre d’attributs disponibles dans l’élément multimédia actuel. Le code utilise cette valeur pour imprimer une liste de noms d’attributs et de valeurs dans une zone de texte HTML, nommée myText. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Media. getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





