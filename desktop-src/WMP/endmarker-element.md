---
title: Élément ENDMARKER
description: l’élément ENDMARKER spécifie un marqueur auquel Lecteur Windows Media cessera de restituer le flux.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- élément ENDMARKER Lecteur Windows Media
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 276b17117d2f01d9bc40d7f171a6d0ff6ea2331da439266ac11bf8c25b5e4f25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996659"
---
# <a name="endmarker-element"></a>Élément ENDMARKER

l’élément **ENDMARKER** spécifie un marqueur auquel Lecteur Windows Media cessera de restituer le flux.

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
| Éléments enfants  | None               |



 

## <a name="remarks"></a>Remarques

cet élément spécifie le marqueur où Lecteur Windows Media doit cesser de restituer le flux défini dans l' **entrée** parente ou l’élément **REF** .

Notes

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

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





