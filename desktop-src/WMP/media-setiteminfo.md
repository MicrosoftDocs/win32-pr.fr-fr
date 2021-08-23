---
title: Méthode Media. setItemInfo
description: La méthode setItemInfo définit la valeur de l’attribut spécifié pour l’élément multimédia actuel.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- Lecteur Windows Media de la méthode setItemInfo
- méthode setItemInfo Lecteur Windows Media, classe multimédia
- Lecteur Windows Media de classe de média, méthode setItemInfo
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1639b86ce1e0643f3d6ce255e5ca492bc4fae0c1301e1a568a0c5609ceda2a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647969"
---
# <a name="mediasetiteminfo-method"></a>Méthode Media. setItemInfo

La méthode **setItemInfo** définit la valeur de l’attribut spécifié pour l’élément multimédia actuel.

## <a name="syntax"></a>Syntaxe


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attribut* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’attribut. pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md)Lecteur Windows Media.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

**Chaîne** contenant la nouvelle valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La propriété **attributeCount** contient le nombre d’attributs disponibles pour un objet **multimédia** donné. Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer les noms des attributs intégrés qui peuvent être utilisés avec cette méthode.

Avant d’utiliser cette méthode, utilisez la méthode **isReadOnlyItem** pour déterminer si un attribut particulier peut être défini.

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Remarque**

si vous incorporez le contrôle Lecteur Windows Media dans votre application, les attributs de fichier que vous modifiez ne seront pas écrits dans le fichier multimédia numérique tant que l’utilisateur n’aura pas exécuté Lecteur Windows Media. Si vous utilisez le contrôle dans une application distante écrite en C++, les attributs de fichier que vous modifiez seront écrits dans le fichier multimédia numérique peu après que vous avez apporté les modifications. Dans les deux cas, les modifications sont immédiatement disponibles pour votre code via la bibliothèque.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas implémentée.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un *média*. **setItemInfo** pour modifier la valeur de l’attribut genre pour l’élément multimédia actuel. Un élément d’entrée de texte HTML nommé genText permet à l’utilisateur d’entrer une chaîne de texte, qui est ensuite utilisée pour modifier les informations d’attribut. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

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

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. isReadOnlyItem**](media-isreadonlyitem.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





