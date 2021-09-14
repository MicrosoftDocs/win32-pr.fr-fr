---
title: Élément PREVIEWDURATION
description: L’élément PREVIEWDURATION définit la durée pendant laquelle un clip est lu en mode aperçu.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- élément PREVIEWDURATION Lecteur Windows Media
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292898"
---
# <a name="previewduration-element"></a>Élément PREVIEWDURATION

L’élément **PREVIEWDURATION** définit la durée pendant laquelle un clip est lu en mode aperçu.

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attributs

**Valeur** (obligatoire)

Durée (en heures, minutes, secondes et centièmes de seconde) pendant laquelle le clip est lu en mode aperçu.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                    |
|-----------------|-----------------------------|
| Éléments parents | **ASX**, **entrée**, **référence** |
| Éléments enfants  | None                        |



 

## <a name="remarks"></a>Notes

Cet élément définit la durée pendant laquelle un clip est lu en mode aperçu. Si cet élément apparaît dans un élément **entry** ou **ref** , il s’applique à l’élément défini par cet élément. S’il apparaît dans l’étendue d’un élément **ASX** , il s’applique à chaque clip dans le métafichier. Un élément **PREVIEWDURATION** dans un élément **ref** est prioritaire sur un élément dans un **élément** Entry et est prioritaire sur un élément **PREVIEWDURATION** dans un élément **ASX** . Si aucun élément **PREVIEWDURATION** n’est défini pour un clip, la durée d’aperçu par défaut est de 10 secondes.

s’il existe un élément **STARTTIME** ou **STARTMARKER** pour le clip, Lecteur Windows Media restitue le clip en commençant au point défini par l’un de ces éléments ; Sinon, elle effectue un rendu à partir du début du clip. Le clip s’arrête normalement s’il est plus petit que l’heure définie par l’élément **PREVIEWDURATION** .

L’élément **Duration** remplace un élément **PREVIEWDURATION** .

## <a name="examples"></a>Exemples


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





