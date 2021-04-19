---
title: Méthode Media. setItemInfo
description: La méthode setItemInfo définit la valeur de l’attribut spécifié pour l’élément multimédia actuel.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- méthode setItemInfo lecteur Windows Media
- méthode setItemInfo lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode setItemInfo
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
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535297"
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

**Chaîne** contenant le nom de l’attribut. Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

**Chaîne** contenant la nouvelle valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La propriété **attributeCount** contient le nombre d’attributs disponibles pour un objet **multimédia** donné. Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer les noms des attributs intégrés qui peuvent être utilisés avec cette méthode.

Avant d’utiliser cette méthode, utilisez la méthode **isReadOnlyItem** pour déterminer si un attribut particulier peut être défini.

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Remarque**

Si vous incorporez le contrôle du lecteur Windows Media dans votre application, les attributs de fichier que vous modifiez ne seront pas écrits dans le fichier multimédia numérique tant que l’utilisateur n’aura pas exécuté le lecteur Windows Media. Si vous utilisez le contrôle dans une application distante écrite en C++, les attributs de fichier que vous modifiez seront écrits dans le fichier multimédia numérique peu après que vous avez apporté les modifications. Dans les deux cas, les modifications sont immédiatement disponibles pour votre code via la bibliothèque.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas implémentée.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise un *média*. **setItemInfo** pour modifier la valeur de l’attribut genre pour l’élément multimédia actuel. Un élément d’entrée de texte HTML nommé genText permet à l’utilisateur d’entrer une chaîne de texte, qui est ensuite utilisée pour modifier les informations d’attribut. L’objet **Player** a été créé avec ID = "Player".


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

 

 





