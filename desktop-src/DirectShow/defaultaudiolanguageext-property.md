---
description: La propriété DefaultAudioLanguageExt récupère l’extension de langage audio DVD par défaut.
ms.assetid: 628af2aa-e528-4689-953b-558e13e1d513
title: Propriété DefaultAudioLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03423e6dda19563b55845662f7af5b21df00802726b279068a40c847aa6fc5e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953108"
---
# <a name="defaultaudiolanguageext-property"></a>Propriété DefaultAudioLanguageExt

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DefaultAudioLanguageExt` propriété récupère l’extension de langage audio DVD par défaut.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultAudioLanguageExt
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière indiquant l’extension de langage audio par défaut. Consultez la section Notes pour connaître les valeurs possibles.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut. Le tableau suivant indique les valeurs possibles pour les extensions de langage audio DVD.



| Valeur | Description       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Sous-titres          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

 

 



