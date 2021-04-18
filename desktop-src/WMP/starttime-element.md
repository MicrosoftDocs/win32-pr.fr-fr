---
title: STARTTIME, élément
description: L’élément STARTTIME définit un index de temps à partir duquel le lecteur Windows Media va commencer le rendu du flux.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- STARTTIME, élément Windows Media Player
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526023"
---
# <a name="starttime-element"></a>STARTTIME, élément

L’élément **StartTime** définit un index de temps à partir duquel le lecteur Windows Media va commencer le rendu du flux.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attributs

**Valeur** (obligatoire)

L’index de temps (en heures, minutes, secondes et centièmes de seconde) à partir duquel le lecteur Windows Media commence à lire un flux défini dans l’élément associé.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **entry**, **ref** |
| Éléments enfants  | Aucune               |



 

## <a name="remarks"></a>Notes

Cet élément définit un index de temps dans le contenu où le lecteur Windows Media doit commencer le rendu du flux. Cet élément peut être utilisé uniquement avec le contenu stocké à la demande qui a été indexé.

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

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





