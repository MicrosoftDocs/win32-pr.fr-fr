---
title: Media. imageSourceWidth
description: La propriété imageSourceWidth récupère la largeur de l’élément multimédia actuel en pixels.
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- Media. imageSourceWidth Lecteur Windows Media
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2a3fef7b74a3d033b058f0afd1f6eece007bd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008406"
---
# <a name="mediaimagesourcewidth"></a>Media. imageSourceWidth

La propriété **imageSourceWidth** récupère la largeur de l’élément multimédia actuel en pixels.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. **imageSourceWidth**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

Si l’élément multimédia n’est pas celui en cours, cette propriété retourne la valeur zéro.

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un *média*. **imageSourceWidth** pour afficher la taille de l’image, en pixels, de l' **élément multimédia actuel. Les informations sont imprimées dans un élément TEXTAREA HTML nommé Videote. L’objet Player** a été créé avec ID = "Player".


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

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

 

 





