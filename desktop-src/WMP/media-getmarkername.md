---
title: Méthode Media. getMarkerName
description: La méthode getMarkerName récupère le nom du marqueur à l’index spécifié.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- Lecteur Windows Media de la méthode getMarkerName
- méthode getMarkerName Lecteur Windows Media, classe multimédia
- Lecteur Windows Media de classe de média, méthode getMarkerName
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008411"
---
# <a name="mediagetmarkername-method"></a>Méthode Media. getMarkerName

La méthode **getMarkerName** récupère le nom du marqueur à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*markerNum* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant un index de marqueur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne une **chaîne**.

## <a name="remarks"></a>Remarques

Cette méthode retourne la **valeur null** si le marqueur spécifié n’existe pas.

Certains éléments multimédias numériques ne contiennent pas de marqueurs. Utilisez **markerCount** pour déterminer le nombre de marqueurs dans le clip actuel.

Les numéros d’index des marqueurs commencent à 1.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un *média*. **getMarkerName** pour remplir un élément textarea html nommé MNAMES avec les noms des marqueurs dans l’élément multimédia actuel. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
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

[**Media. getMarkerTime**](media-getmarkertime.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





