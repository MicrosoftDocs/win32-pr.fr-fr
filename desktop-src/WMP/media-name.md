---
title: Media.name
description: La propriété Name spécifie ou récupère le nom de l’élément multimédia.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Lecteur Windows Media Media.name
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542629"
---
# <a name="medianame"></a>Media.name

La propriété **Name** spécifie ou récupère le nom de l’élément multimédia.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. **nom**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture contenant le nom de l’élément multimédia.

## <a name="remarks"></a>Notes

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour spécifier la valeur de cette propriété, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Avant d’utiliser cette méthode pour spécifier le nom d’un élément multimédia, utilisez **isReadOnlyItem** pour déterminer si le nom peut être défini.

**Lecteur Windows Media 10 Mobile :** Cette propriété est en lecture seule.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise un *média*. **nom** pour modifier le nom de l’élément multimédia actuel. Un élément d’entrée de texte HTML nommé NameText permet à l’utilisateur d’entrer une chaîne de texte pour le nouveau nom. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
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

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





