---
title: Événement Player. CurrentMediaItemAvailable
description: L’événement CurrentMediaItemAvailable se produit lorsqu’un élément de métadonnées graphiques de l’élément multimédia actuel devient disponible. | Événement Player. CurrentMediaItemAvailable
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Événement CurrentMediaItemAvailable lecteur Windows Media
- Événement CurrentMediaItemAvailable lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement CurrentMediaItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523964"
---
# <a name="playercurrentmediaitemavailable-event"></a>Événement Player. CurrentMediaItemAvailable

L’événement **CurrentMediaItemAvailable** se produit lorsqu’un élément de métadonnées graphiques de l’élément multimédia actuel devient disponible.

## <a name="syntax"></a>Syntaxe


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrItemName* 
</dt> <dd>

**Chaîne** contenant le nom de l’élément multimédia actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Dans la mesure où la lecture peut commencer avant le téléchargement complet d’un élément multimédia, les graphiques de métadonnées contenus dans l’élément multimédia (par exemple, les jaquettes de la couverture de l’album) peuvent ne pas être disponibles au début de la lecture. Cet événement vous avertit à la fin du téléchargement d’un élément de graphique de métadonnées. Vous pouvez ensuite récupérer l’objet **Media** en passant la valeur de *bstrItemName* à *MediaCollection*. méthode **GetByName** , après laquelle vous pouvez accéder à l’élément de graphique de métadonnées à l’aide d’un *média*. **getItemInfoByType** et en spécifiant **WM/image** comme nom d’attribut.

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**MediaCollection.getByName**](mediacollection-getbyname.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





