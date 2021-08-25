---
title: Élément DURATION
description: l’élément DURATION définit la durée pendant laquelle Lecteur Windows Media affiche l’entrée de playlist associée.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- élément DURATION Lecteur Windows Media
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b06b497a6d31b03c4cbec23748f6995a1382fb806ad18fabaa542ed8ff33e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863349"
---
# <a name="duration-element"></a>Élément DURATION

l’élément **DURATION** définit la durée pendant laquelle Lecteur Windows Media affiche l’entrée de playlist associée.

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attributs

**Valeur** (obligatoire)

durée, en heures, minutes, secondes et centièmes de seconde, qu’une entrée est restituée par Lecteur Windows Media. La valeur par défaut correspond à la longueur totale de l’entrée. Si l’entrée est un fichier graphique, vous devez spécifier une valeur de durée.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **entry**, **ref** |
| Éléments enfants  | None               |



 

## <a name="remarks"></a>Remarques

Cet élément définit la durée pendant laquelle un flux doit être rendu. Si l’attribut de **valeur** dépasse la longueur du flux de contenu, le flux se termine à son point de terminaison normal.

Cet élément peut apparaître dans un élément **ref** ou dans un élément **entry** . Toutefois, un élément **Duration** défini dans un élément **ref** remplace celui qui apparaît dans l’élément d' **entrée** parent de l’élément **ref** .

L’élément **Duration** remplace un élément **PREVIEWDURATION** .

## <a name="examples"></a>Exemples


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





