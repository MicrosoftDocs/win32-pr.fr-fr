---
description: La propriété DefaultAudioLanguageExt récupère l’extension de langage audio DVD par défaut.
ms.assetid: 628af2aa-e528-4689-953b-558e13e1d513
title: Propriété DefaultAudioLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5ce89099cd8e31cde9beb8bb3c8a9f1e16b3b0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520964"
---
# <a name="defaultaudiolanguageext-property"></a>Propriété DefaultAudioLanguageExt

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DefaultAudioLanguageExt` propriété récupère l’extension de langage audio DVD par défaut.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultAudioLanguageExt
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière indiquant l’extension de langage audio par défaut. Consultez la section Notes pour connaître les valeurs possibles.

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut. Le tableau suivant indique les valeurs possibles pour les extensions de langage audio DVD.



| Valeur | Description       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Sous-titres          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

 

 



