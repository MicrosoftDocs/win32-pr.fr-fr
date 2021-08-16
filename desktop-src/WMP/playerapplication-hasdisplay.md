---
title: PlayerApplication.hasDisplay
description: La propriété hasDisplay récupère une valeur indiquant si la vidéo peut s’afficher par le biais du contrôle de lecteur distant.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- PlayerApplication. hasDisplay Lecteur Windows Media
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cffddc08c154ced6d7cb72b18642b5ebb4960e539e5682d1cf6e8518b74831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747358"
---
# <a name="playerapplicationhasdisplay"></a>PlayerApplication.hasDisplay

La propriété **hasDisplay** récupère une valeur indiquant si la vidéo peut s’afficher par le biais du contrôle de lecteur distant.

## <a name="syntax"></a>Syntaxe

*playerApplication*. **hasDisplay**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture seule.

## <a name="remarks"></a>Remarques

cette propriété est utilisée uniquement lors de la communication à distance du contrôle Lecteur Windows Media.

plusieurs contrôles Lecteur Windows Media peuvent s’exécuter à distance en même temps, mais la vidéo ne peut s’afficher qu’à un seul emplacement à la fois, soit en mode complet du lecteur, soit dans l’un des contrôles Lecteur Windows Media distants. Utilisez cette propriété pour déterminer si le contrôle actuel est celui par le biais duquel la vidéo peut être affichée.

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours **true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





