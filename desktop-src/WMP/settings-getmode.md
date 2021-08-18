---
title: méthode Paramètres. getMode
description: La méthode getMode détermine si le mode de boucle ou le mode de lecture aléatoire est actif.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- Lecteur Windows Media de la méthode getMode
- Lecteur Windows Media de la méthode getMode, classe Paramètres
- Paramètres de la classe Lecteur Windows Media, méthode getMode
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
ms.openlocfilehash: 779c775319cbe0d6dc443b4eb99febd494db3d30fb35228b7310f8f1ae7d691d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995329"
---
# <a name="settingsgetmode-method"></a>méthode Paramètres. getMode

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
| Version<br/> | pour les modes boucle et lecture aléatoire, Lecteur Windows Media version 7,0 ou ultérieure. pour les modes autoRewind et showFrame, Lecteur Windows Media série 9 ou ultérieure.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> <dt>

[**Paramètres. setMode**](settings-setmode.md)
</dt> </dl>

 

 





