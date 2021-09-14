---
title: Méthode Media. getMarkerTime
description: La méthode getMarkerTime récupère l’heure du marqueur au niveau de l’index spécifié.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- Lecteur Windows Media de la méthode getMarkerTime
- méthode getMarkerTime Lecteur Windows Media, classe multimédia
- Lecteur Windows Media de classe de média, méthode getMarkerTime
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008410"
---
# <a name="mediagetmarkertime-method"></a>Méthode Media. getMarkerTime

La méthode **getMarkerTime** récupère l’heure du marqueur au niveau de l’index spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*markerNum* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant l’index du marqueur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un **nombre** (**double**) qui spécifie l’emplacement du marqueur, en secondes, à partir du début du clip.

## <a name="remarks"></a>Remarques

Cette méthode retourne la **valeur null** si le marqueur spécifié n’existe pas.

Certains éléments multimédias numériques ne contiennent pas de marqueurs. Utilisez **markerCount** pour déterminer le nombre de marqueurs dans le clip actuel.

Les numéros d’index des marqueurs commencent à 1.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un *média*. **getMarkerTime** pour remplir un élément textarea html nommé MTIMES avec l’emplacement de chaque marqueur. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
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

[**Media. getMarkerName**](media-getmarkername.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





