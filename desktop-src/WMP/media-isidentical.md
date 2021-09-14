---
title: Méthode Media. isIdentical
description: La méthode isIdentical récupère une valeur indiquant si l’objet fourni est le même que celui actuel. | Méthode Media. isIdentical
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- Lecteur Windows Media de la méthode isIdentical
- méthode isIdentical Lecteur Windows Media, classe multimédia
- Lecteur Windows Media de classe de média, méthode isIdentical
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008404"
---
# <a name="mediaisidentical-method"></a>Méthode Media. isIdentical

La méthode **isIdentical** récupère une valeur indiquant si l’objet fourni est le même que celui actuel.

## <a name="syntax"></a>Syntaxe


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*éléments multimédias* \[ dans\]
</dt> <dd>

Objet **multimédia** à comparer avec l’objet **multimédia** actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne une **valeur booléenne**.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise un *média*. **isIdentical** pour vérifier si un élément multimédia nommé newMedia est le même que l’élément multimédia en cours. Si ce n’est pas le cas, le nouvel élément multimédia est lu. Dans le cas contraire, le média actuel continue de s’exécuter sans interruption. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
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
</dt> </dl>

 

 





