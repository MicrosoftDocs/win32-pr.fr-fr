---
title: Settings. getMode, méthode
description: La méthode getMode détermine si le mode de boucle ou le mode de lecture aléatoire est actif.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- méthode getMode lecteur Windows Media
- méthode getMode lecteur Windows Media, classe de paramètres
- Classe de paramètres lecteur Windows Media, méthode getMode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520894"
---
# <a name="settingsgetmode-method"></a>Settings. getMode, méthode

La méthode **getMode** détermine si le mode de boucle ou le mode de lecture aléatoire est actif.

## <a name="syntax"></a>Syntaxe


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*modeName* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant le nom du mode en question, contenant l’une des valeurs suivantes.



| String     | Description                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| autoRewind | Les suivis sont redémarrés au début après avoir été lus jusqu’à la fin.                                                          |
| loop       | La séquence de suivi se répète lui-même.                                                                                   |
| showFrame  | L’image clé la plus proche s’affiche à la position actuelle lorsqu’elle n’est pas lue. Ce mode n’est pas pertinent pour les pistes audio. |
| lecture aléatoire    | Les pistes sont lues dans un ordre aléatoire.                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une valeur **booléenne** indiquant si le mode spécifié est actif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Pour les modes boucle et lecture aléatoire, le lecteur Windows Media version 7,0 ou ultérieure. Pour les modes autoRewind et showFrame, le lecteur Windows Media 9 ou version ultérieure.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Settings (objet)**](settings-object.md)
</dt> <dt>

[**Paramètres. setMode**](settings-setmode.md)
</dt> </dl>

 

 





