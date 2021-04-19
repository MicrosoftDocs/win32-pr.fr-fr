---
title: Élément ENDMARKER
description: L’élément ENDMARKER spécifie un marqueur auquel le lecteur Windows Media cesse de restituer le flux.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Élément ENDMARKER lecteur Windows Media
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544369"
---
# <a name="endmarker-element"></a>Élément ENDMARKER

L’élément **ENDMARKER** spécifie un marqueur auquel le lecteur Windows Media cesse de restituer le flux.

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Attributs

**CERTAIN**

Numéro d’un marqueur numérique dans l’index. La valeur par défaut est la fin du contenu.

**NAME**

Nom d’un marqueur nommé dans l’index. La valeur par défaut est la fin du contenu.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **entry**, **ref** |
| Éléments enfants  | Aucune               |



 

## <a name="remarks"></a>Notes

Cet élément spécifie le marqueur dans lequel le lecteur Windows Media doit arrêter le rendu du flux défini dans l’élément d' **entrée** ou de **référence** parent.

Remarque

Utilisez l’élément **ENDMARKER** avec l’attribut **Number** ou **Name** , mais pas les deux.

En mode aperçu, le fait d’atteindre un marqueur de fin arrête l’aperçu, même si l’heure spécifiée par l’élément **PREVIEWDURATION** n’est pas écoulée. L’élément **ENDMARKER** est également prioritaire sur l’élément **Duration** .

Un élément **ENDMARKER** défini dans un élément **ref** est prioritaire sur un **ENDMARKER** défini dans l’élément d' **entrée** parent de l’élément **ref** .

Si le marqueur spécifié par un élément **ENDMARKER** se produit plus tôt dans le flux que le marqueur défini par un élément **STARTMARKER** , aucun contenu n’est lu, mais aucune erreur n’est générée.

## <a name="examples"></a>Exemples


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

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

 

 





