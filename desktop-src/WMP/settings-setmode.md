---
title: Settings. setMode, méthode
description: La méthode setMode définit différents modes comme active ou inactive.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- méthode setMode lecteur Windows Media
- méthode setMode lecteur Windows Media, classe de paramètres
- Classe de paramètres lecteur Windows Media, méthode setMode
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
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520893"
---
# <a name="settingssetmode-method"></a>Settings. setMode, méthode

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

## <a name="remarks"></a>Notes

Lorsque le mode showFrame est actif, le joueur doit accéder au contenu Track pour récupérer l’image vidéo. En raison des considérations relatives à la bande passante, utilisez ce mode avec précaution lors de la diffusion de contenu non local.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Pour les modes boucle et lecture aléatoire, le lecteur Windows Media version 7,0 ou ultérieure. Pour les modes autoRewind et showFrame, le lecteur Windows Media 9 ou version ultérieure.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Settings (objet)**](settings-object.md)
</dt> <dt>

[**Paramètres. getMode**](settings-getmode.md)
</dt> </dl>

 

 





