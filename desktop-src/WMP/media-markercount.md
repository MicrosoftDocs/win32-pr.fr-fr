---
title: Media. markerCount
description: La propriété markerCount récupère le nombre de marqueurs dans l’élément multimédia.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media. markerCount Lecteur Windows Media
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00206991f81c6a445648a063a37bcc45bf91f647b60317772478142eefd1b20e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123349"
---
# <a name="mediamarkercount"></a>Media. markerCount

La propriété **markerCount** récupère le nombre de marqueurs dans l’élément multimédia.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. **markerCount**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**) qui spécifie le nombre de marqueurs dans le fichier.

## <a name="remarks"></a>Remarques

Cette propriété retourne la valeur zéro si un fichier n’a pas de marqueurs, ou si l’élément multimédia n’est pas le même que le *joueur*. **currentMedia**.

Les numéros des marqueurs commencent à 1.

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un *média*. **markerCount** pour récupérer le nombre de marqueurs dans l’élément multimédia actuel. Cette valeur est ensuite utilisée comme limite supérieure pour une structure de bouclage, qui itère au sein de la liste des marqueurs pour récupérer chaque nom de marqueur. Un élément TEXTAREA HTML nommé MNAMES affiche les noms des marqueurs dans l’élément multimédia en cours. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
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

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





