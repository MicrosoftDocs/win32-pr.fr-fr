---
title: THEMe. playSound
description: La méthode playSound lit le fichier son spécifié.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- THÈME. playSound Windows Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528140"
---
# <a name="themeplaysound"></a>THEMe. playSound

La méthode **playSound** lit le fichier son spécifié.

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*
</dt> <dd>

**Chaîne** spécifiant le nom du fichier son à lire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode vous permet d’ajouter des effets sonores à une apparence, par exemple, en cas de clic sur les boutons. Le son est lu par le système d’exploitation directement et non par le lecteur Windows Media. Cela signifie que le son ne peut pas être contrôlé avec les paramètres et les méthodes du lecteur Windows Media, mais il peut être lu pendant que le lecteur Windows Media lit un autre fichier multimédia numérique.

Cette méthode prend en charge uniquement les fichiers WAV.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément THEMe**](theme-element.md)
</dt> </dl>

 

 





