---
title: Événement Player. AudioLanguageChange
description: L’événement AudioLanguageChange se produit lorsque le langage audio actuel change. | Événement Player. AudioLanguageChange
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Lecteur Windows Media d’événements AudioLanguageChange
- Lecteur Windows Media d’événements AudioLanguageChange, classe Player
- Lecteur Windows Media de classe Player, événement AudioLanguageChange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403995"
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

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Un LCID identifie de façon unique un dialecte de langage particulier, appelé paramètres régionaux.

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou transmise à une méthode dans un fichier de JScript Microsoft importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Spécifications



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

 

 





