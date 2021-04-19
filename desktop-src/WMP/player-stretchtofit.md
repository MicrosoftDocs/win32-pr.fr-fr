---
title: Player. stretchToFit
description: La propriété stretchToFit spécifie ou récupère une valeur indiquant si la vidéo affichée par le contrôle du lecteur Windows Media se redimensionne automatiquement pour s’adapter à la fenêtre vidéo, lorsque la fenêtre vidéo est plus grande que les dimensions de l’image vidéo.
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
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541265"
---
# <a name="playerstretchtofit"></a>Player. stretchToFit

La propriété **stretchToFit** spécifie ou récupère une valeur indiquant si la vidéo affichée par le contrôle du lecteur Windows Media se redimensionne automatiquement pour s’adapter à la fenêtre vidéo, lorsque la fenêtre vidéo est plus grande que les dimensions de l’image vidéo.

## <a name="syntax"></a>Syntaxe

*lecteur*. **stretchToFit**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                            |
|-------|--------------------------------------------------------|
| true  | La vidéo est étirée pour s’ajuster à la fenêtre.              |
| false | Par défaut. La vidéo n’est pas étirée pour s’ajuster à la fenêtre. |



 

## <a name="remarks"></a>Notes

Quand **stretchToFit** a la valeur true, le contrôle du lecteur Windows Media conserve les proportions d’origine de la vidéo. Si les proportions de la vidéo ne correspondent pas aux proportions de la fenêtre vidéo, les zones de masque noires peuvent apparaître en haut et en bas, ou à gauche et à droite de l’image vidéo.

Cette propriété s’applique au contrôle du lecteur Windows Media uniquement lorsqu’il est incorporé dans une page Web.

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

 

 





