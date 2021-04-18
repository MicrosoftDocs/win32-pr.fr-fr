---
title: Player. windowlessVideo
description: La propriété windowlessVideo spécifie ou récupère une valeur indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Lecteur Windows Media Player. windowlessVideo
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532829"
---
# <a name="playerwindowlessvideo"></a>Player. windowlessVideo

La propriété **windowlessVideo** spécifie ou récupère une valeur indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre.

## <a name="syntax"></a>Syntaxe

*lecteur*. **windowlessVideo**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** qui est spécifiée au moment de la conception et est en lecture seule par la suite.



| Valeur | Description                                      |
|-------|--------------------------------------------------|
| true  | La vidéo est rendue en mode sans fenêtre.        |
| false | Par défaut. La vidéo est rendue en mode fenêtre. |



 

## <a name="remarks"></a>Notes

Par défaut, un contrôle du lecteur Windows Media incorporé affiche la vidéo dans sa propre fenêtre au sein de la zone cliente. Quand **windowlessVideo** a la valeur true, le contrôle du lecteur affiche la vidéo directement dans la zone cliente, ce qui vous permet d’appliquer des effets spéciaux ou de coucher la vidéo avec du texte.

Dans Windows Vista, le rendu de la vidéo en mode sans fenêtre peut dégrader les performances.

La propriété **windowlessVideo** n’est pas prise en charge pour Netscape Navigator. La définition d’une valeur pour cette propriété dans le navigateur peut donner des résultats inattendus.

**Lecteur Windows Media 10 Mobile :** Cette propriété n’est pas prise en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



 

 





