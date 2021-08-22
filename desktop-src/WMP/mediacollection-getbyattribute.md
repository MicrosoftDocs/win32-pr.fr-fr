---
title: Méthode MediaCollection. getByAttribute
description: La méthode getByAttribute récupère une sélection d’éléments multimédias qui contiennent une valeur spécifiée pour un attribut spécifié.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- Lecteur Windows Media de la méthode getByAttribute
- méthode getByAttribute Lecteur Windows Media, classe MediaCollection
- Lecteur Windows Media de la classe MediaCollection, méthode getByAttribute
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f942f0718202d6c3e509b177c34c4c4be20c058b1e74991fa0ae89955d7711d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996308"
---
# <a name="mediacollectiongetbyattribute-method"></a>Méthode MediaCollection. getByAttribute

La méthode **getByAttribute** récupère une sélection d’éléments multimédias qui contiennent une valeur spécifiée pour un attribut spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attribut* \[ dans\]
</dt> <dd>

**Chaîne** indiquant le nom de l’attribut à rechercher. pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md)Lecteur Windows Media.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

**Chaîne** indiquant la valeur que l’attribut doit avoir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **playlist** .

## <a name="remarks"></a>Remarques

Cette méthode peut être utilisée pour créer une requête générique pour les éléments multimédias qui correspondent à une valeur pour un attribut de la base de données. Cela est utile dans le cas des attributs définis par l’utilisateur. Si l’attribut n’existe pas, une erreur se produit.

Vous pouvez utiliser cette méthode pour récupérer tous les éléments multimédias d’un type spécifique. Utilisez le nom d’attribut « MediaType » et l’une des valeurs suivantes :



| Valeur    | Description                                                |
|----------|------------------------------------------------------------|
| audio    | Musique et d’autres éléments audio uniquement.                          |
| playlist | Sélections représentées en tant qu’objets **multimédias** .                |
| radio    | Éléments de station de radio. non utilisé par Lecteur Windows Media 10.  |
| video    | Éléments vidéo.                                               |
| photos    | Éléments de photo. requiert Lecteur Windows Media 10.             |
| Autres    | Autres éléments, tels que les fichiers ASF ou les URL, pour la diffusion multimédia en continu. |



 

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise *MediaCollection*. **getByAttribute** pour lire tout le contenu de la bibliothèque par l’artiste nommé triode 48. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





