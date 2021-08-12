---
title: STARTTIME, élément
description: l’élément STARTTIME définit un index de temps à partir duquel Lecteur Windows Media démarrera le rendu du flux.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- STARTTIME, élément Lecteur Windows Media
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9138b05b949098c59996c69143059de5cb5b25cafcd8da7d922de120d586b356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568791"
---
# <a name="starttime-element"></a>STARTTIME, élément

l’élément **STARTTIME** définit un index de temps à partir duquel Lecteur Windows Media démarrera le rendu du flux.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attributs

**Valeur** (obligatoire)

l’index de temps (en heures, minutes, secondes et centièmes de seconde) à partir duquel Lecteur Windows Media commence à lire un flux défini dans l’élément associé.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **entry**, **ref** |
| Éléments enfants  | Aucune               |



 

## <a name="remarks"></a>Notes

cet élément définit un index de temps dans le contenu où Lecteur Windows Media doit commencer le rendu du flux. Cet élément peut être utilisé uniquement avec le contenu stocké à la demande qui a été indexé.

## <a name="examples"></a>Exemples


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





