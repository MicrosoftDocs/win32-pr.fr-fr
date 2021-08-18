---
title: Player. stretchToFit
description: la propriété stretchToFit spécifie ou récupère une valeur indiquant si la vidéo affichée par le contrôle Lecteur Windows Media se redimensionne automatiquement pour s’adapter à la fenêtre vidéo, lorsque la fenêtre vidéo est plus grande que les dimensions de l’image vidéo.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Lecteur Windows Media Player. stretchToFit
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570d0b9bf7e266af769944b675a85c0ac1518c321d11038ff94cab035dfb316c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995839"
---
# <a name="playerstretchtofit"></a>Player. stretchToFit

la propriété **stretchToFit** spécifie ou récupère une valeur indiquant si la vidéo affichée par le contrôle Lecteur Windows Media se redimensionne automatiquement pour s’adapter à la fenêtre vidéo, lorsque la fenêtre vidéo est plus grande que les dimensions de l’image vidéo.

## <a name="syntax"></a>Syntaxe

*lecteur*. **stretchToFit**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                            |
|-------|--------------------------------------------------------|
| true  | La vidéo est étirée pour s’ajuster à la fenêtre.              |
| false | Par défaut. La vidéo n’est pas étirée pour s’ajuster à la fenêtre. |



 

## <a name="remarks"></a>Remarques

quand **stretchToFit** a la valeur true, le contrôle Lecteur Windows Media conserve les proportions d’origine de la vidéo. Si les proportions de la vidéo ne correspondent pas aux proportions de la fenêtre vidéo, les zones de masque noires peuvent apparaître en haut et en bas, ou à gauche et à droite de l’image vidéo.

cette propriété s’applique au contrôle Lecteur Windows Media uniquement lorsqu’il est incorporé dans une page web.

**Lecteur Windows Media 10 Mobile :** Cette propriété n’est pas prise en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,1 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





