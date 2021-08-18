---
title: ClosedCaption.SAMIFileName
description: La propriété SAMIFileName spécifie ou récupère le nom du fichier contenant les informations nécessaires pour le sous-titrage.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- ClosedCaption. SAMIFileName Lecteur Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ba314208db3cb5529042011f269f026a4cf2bd4d4b01d1b8d64719b96a5f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119510"
---
# <a name="closedcaptionsamifilename"></a>ClosedCaption.SAMIFileName

La propriété **SAMIFileName** spécifie ou récupère le nom du fichier contenant les informations nécessaires pour le sous-titrage.

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Le fichier SAMI (Synchronized Accessible Media Interchange) doit utiliser une extension de nom de fichier. SMI ou. sami.

Si vous ne spécifiez pas de valeur pour **SAMIFileName**, cette propriété récupère une chaîne contenant le nom de fichier ou l’URL associé à l’élément multimédia en cours. Cette association peut se produire lorsqu’un fichier SAMI est spécifié à l’aide du paramètre d’URL *sami* , ou automatiquement lorsque le fichier sami porte le même nom que le nom du fichier multimédia numérique (à l’exception de l’extension de nom de fichier). Si aucun fichier SAMI n’est associé au média actuel, cette propriété récupère une chaîne vide ("").

Une fois que vous avez spécifié une valeur pour **SAMIFileName**, cette valeur persiste jusqu’à ce que vous spécifiiez une nouvelle valeur (ou jusqu’à ce qu’un nouvel élément multimédia soit ouvert à l’aide du paramètre URL *sami* ). Par conséquent, vous devez spécifier une nouvelle valeur pour cette propriété avant de lire chaque nouvel élément multimédia. De cette façon, la nouvelle valeur de **SAMIFileName** prend effet lors de l’ouverture de l’élément multimédia suivant (ou de *Player*.**** la méthode Close est appelée). La spécification d’une nouvelle valeur pour **SAMIFileName** n’a aucun effet sur le média actuel.

pour que Lecteur Windows Media retourne à l’aide du fichier SAMI associé à un élément multimédia particulier, spécifiez une valeur pour **SAMIFileName** égale à une chaîne vide ("") avant de lire l’élément multimédia suivant.

**Lecteur Windows Media 10 Mobile :** Cette propriété est en lecture seule et retourne toujours une chaîne vide.

## <a name="examples"></a>Exemples

les trois exemples de JScript suivants utilisent *ClosedCaption*. **SAMIFileName** pour spécifier le nom d’un fichier texte de légende fermé. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objet ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Player. Close**](player-close.md)
</dt> </dl>

 

 





