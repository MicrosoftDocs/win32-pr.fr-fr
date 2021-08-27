---
title: Méthode Media. isReadOnlyItem
description: La méthode isReadOnlyItem retourne une valeur indiquant si l’attribut spécifié de l’élément multimédia peut être modifié.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- Lecteur Windows Media de la méthode isReadOnlyItem
- méthode isReadOnlyItem Lecteur Windows Media, classe multimédia
- Lecteur Windows Media de classe de média, méthode isReadOnlyItem
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 501aacb7b9a56fd9780aba75a15aa9f717640ebff7619df020bad432cdffd459
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123389"
---
# <a name="mediaisreadonlyitem-method"></a>Méthode Media. isReadOnlyItem

La méthode **isReadOnlyItem** retourne une valeur indiquant si l’attribut spécifié de l’élément multimédia peut être modifié.

## <a name="syntax"></a>Syntaxe


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attribut* \[ dans\]
</dt> <dd>

**Chaîne** indiquant le nom de l’attribut à tester. pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md)Lecteur Windows Media.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une **valeur booléenne**.

## <a name="remarks"></a>Remarques

Si un attribut est en lecture seule, il ne peut pas être défini à l’aide de la méthode **setItemInfo** . notez que cette méthode peut retourner des valeurs différentes pour un attribut particulier lorsqu’elle est utilisée avec différentes versions de Lecteur Windows Media.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours **true**.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un *média*. **isReadOnlyItem** pour remplir un élément textarea html nommé rwText avec des informations sur l’élément multimédia actuel. Le code génère chaque attribut de l’élément multimédia en cours, ainsi que le texte indiquant si l’attribut est en lecture seule ou en lecture/écriture. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
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

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





