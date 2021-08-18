---
title: méthode Paramètres. setMode
description: La méthode setMode définit différents modes comme active ou inactive.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- Lecteur Windows Media de la méthode setMode
- Lecteur Windows Media de la méthode setMode, classe Paramètres
- Paramètres de la classe Lecteur Windows Media, méthode setMode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f504fe429dddf1b3db191545e2f34a3605a8fc390346c8f00afe8c3d005f0277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995319"
---
# <a name="settingssetmode-method"></a>méthode Paramètres. setMode

La méthode **setMode** définit différents modes comme active ou inactive.

## <a name="syntax"></a>Syntaxe


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*modeName* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant le nom du mode en cours de modification, contenant l’une des valeurs suivantes.



| String     | Description                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| autoRewind | Mode indiquant si les pistes sont rembobinées jusqu’au début après avoir été lues jusqu’à la fin. L’État par défaut est true.                                                  |
| loop       | Mode indiquant si la séquence de suivi se répète lui-même. L’État par défaut est false.                                                                            |
| showFrame  | Mode indiquant si l’image clé vidéo la plus proche s’affiche à la position actuelle lorsqu’elle n’est pas lue. L’État par défaut est false. N’a aucun effet sur les pistes audio. |
| lecture aléatoire    | Mode indiquant si les pistes sont lues dans un ordre aléatoire. L’État par défaut est false.                                                                            |



 

</dd> <dt>

*État* \[ dans\]
</dt> <dd>

**Valeur booléenne** indiquant si le nouveau mode spécifié est actif ou non.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Lorsque le mode showFrame est actif, le joueur doit accéder au contenu Track pour récupérer l’image vidéo. En raison des considérations relatives à la bande passante, utilisez ce mode avec précaution lors de la diffusion de contenu non local.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | pour les modes boucle et lecture aléatoire, Lecteur Windows Media version 7,0 ou ultérieure. pour les modes autoRewind et showFrame, Lecteur Windows Media série 9 ou ultérieure.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> <dt>

[**Paramètres. getMode**](settings-getmode.md)
</dt> </dl>

 

 





