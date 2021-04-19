---
title: Événement Player. AudioLanguageChange
description: L’événement AudioLanguageChange se produit lorsque le langage audio actuel change. | Événement Player. AudioLanguageChange
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Événement AudioLanguageChange lecteur Windows Media
- Événement AudioLanguageChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement AudioLanguageChange
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542317"
---
# <a name="playeraudiolanguagechange-event"></a>Événement Player. AudioLanguageChange

L’événement **AudioLanguageChange** se produit lorsque le langage audio actuel change.

## <a name="syntax"></a>Syntaxe


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LangID* 
</dt> <dd>

**Nombre** (**long**) spécifiant le nouvel identificateur de paramètres régionaux (LCID).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier Microsoft JScript importé en utilisant le nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





